# Bayesian Optimization in a Billion Dimensions via Random Embeddings
### author
Ziyu Wang‚ Masrour Zoghi‚ Frank Hutter‚ David Matheson and Nando de Freitas
### Paper
doi:10.1613/jair.4806
http://jair.org/media/4806/live-4806-9131-jair.pdf
### Journal
Journal of Artificial Intelligence Research 55 (2016)
### Abstract
Bayesian optimization techniques have been successfully applied to robotics, planning, sensor placement, recommendation, advertising, intelligent user interfaces and automatic algorithm configuration. Despite these successes, the approach is restricted to problems of moderate dimension, and several workshops on Bayesian optimization have identified its scaling to high-dimensions as one of the holy grails of the field. In this paper, we introduce a novel random embedding idea to attack this problem. The resulting Random EMbedding Bayesian Optimization (REMBO) algorithm is very simple, has important invariance prop- erties, and applies to domains with both categorical and continuous variables. We present a thorough theoretical analysis of REMBO. Empirical results confirm that REMBO can effectively solve problems with billions of dimensions, provided the intrinsic dimensionality is low. They also show that REMBO achieves state-of-the-art performance in optimizing the 47 discrete parameters of a popular mixed integer linear programming solver.

ロボティクス，プランニング，センサー配置，レコメンデーション，広告，インテリジェントUI，自動アルゴリズム設計などの分野でベイズ最適化のテクニックは応用され，成功を収めている．一方で，そのアプローチは適度な次元に制限され，ベイズ最適化のいくつか研究集会ではベイズ最適化の高次元へのスケーリングは難しい問題であると考えられている．この論文では我々はこの問題にアタックするために，新しいRandom Embeddingのアイディアを導入する．それによって生まれたRandom EMbeddingベイズ最適化(REMBO) アルゴリズムはとてもシンプルであり，重要な不変性を持ち，カテゴリ変数と連続変数のどちらにも適応する．我々はREMBOの完全な理論解析を示す．また，REMBOは本質的な次元が小さい数十億次元の問題を効果的に解けることを実験的に確認する．その際，一般的な混合整数線形計画法の47個の離散パラメータの最適化において最新の結果を得ることも示される．
