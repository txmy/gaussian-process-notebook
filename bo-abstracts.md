# Bayesian Optimization Abstract book
## On the choice of the low-dimensional domain for global optimization via random embeddings（ランダム埋め込みを用いた大域最適化のための低次元領域の選択について）
[arXiv 2017 preprint]
### Author
Binois, M., Ginsbourger D. & Roustant, O.
### Paper
https://arxiv.org/abs/1704.05318

### Abstract
The challenge of taking many variables into account in optimization problems may be overcome under the hypothesis of low effective dimensionality. Then, the search of solutions can be reduced to the random embedding of a low dimensional space into the original one, resulting in a more manageable optimization problem. Specifically, in the case of time consuming black-box functions and when the budget of evaluations is severely limited, global optimization with random embeddings appears as a sound alternative to random search. Yet, in the case of box constraints on the native variables, defining suitable bounds on a low dimensional domain appears to be complex. Indeed, a small search domain does not guarantee to find a solution even under restrictive hypotheses about the function, while a larger one may slow down convergence dramatically. Here we tackle the issue of low-dimensional domain selection based on a detailed study of the properties of the random embedding, giving insight on the aforementioned difficulties. In particular, we describe a minimal low-dimensional set in correspondence with the embedded search space. We additionally show that an alternative equivalent embedding procedure yields simultaneously a simpler definition of the low-dimensional minimal set and better properties in practice. Finally, the performance and robustness gains of the proposed enhancements for Bayesian optimization are illustrated on three examples.

最適化問題において，多くの変数を考慮するという課題は，有効次元が低いという仮説の下で克服することができる。次に，解の探索は，低次元空間を元の空間にランダムに埋め込むことに減らすことができ，その結果，より扱いやすい最適化問題になる．具体的には，計算コストのかかるブラックボックス関数の場合や，関数の値を求める回数が厳しく制限されている場合，ランダムな埋め込みを伴う大域最適化は，ランダム探索の健全な代替として見える．しかし，元の変数の存在する長方形領域において，低次元領域上の適切な境界を定義することは複雑である．実際，探索領域が小さいと，関数の制限的仮定の下でも解を見つかることは保証されず，探索領域が大きいと，収束を急激に遅くする可能性がある．ここでは，ランダムな埋め込みの性質の詳細な調査に基づいて，低次元空間の領域の選択の問題に取り組み，前述の困難を考察する．特に，埋め込まれた探索空間に対応する最小の低次元集合を述べる．さらに，同等の代替埋め込みの手順によって，低次元最小集合のより簡単な定義と実際のより良い特性が同時に得られることがさらに示される．最後に，提案されたベイズ最適化の改善手法のパフォーマンスとrobustnessの向上を3つの例で示す．

## Ensemble Bayesian Optimization(アンサンブルベイズ最適化)
[arXiv:1706.01445 (preprint)]

### Author
Zi Wang, Clement Gehring, Pushmeet Kohli, Stefanie Jegelka

### Paper
https://arxiv.org/abs/1706.01445

### Abstract
Bayesian Optimization (BO) has been shown to be a very effective paradigm for tackling hard black-box and non-convex optimization problems encountered in Machine Learning. Despite these successes, the computational complexity of the underlying function approximation has restricted the use of BO to problems that can be handled with less than a few thousand function evaluations. Harder problems like those involving functions operating in very high dimensional spaces may require hundreds of thousands or millions of evaluations or more and become computationally intractable to handle using standard Bayesian Optimization methods. In this paper, we propose Ensemble Bayesian Optimization (EBO) to overcome this problem. Unlike conventional BO methods that operate on a single posterior GP model, EBO works with an ensemble of posterior GP models. Further, we represent each GP model using tile coding random features and an additive function structure. Our approach generates speedups by parallelizing the time consuming hyper-parameter posterior inference and functional evaluations on hundreds of cores and aggregating the models in every iteration of BO. Our extensive experimental evaluation shows that EBO can speed up the posterior inference between 2-3 orders of magnitude (400 times in one experiment) compared to the state-of-the-art by putting data into Mondrian bins without sacrificing the sample quality. We demonstrate the ability of EBO to handle sample-intensive hard optimization problems by applying it to a rover navigation problem with tens of thousands of observations.

## Discovering and Exploiting Additive Structure for Bayesian Optimization(ベイズ最適化のための加法構造の発見と活用)
[Proceedings of the 20th International Conference on Artificial Intelligence and Statistics, PMLR 54:1311-1319, 2017.]
### Author
Jacob R. Gardner, Chuan Guo, Kilian Q. Weinberger, Roman Garnett, Roger Grosse

### Paper
http://proceedings.mlr.press/v54/gardner17a/gardner17a.pdf
http://proceedings.mlr.press/v54/gardner17a.html

