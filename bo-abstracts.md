# Bayesian Optimization Abstract book
## COMBO: An Efficient Bayesian Optimization Library for Materials Science
### Author
Tsuyoshi Ueno, Trevor David Rhone, Zhufeng Hou, Teruyasu Mizoguchi, Koji Tsuda

### Abstract
In many subfields of chemistry and physics, numerous attempts have been made to accelerate scientific discovery by data-driven experimental design al- gorithms. Among them, Bayesian optimization has been proven as an effec- tive tool. A standard implementation (e.g., scikit-learn), however, can ac- commodate only small training data. We designed an efficient protocol for Bayesian optimization that employs Thompson sampling, random feature maps, one-rank Cholesky update and automatic hyperparameter tuning, and imple- mented it as an open-source python library called COMBO (COMmon Bayesian Optimization library). Promising results are presented in determination of atomic structure of a crystalline interface. COMBO is available at https://github.com/tsudalab/combo .

化学や物理の分野において，データドリブンな実験設計アルゴリズムによる科学的発見の加速のための多くの試みがなされてきた．その中でもベイズ最適化は効果的なツールであることが示されている．しかし，スタンダードな実装では小さいトレーニングデータにしか適応できない．我々はベイズ最適化の効果的なプロトコルであるThompson sampling，random feature map，one-rank Cholesky update，自動パラメータチューニングを採用し，COMBO(COMmon Bayesian Optimization library)と呼ぶPythonライブラリをオープンソースで実装した．結晶表面の原始的な構造の決定に関して期待できる結果が示された．COMBOはこちらで利用可能である． https://github.com/tsudalab/combo

### 補足
[COMBO](/notes/combo.md)

## Taking the Human Out of the Loop: A Review of Bayesian Optimization
### Author
Bobak Shahriari, Kevin Swersky, Ziyu Wang, Ryan P. Adams, and Nando de Freitas
### Paper

### Abstract
Big Data applications are typically associated with systems involving large numbers of users, massive complex software systems, and large-scale heterogeneous computing and storage architectures. The construction of such systems involves many distributed design choices. The end products (e.g., recommendation systems, medical analysis tools, real- time game engines, speech recognizers) thus involve many tunable configuration parameters. These parameters are often specified and hard-coded into the software by various developers or teams. If optimized jointly, these parameters can result in significant improvements. Bayesian optimization is a powerful tool for the joint optimization of design choices that is gaining great popularity in recent years. It promises greater automation so as to increase both product quality and human productivity. This review paper introduces Bayesian optimization, highlights some of its methodological aspects, and showcases a wide range of applications.

