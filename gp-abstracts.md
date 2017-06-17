# Gaussian Process Abstract book
## A Review of Heteroscedasticity Treatment with Gaussian Processes and Quantile Regression Meta-models
[Seeing Cities Through Big Data
Part of the series Springer Geography pp 141-160
Date: 08 October 2016]

### Author
Francisco Antunes , Aidan O’Sullivan, Filipe Rodrigues, Francisco Pereira

### Paper
https://link.springer.com/chapter/10.1007/978-3-319-40902-3_9

### Abstract
For regression problems, the general practice is to consider a constant variance of the error term across all data. This aims to simplify an often complicated model and relies on the assumption that this error is independent of the input variables. This property is known as homoscedasticity. On the other hand, in the real world, this is often a naive assumption, as we are rarely able to exhaustively include all true explanatory variables for a regression. While Big Data is bringing new opportunities for regression applications, ignoring this limitation may lead to biased estimators and inaccurate confidence and prediction intervals.
This paper aims to study the treatment of non-constant variance in regression models, also known as heteroscedasticity. We apply two methodologies: integration of conditional variance within the regression model itself; treat the regression model as a black box and use a meta-model that analyzes the error separately. We compare the performance of both approaches using two heteroscedastic data sets.
Although accounting for heteroscedasticity in data increases the complexity of the models used, we show that it can greatly improve the quality of the predictions, and more importantly, it can provide a proper notion of uncertainty or “confidence” associated with those predictions. We also discuss the feasibility of the solutions in a Big Data context.

## Learning to Detect Sepsis with a Multitask Gaussian Process RNN Classifier（マルチタスクガウス過程RNN分類器を用いた敗血症検出の学習）
[ICML 2017]

### Author
[Joseph Futoma, Sanjay Hariharan, Katherine Heller]

### Paper
https://arxiv.org/pdf/1706.04152.pdf

### Abstract
We present a scalable end-to-end classifier that uses streaming physiological and medication data to accurately predict the onset of sepsis, a life-threatening complication from infections that has high mortality and morbidity. Our pro- posed framework models the multivariate trajec- tories of continuous-valued physiological time series using multitask Gaussian processes, seam- lessly accounting for the high uncertainty, fre- quent missingness, and irregular sampling rates typically associated with real clinical data. The Gaussian process is directly connected to a black-box classifier that predicts whether a pa- tient will become septic, chosen in our case to be a recurrent neural network to account for the ex- treme variability in the length of patient encoun- ters. We show how to scale the computations as- sociated with the Gaussian process in a manner so that the entire system can be discriminatively trained end-to-end using backpropagation. In a large cohort of heterogeneous inpatient encoun- ters at our university health system we find that it outperforms several baselines at predicting sep- sis, and yields 19.4% and 55.5% improved ar- eas under the Receiver Operating Characteristic and Precision Recall curves as compared to the NEWS score currently used by our hospital.

## Scaling up the Automatic Statistician: Scalable Structure Discovery using Gaussian Processes（Automatic Statisticianのスケールアップ：ガウス過程を用いたスケーラブルな構造の発見）
+ [ArXiv, 2017]
+ [AutoML 2016, Journal of Machine Learning Research Workshop and Conference Proceedings. Practical Bayesian Nonparametrics Workshop, NIPS 2016. Oral & Travel Award. ]

### Author
Hyunjik Kim, Yee Whye Teh

### Paper
+ https://arxiv.org/pdf/1706.02524.pdf
+ http://proceedings.mlr.press/v64/kim_scalable_2016.pdf

### Abstract
Automating statistical modelling is a challenging problem that has far-reaching implications for artificial intelligence. The Automatic Statistician employs a kernel search algorithm to provide a first step in this direction for regression problems. However this does not scale due to its O(N3) running time for the model selection. This is undesirable not only because the average size of data sets is growing fast, but also because there is potentially more information in bigger data, implying a greater need for more expressive models that can discover finer structure. We propose Scalable Kernel Composition (SKC), a scalable kernel search algorithm, to encompass big data within the boundaries of automated statistical modelling.

