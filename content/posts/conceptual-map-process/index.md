---
title: "Process: A Survey of DevOps Concepts and Challenges"
date: 2022-05-03T00:57:38+09:00
categories:
    - devops
---

サーベイ論文 [A Survey of DevOps Concepts and Challenges](https://arxiv.org/pdf/1909.05409.pdf) から _process_ の概念についてみていく。

>DevOps aims to achieve some business outcomes, such as reducing risk and cost, complying with regulations, and improving product quality and customer satisfaction. We grouped these concepts into the process category of concepts, presented in Figure 5, which reveals that DevOps achieves such business outcomes through the accomplishment of a process with frequent and reliable releases. 

DevOps は、頻繁で信頼性のあるリリースをすることによってビジネスの成果を上げることを目標にしている。継続的デリバリーによってもたらされる短いフィードバックサイクルが、プロダクトの質・顧客満足度を改善することにつながっていく。ビジネスで成果につきまとう、リスク・コスト・レギュレーション・プロダクトの質・顧客満足度などをまとめて _process_ という概念にまとめ上げている。

DevOps がどのようにしてビジネスの成果を上げようとしているかを図で示したのが下の図である。"**Freequent and reliable release process**" が中心にきており、DevOps の _process_ において重要なキーワードとなっている。 

{{< imgproc process Fit "800x800" >}}
{{< /imgproc >}}

近年注目されているソフトウェア開発手法のアジャイルは、開発ライフサイクルを短くして、実装した機能に対するフィードバックを早く受けることを目指しており、それを可能にするのが"Freequent and reliable release process"である。そして、この"Freequent and reliable release process"を可能にするのがまさに DevOps なのである。DevOps とアジャイルは別々の文脈で語られるものではなく、また、DevOps はアジャイルを発展させたもの、あるいはアジャイルをベースにしたものであることが図から読み取れる。

DevOps は _process_ だけをあつかったものではなく、そのほかにも _people_、_runtime_、_delivery_ といった概念もあつかっている。残りの概念についても今度みていく。

ONWARDS.