### Abstract
Bayesian optimization has proven invaluable for black-box optimization of expensive functions. Its main limitation is its exponential complexity with respect to the dimensionality of the search space using typical kernels. Luckily, many objective functions can be decomposed into additive subproblems, which can be optimized independently. We investigate how to automatically discover such (typically unknown) additive structure while simultaneously exploiting it through Bayesian optimization. We propose an efficient algorithm based on Metropolis-Hastings sampling and demonstrate its efficacy empirically on synthetic and real-world data sets. Throughout all our experiments we reliably discover hidden additive structure whenever it exists and exploit it to yield significantly faster convergence.

値を求めるのにコストの掛かる関数のブラックボックス最適化にとって，ベイズ最適化は非常に重要であることが証明されている．その主な制限は，典型的なカーネルを用いた探索空間の次元に対して指数関数的に複雑になることである． 幸いにも，多くの目的関数を独立して最適化できる加法的な問題(additive subproblems)に分解することができる．このような（一般的には未知の）加法構造(additive structure)を自動的に発見し，それをベイズ最適化に活用する方法を調査する．Metropolis-Hastingsサンプリングに基づいた効果的なアルゴリズムを提案し，人工データおよび実世界のデータセットにその効果を経験的に示す．すべての実験を通して，隠れた加法構造が存在する場合は常に発見し，それを利用して有意に高速に収束することを示す．

## Multi-Task Bayesian Optimization(マルチタスクベイズ最適化)
[NIPS 2013]

### Author
Kevin Swersky, Jasper Snoek, Ryan P. Adams

### Paper
http://papers.nips.cc/paper/5086-multi-task-bayesian-optimization.pdf
http://papers.nips.cc/paper/5086-multi-task-bayesian-optimization

### Abstract
Bayesian optimization has recently been proposed as a framework for automatically tuning the hyperparameters of machine learning models and has been shown to yield state-of-the-art performance with impressive ease and efficiency. In this paper, we explore whether it is possible to transfer the knowledge gained from previous optimizations to new tasks in order to find optimal hyperparameter settings more efficiently. Our approach is based on extending multi-task Gaussian processes to the framework of Bayesian optimization. We show that this method significantly speeds up the optimization process when compared to the standard single-task approach. We further propose a straightforward extension of our algorithm in order to jointly minimize the average error across multiple tasks and demonstrate how this can be used to greatly speed up k-fold cross-validation. Lastly, we propose an adaptation of a recently developed acquisition function, entropy search, to the cost-sensitive, multi-task setting. We demonstrate the utility of this new acquisition function by leveraging a small dataset to explore hyperparameter settings for a large dataset. Our algorithm dynamically chooses which dataset to query in order to yield the most information per unit cost.

近年ベイズ最適化は機械学習モデルのハイパーパラメータチューニングを自動的に行うフレームワークとして提案され，印象的な容易さと効率によってstate-of-the-artなパフォーマンスを示している．この論文では，より効率的に最適なハイパーパラメータを見つけるために，前のタスクの最適化の結果から情報を得て，次のタスクに活かすことができるかどうかを調べる．我々のアプローチはマルチタスクガウス過程をベイズ最適化のフレームワークに拡張することをベースとしている．スタンダードなシングルタスクのアプローチに比べて，この手法は有意に最適化のプロセスを高速化することを示す．さらに，マルチタスク間の平均誤差を一緒に最小化するために，我々のアルゴリズムの単純な拡張を行い，どのようにk-fold クロスバリデーションを大幅に高速化されるかを示す．最後に我々は近年開発された獲得関数であるエントロピーサーチをコストに敏感なマルチタスクな設定に適用する．巨大なデータセットのハイパーパラメータの設定に小さなデータセットを活用することによる新しい獲得関数の有用性を示す．我々のアルゴリズムは，1単位コストあたり最も多くの情報をもたらすためにどのデータセット選ぶかを動的に決める．

## Dealing with Integer-valued Variables in Bayesian Optimization with Gaussian Processes（ガウス過程を使った整数変数のベイズ最適化の扱いについて）
[ICML 2017 AutoML Workshop]
### Author
Eduardo C. Garrido-Merchán, Daniel Hernández-Lobato
### Paper
https://arxiv.org/pdf/1706.03673v1.pdf
### Abstract
Bayesian optimization (BO) methods are useful for optimizing functions that are expensiveto evaluate, lack an analytical expression and whose evaluations can be contaminated by noise. These methods rely on a probabilistic model of the objective function, typically a Gaussian process (GP), upon which an acquisition function is built. This function guides the optimization process and measures the expected utility of performing an evaluation of the objective at a new point. GPs assume continous input variables. When this is not the case, such as when some of the input variables take integer values, one has to introduce extra approximations. A common approach is to round the suggested variable value to the closest integer before doing the evaluation of the objective. We show that this can lead to problems in the optimization process and describe a more principled approach to account for input variables that are integer-valued. We illustrate in both synthetic and a real experiments the utility of our approach, which significantly improves the results of standard BO methods on problems involving integer-valued variables.