ビッグデータの応用は，とても多くのユーザー，巨大で複雑なソフトウェアシステム，巨大な[ヘテロジニアス・コンピューティング](https://goo.gl/Lj6bpa)，ストレージアーキテクチャーに結びついている．そのシステムの構築には多くの分散的な設計選択を伴う．従って，その最終成果（例えば，レコメンデーションシステム，メディカル解析ツール，リアルタイムゲームエンジン，音声認識等）は多くのチューニングすべき設定パラメータを伴う．これらのパラメータは様々な開発者やチームにより，しばしばソフトウェアにhard-codeされている．もし，連帯的に最適化できたのであればこれらのパラメータは有意に改善する結果をもたらす．ベイズ最適化は近年非常に脚光を浴びている，設計選択の連帯最適化に強力なツールである．製品の質と人間の生産性の両方を高めるためによりよい自動化を保証する．このreview paperはベイズ最適化を紹介し，幾つかの方法的側面と，その広い範囲への応用をハイライトする．

## Scalable Bayesian Optimization Using Deep Neural Networks
### Author
Jasper Snoek
### Paper
http://videolectures.net/site/normal_dl/tag=1005113/icml2015_snoek_neural_networks_01.pdf
### Video
http://videolectures.net/icml2015_snoek_neural_networks/
### Abstract
Bayesian optimization is an effective methodology for the global optimization of functions with expensive evaluations. It relies on querying a distribution over functions defined by a relatively cheap surrogate model. An accurate model for this distribution over functions is critical to the effectiveness of the approach, and is typically fit using Gaussian processes (GPs). However, since GPs scale cubically with the number of observations, it has been challenging to handle objectives whose optimization requires many evaluations, and as such, massively parallelizing the optimization. In this work, we explore the use of neural networks as an alternative to GPs to model distributions over functions. We show that performing adaptive basis function regression with a neural network as the parametric form performs competitively with state-of-the-art GP-based approaches, but scales linearly with the number of data rather than cubically. This allows us to achieve a previously intractable degree of parallelism, which we apply to large scale hyperparameter optimization, rapidly finding competitive models on benchmark object recognition tasks using convolutional networks, and image caption generation using neural language models.

## Bayesian Optimization in a Billion Dimensions via Random Embeddings (Random Embeddingを使った10億次元のベイズ最適化)
### Author
Ziyu Wang‚ Masrour Zoghi‚ Frank Hutter‚ David Matheson and Nando de Freitas
### Paper
doi:10.1613/jair.4806
http://jair.org/media/4806/live-4806-9131-jair.pdf
### Journal
Journal of Artificial Intelligence Research 55 (2016)
### Abstract
Bayesian optimization techniques have been successfully applied to robotics, planning, sensor placement, recommendation, advertising, intelligent user interfaces and automatic algorithm configuration. Despite these successes, the approach is restricted to problems of moderate dimension, and several workshops on Bayesian optimization have identified its scaling to high-dimensions as one of the holy grails of the field. In this paper, we introduce a novel random embedding idea to attack this problem. The resulting Random EMbedding Bayesian Optimization (REMBO) algorithm is very simple, has important invariance prop- erties, and applies to domains with both categorical and continuous variables. We present a thorough theoretical analysis of REMBO. Empirical results confirm that REMBO can effectively solve problems with billions of dimensions, provided the intrinsic dimensionality is low. They also show that REMBO achieves state-of-the-art performance in optimizing the 47 discrete parameters of a popular mixed integer linear programming solver.

ロボティクス，プランニング，センサー配置，レコメンデーション，広告，インテリジェントUI，自動アルゴリズム設計などの分野でベイズ最適化のテクニックは応用され，成功を収めている．一方で，そのアプローチは適度な次元に制限され，ベイズ最適化のいくつか研究集会ではベイズ最適化の高次元へのスケーリングは難しい問題であると考えられている．この論文では我々はこの問題にアタックするために，新しいRandom Embeddingのアイディアを導入する．それによって生まれたRandom EMbeddingベイズ最適化(REMBO) アルゴリズムはとてもシンプルであり，重要な不変性を持ち，カテゴリ変数と連続変数のどちらにも適応する．我々はREMBOの完全な理論解析を示す．また，REMBOは本質的な次元が小さい数十億次元の問題を効果的に解けることを実験的に確認する．その際，一般的な混合整数線形計画法の47個の離散パラメータの最適化において最新の結果を得ることも示される．

## Sparse Gaussian Processes for Bayesian Optimization（ベイズ最適化のためのスパースガウス過程）
### Paper
http://www.auai.org/uai2016/proceedings/papers/269.pdf

### Abstract
Bayesian optimization schemes often rely on Gaussian processes (GP). GP models are very flexible, but are known to scale poorly with the number of training points. While several efficient sparse GP models are known, they have limitations when applied in optimization settings. We propose a novel Bayesian optimization framework that uses sparse online Gaussian processes. We introduce a new updating scheme for the online GP that accounts for our preference during optimization for regions with better performance. We apply this method to optimize the performance of a free-electron laser, and demonstrate empirically that the weighted updating scheme leads to substantial improvements to performance in optimization.

ベイズ最適化のスキームはしばしばガウス過程(GP)に依存する．GPモデルは非常に柔軟であるが，トレーニングポイントの数に対してスケールしづらいことが知られている．いくつかの効果的なスパースGPモデルが知られている一方で，それらには最適化に応用するときに制限が存在する．我々はオンラインガウス過程を用いた画期的なベイズ最適化のフレームワークを提案する．我々はオンラインGPの新しい更新スキームを導入する．それはより良いパフォーマンスをもつ領域の最適化の間，我々の好みを説明する．我々はこの手法をフリーエレクトロンレーザーのパフォーマンスの最適化に応用し，重み付けられた更新スキームによって最適化のパフォーマンスが大幅に改善することを実証した．
