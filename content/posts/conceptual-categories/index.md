---
title: "Conceptual Categories"
date: 2022-05-02T02:12:43+09:00
categories:
    - devops
---
[A Survey of DevOps Concepts and Challenges](https://arxiv.org/pdf/1909.05409.pdf) の内容をまとめていく。まずは conceptual categories から。

さまざまな文献を分析することによって、DevOps のコンセプトは大きく4つのカテゴリーに大別することができる。その4つとは、_process_, _people_, _delivery_, _runtime_ である。そして、この4つのカテゴリーは学術論文で最も引用されている DevOps の定義と合致している。

学術論文で最も引用されている DevOps の定義をみていく。

>DevOps is a collaborative and multidisciplinary effort within an organization to automate continuous delivery of new software versions, while guaranteeing their correctness and reliability.

conceptual categories と 定義が合致する部分は下記

- _process_: continuous delivery
- _people_: a collaborative and multidisciplinary effort within an organization
- _delivery_: automate, guaranteeing software correctness 
- _runtime_: reliability

conceptual categories を可視化すると下記の図になる。

{{< imgproc conceptual-category Fit "450x450" >}}
{{< /imgproc >}}

Engineering 的な側面と Management 的な側面に分かれ、Engineering な側面は Ops または Dev に関係するかで分かれる。SRE は Ops に関係している Runtime の概念から生まれた。

conceptual categories は、この論文で提唱されている a conceptual framework of fundamental concepts of DevOps の構成概念の1つである。その他の構成概念はまた今度見ていく。