ベイズ最適化(BO)は数値を求めるのにコストがかかったり，解析的な表現ができなかったり，ノイズの影響を受けるような関数の最適化に役に立つ．BOは目的関数の確率的なモデルに依存し，典型的にはGaussian Process(GP)であり，その上で獲得関数(acquisition function)を構築する．この関数は最適化のプロセスの指針となり，新しい点の目的関数の値がどれだけ良いかを計る．GPは連続的な入力変数を仮定する．そうでない場合，例えば，整数値をとる変数がある場合，それはさらに近似を導入する必要がある．一般的には目的関数の値を計算するときに最も近い整数に丸め込むアプローチが取られる．この方法は最適化のプロセスにおいて問題を引き起こすことを示し，整数値の入力変数のためのより理論に基づいたアプローチを述べる．人工的なデータと実データの両方で我々のアプローチの有用性を調べ，整数値変数のstandard BOの結果が有意に改善することを示す．

## COMBO: An Efficient Bayesian Optimization Library for Materials Science（マテリアルサイエンスのための効率のよいベイズ最適化ライブラリ）
[2016 Materials Discovery]
### Author
Tsuyoshi Ueno, Trevor David Rhone, Zhufeng Hou, Teruyasu Mizoguchi, Koji Tsuda
### paper
http://www.sciencedirect.com/science/article/pii/S2352924516300035
https://doi.org/10.1016/j.md.2016.04.001
### Abstract
In many subfields of chemistry and physics, numerous attempts have been made to accelerate scientific discovery by data-driven experimental design al- gorithms. Among them, Bayesian optimization has been proven as an effec- tive tool. A standard implementation (e.g., scikit-learn), however, can ac- commodate only small training data. We designed an efficient protocol for Bayesian optimization that employs Thompson sampling, random feature maps, one-rank Cholesky update and automatic hyperparameter tuning, and imple- mented it as an open-source python library called COMBO (COMmon Bayesian Optimization library). Promising results are presented in determination of atomic structure of a crystalline interface. COMBO is available at https://github.com/tsudalab/combo .

化学や物理の分野において，データドリブンな実験設計アルゴリズムによる科学的発見の加速のための多くの試みがなされてきた．その中でもベイズ最適化は効果的なツールであることが示されている．しかし，スタンダードな実装では小さいトレーニングデータにしか適応できない．我々はベイズ最適化の効果的なプロトコルであるThompson sampling，random feature map，one-rank Cholesky update，自動パラメータチューニングを採用し，COMBO(COMmon Bayesian Optimization library)と呼ぶPythonライブラリをオープンソースで実装した．結晶表面の原始的な構造の決定に関して期待できる結果が示された．COMBOはこちらで利用可能である． https://github.com/tsudalab/combo

### 補足
[COMBO](/notes/combo.md)

## Taking the Human Out of the Loop: A Review of Bayesian Optimization（ベイズ最適化レビュー：人をループの外側へ）
[2015 Proceedings of the IEEE]
### Author
Bobak Shahriari, Kevin Swersky, Ziyu Wang, Ryan P. Adams, and Nando de Freitas
### Paper
http://ieeexplore.ieee.org/document/7352306/
DOI: 10.1109/JPROC.2015.2494218
### Abstract
Big Data applications are typically associated with systems involving large numbers of users, massive complex software systems, and large-scale heterogeneous computing and storage architectures. The construction of such systems involves many distributed design choices. The end products (e.g., recommendation systems, medical analysis tools, real- time game engines, speech recognizers) thus involve many tunable configuration parameters. These parameters are often specified and hard-coded into the software by various developers or teams. If optimized jointly, these parameters can result in significant improvements. Bayesian optimization is a powerful tool for the joint optimization of design choices that is gaining great popularity in recent years. It promises greater automation so as to increase both product quality and human productivity. This review paper introduces Bayesian optimization, highlights some of its methodological aspects, and showcases a wide range of applications.

