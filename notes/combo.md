# COMBO: An Efficient Bayesian Optimization Library for Materials Science

## Author
Tsuyoshi Ueno, Trevor David Rhone, Zhufeng Hou, Teruyasu Mizoguchi, Koji Tsuda

## Abstract
In many subfields of chemistry and physics, numerous attempts have been made to accelerate scientific discovery by data-driven experimental design al- gorithms. Among them, Bayesian optimization has been proven as an effec- tive tool. A standard implementation (e.g., scikit-learn), however, can ac- commodate only small training data. We designed an efficient protocol for Bayesian optimization that employs Thompson sampling, random feature maps, one-rank Cholesky update and automatic hyperparameter tuning, and imple- mented it as an open-source python library called COMBO (COMmon Bayesian Optimization library). Promising results are presented in determination of atomic structure of a crystalline interface. COMBO is available at https://github.com/tsudalab/combo .

化学や物理の分野において，データドリブンな実験設計アルゴリズムによる科学的発見の加速のための多くの試みがなされてきた．その中でもベイズ最適化は効果的なツールであることが示されている．しかし，スタンダードな実装では小さいトレーニングデータにしか適応できない．我々はベイズ最適化の効果的なプロトコルであるThompson sampling，random feature map，one-rank Cholesky update，自動パラメータチューニングを採用し，COMBO(COMmon Bayesian Optimization library)と呼ぶPythonライブラリをオープンソースで実装した．結晶表面の原始的な構造の決定に関して期待できる結果が示された．COMBOはこちらで利用可能である． https://github.com/tsudalab/combo

## Thompson sampling
$x_i$
