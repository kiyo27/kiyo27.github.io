---
title: "Runtime: A Survey of DevOps Concepts and Challenges"
date: 2022-05-18T23:18:17+09:00
# bookComments: false
# bookSearchExclude: false
categories:
    - devops
---

サーベイ論文 [A Survey of DevOps Concepts and Challenges](https://arxiv.org/pdf/1909.05409.pdf) から _runtime_ の概念についてみていく。

継続的デリバリーによって新しいバージョンのソフトウェアをリリースするだけでは十分ではなく、新しいバージョンが安定して信頼できる状態にすることもまた必要である。DevOps における _runtime_ はそのことに焦点を当てる。

{{< imgproc runtime Fit "800x800" >}}
{{< /imgproc >}}

SRE は _runtime_ の監視をソフトウェアを使って自動化させることからきている。