ビッグデータの応用は，とても多くのユーザー，巨大で複雑なソフトウェアシステム，巨大な[ヘテロジニアス・コンピューティング](https://goo.gl/Lj6bpa)，ストレージアーキテクチャーに結びついている．そのシステムの構築には多くの分散的な設計選択を伴う．従って，その最終成果（例えば，レコメンデーションシステム，メディカル解析ツール，リアルタイムゲームエンジン，音声認識等）は多くのチューニングすべき設定パラメータを伴う．これらのパラメータは様々な開発者やチームにより，しばしばソフトウェアにhard-codeされている．もし，連帯的に最適化できたのであればこれらのパラメータは有意に改善する結果をもたらす．ベイズ最適化は近年非常に脚光を浴びている，設計選択の連帯最適化に強力なツールである．製品の質と人間の生産性の両方を高めるためによりよい自動化を保証する．このreview paperはベイズ最適化を紹介し，幾つかの方法的側面と，その広い範囲への応用をハイライトする．

## Scalable Bayesian Optimization Using Deep Neural Networks（ディープラーニングを用いたスケーラブルなベイズ最適化）
[2015 PMLR]
### Author
Jasper Snoek, Oren Rippel, Kevin Swersky, Ryan Kiros, Nadathur Satish, Narayanan Sundaram, Md. Mostofa Ali Patwary, Prabhat, Ryan P. Adams

### Paper
http://proceedings.mlr.press/v37/snoek15.html

### Video
http://videolectures.net/icml2015_snoek_neural_networks/

### Abstract
Bayesian optimization is an effective methodology for the global optimization of functions with expensive evaluations. It relies on querying a distribution over functions defined by a relatively cheap surrogate model. An accurate model for this distribution over functions is critical to the effectiveness of the approach, and is typically fit using Gaussian processes (GPs). However, since GPs scale cubically with the number of observations, it has been challenging to handle objectives whose optimization requires many evaluations, and as such, massively parallelizing the optimization. In this work, we explore the use of neural networks as an alternative to GPs to model distributions over functions. We show that performing adaptive basis function regression with a neural network as the parametric form performs competitively with state-of-the-art GP-based approaches, but scales linearly with the number of data rather than cubically. This allows us to achieve a previously intractable degree of parallelism, which we apply to large scale hyperparameter optimization, rapidly finding competitive models on benchmark object recognition tasks using convolutional networks, and image caption generation using neural language models.

ベイズ最適化は値を求めるのにコストが掛かる関数の大域最適化のための有効な手法である．それは、値を求めるのに比較的コストの掛からない代わりのモデルによって定義された関数に対する分布を求めることによる手法である．関数上の分布の正確なモデルは，このアプローチの有効性にとって非常に重要であり，通常はガウス過程（GP）を使用してフィッティングする．しかし，GPは観測数によって cubically にスケールされるため，多くの評価を必要とする目的関数の最適化を扱うことは困難であり，最適化を大規模に並列化することも困難である．
この論文では，関数の分布をモデル化するために，GPの代わりにニューラルネットワークを使用することを考える．パラメトリック形式としてニューラルネットワークを用いて適応基底関数回帰を行うと，state-of-the-artなGPベースのアプローチと競合する程度のパフォーマンスを発揮するが，データ数に対してcubicallyではなく線形にスケールことを示す．これにより，従来の困難であった並列化を達成することができる．大規模なハイパーパラメータの最適化に応用し，畳み込みネットワークを使用したベンチマーク用の物体認識タスクやニューラル言語モデルを使用したイメージキャプション生成において素早く競合するモデルを発見することを示す．

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

### 補足
[Bayesian Optimization in a Billion Dimensions via Random Embeddings](/notes/Bayesian_Optimization_in_a_Billion_Dimensions_via_Random_Embeddings.md)

## Sparse Gaussian Processes for Bayesian Optimization（ベイズ最適化のためのスパースガウス過程）
[2016 UAI'16 Proceedings of the Thirty-Second Conference on Uncertainty in Artificial Intelligence]
### Author
Mitchell McIntire, 	Daniel Ratner, 	Stefano Ermon
### Paper
http://www.auai.org/uai2016/proceedings/papers/269.pdf
http://dl.acm.org/citation.cfm?id=3021002
### Abstract
Bayesian optimization schemes often rely on Gaussian processes (GP). GP models are very flexible, but are known to scale poorly with the number of training points. While several efficient sparse GP models are known, they have limitations when applied in optimization settings. We propose a novel Bayesian optimization framework that uses sparse online Gaussian processes. We introduce a new updating scheme for the online GP that accounts for our preference during optimization for regions with better performance. We apply this method to optimize the performance of a free-electron laser, and demonstrate empirically that the weighted updating scheme leads to substantial improvements to performance in optimization.

ベイズ最適化のスキームはしばしばガウス過程(GP)に依存する．GPモデルは非常に柔軟であるが，トレーニングポイントの数に対してスケールしづらいことが知られている．いくつかの効果的なスパースGPモデルが知られている一方で，それらには最適化に応用するときに制限が存在する．我々はオンラインガウス過程を用いた画期的なベイズ最適化のフレームワークを提案する．我々はオンラインGPの新しい更新スキームを導入する．それはより良いパフォーマンスをもつ領域の最適化の間，我々の好みを説明する．我々はこの手法をフリーエレクトロンレーザーのパフォーマンスの最適化に応用し，重み付けられた更新スキームによって最適化のパフォーマンスが大幅に改善することを実証した．