自動統計モデリングは人工知能に広く影響するチャレンジングな問題である．Automatic Statisticianは回帰の問題にこの方向で最初の一歩を提供するために，カーネルサーチアルゴリズムを採用している．しかし，これはモデル選択にO(n^3)の計算量がかかり，スケールしない．データセットの平均サイズはすぐに増えていくという理由からだけでなく，大きいデータにはより多くのデータが潜在しているという理由からも，スケールしないことは望ましくない．良い構造を見つけることができる，より表現豊かなモデルが必要である，ということである．我々はスケーラブルなカーネルサーチアルゴリズムである，Scalable Kernel Composition (SKC)を提案し，自動統計モデリングの領域をビッグデータを含む領域まで広げる．

## Online Sparse Gaussian Process Regression and Its Applications（オンラインスパースガウス過程回帰とその応用）
[IEEE TRANSACTIONS ON IMAGE PROCESSING, VOL. 20, NO. 2, FEBRUARY 2011]

### Author
[Ananth Ranganathan, Ming-Hsuan Yang, Senior Member, IEEE, and Jeffrey Ho]

### Paper
http://ieeexplore.ieee.org/abstract/document/5549909/?reload=true

### Abstract
We present a new Gaussian process (GP) inference algorithm, called online sparse matrix Gaussian processes (OSMGP), and demonstrate its merits by applying it to the problems of head pose estimation and visual tracking. The OSMGP is based upon the observation that for kernels with local support, the Gram matrix is typically sparse. Maintaining and updating the sparse Cholesky factor of the Gram matrix can be done efficiently using Givens rotations. This leads to an exact, online algorithm whose update time scales linearly with the size of the Gram matrix. Further, we provide a method for constant time operation of the OSMGP using matrix downdates. The downdates maintain the Cholesky factor at a constant size by removing certain rows and columns corresponding to discarded training examples. We demonstrate that, using these matrix downdates, online hyperparameter estimation can be included at cost linear in the number of total training examples. We describe a robust appearance-based head pose estimation system based upon the OSMGP. Numerous experiments and comparisons with existing methods using a large dataset system demonstrate the efficiency and accuracy of our system. Further, to showcase the applicability of OSMGP to a wide variety of problems, we also describe a regression-based visual tracking method. Experiments show that our OSMGP algorithm generalizes well using online learning.

我々はオンラインスパース行列ガウス過程(OSMGP)と呼ばれる，新しいガウス過程推定アルゴリズムを提案し，頭部の姿勢推定と[ビジュアルトラッキング](http://www.indsys.chuo-u.ac.jp/~sakane/research-A.htm)の問題に応用することでそれのメリットを示す．OSMGPはカーネルを局所的にサポートするために，普通，そのグラム行列はスパースである．[ギブンス回転 (Givens rotation) ](https://goo.gl/oLqQ4j)を使うことで，効果的にグラム行列のスパースな[コレスキー因子](https://goo.gl/CctIyJ)の維持(maintaining)や更新(updating)をすることが可能である．これは，グラム行列のサイズに対して線形時間で更新できる正確なオンラインアルゴリズムを導く．さらに，行列のダウンデート(downdate)を使ってOSMGPのオペレーションを定数時間にする手法も示す．ダウンデートは特定の行と列を削除する(学習サンプルを破棄する)ことによって，コレスキー因子を定数サイズに維持する．これらの行列のダウンデートを使って，学習サンプルの総数に対して線形なコストで，オンラインハイパーパラメータ推定ができることを示す．OSMGPを使ったロバストな外観ベースの頭部の姿勢推定システムを説明する．大きなデータセットを使った既存の手法の多数の実験と比較により，我々のシステムの有効性と正確さが示される．さらに，OSMGPの広範囲の問題に渡る応用性を示すために，回帰ベースのビジュアルトラッキング手法も説明する．実験では我々のOSMGPアルゴリズムはオンライン学習を使ってうまく汎化できることを示す．
