# Gaussian Process Abstract book
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

## Online Sparse Gaussian Process Regression and Its Applications（オンラインスパースガウス過程回帰とその応用）
### Paper
http://ieeexplore.ieee.org/abstract/document/5549909/?reload=true

### Abstract
We present a new Gaussian process (GP) inference algorithm, called online sparse matrix Gaussian processes (OSMGP), and demonstrate its merits by applying it to the prob- lems of head pose estimation and visual tracking. The OSMGP is based upon the observation that for kernels with local support, the Gram matrix is typically sparse. Maintaining and updating the sparse Cholesky factor of the Gram matrix can be done efficiently using Givens rotations. This leads to an exact, online algorithm whose update time scales linearly with the size of the Gram matrix. Further, we provide a method for constant time operation of the OSMGP using matrix downdates. The downdates maintain the Cholesky factor at a constant size by removing certain rows and columns corresponding to discarded training examples. We demonstrate that, using these matrix downdates, online hyperpa- rameter estimation can be included at cost linear in the number of total training examples. We describe a robust appearance-based head pose estimation system based upon the OSMGP. Numerous experiments and comparisons with existing methods using a large dataset system demonstrate the efficiency and accuracy of our system. Further, to showcase the applicability of OSMGP to a wide variety of problems, we also describe a regression-based visual tracking method. Experiments show that our OSMGP algorithm generalizes well using online learning.

我々はオンラインスパース行列ガウス過程(OSMGP)と呼ばれる，新しいガウス過程推定アルゴリズムを提案する．
