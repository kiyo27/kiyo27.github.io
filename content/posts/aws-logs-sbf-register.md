---
title: "aws cli でサブスクリプションフィルターを登録"
date: 2025-08-03T10:48:13+09:00
# bookComments: false
# bookSearchExclude: false
categories:
    - aws
---

aws cli で CloudWatch Logs のロググループにサブスクリプションフィルターを登録する。登録しようとしているサブスクリプションフィルターがすでにある場合は、登録処理をスキップするようになっている。

```shell
#!/bin/bash

# 設定項目
FIREHOSE_ARN="arn:aws:firehose:ap-northeast-1:123456789012:deliverystream/my-delivery-stream"
ROLE_ARN="arn:aws:iam::123456789012:role/CWLToFirehoseRole"
FILTER_PATTERN=""
REGION="ap-northeast-1"
LOG_GROUP_PREFIX="/dev/ecs/batch-"

# ロググループの一覧を取得
log_groups=$(aws logs describe-log-groups \
  --log-group-name-prefix "$LOG_GROUP_PREFIX" \
  --region "$REGION" \
  --query "logGroups[*].logGroupName" \
  --output text)

# 各ロググループに対して処理
for log_group in $log_groups; do
  echo "Checking $log_group..."

  base_name=$(basename "$log_group")
  filter_name="${base_name}-subscription-filter"

  # 既存のサブスクリプションフィルター一覧を取得
  filters=$(aws logs describe-subscription-filters \
    --log-group-name "$log_group" \
    --region "$REGION" \
    --query "subscriptionFilters[*].filterName" \
    --output text)

  if echo "$filters" | grep -q "${filter_name}"; then
    echo "Subscription filter '$filter_name' already exists for $log_group. Skipping."
  else
    echo "Creating subscription filter '$filter_name' for $log_group"

    aws logs put-subscription-filter \
      --log-group-name "$log_group" \
      --filter-name "$filter_name" \
      --filter-pattern "$FILTER_PATTERN" \
      --destination-arn "$FIREHOSE_ARN" \
      --role-arn "$ROLE_ARN" \
      --region "$REGION"
  fi
done
```