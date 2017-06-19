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

## 基本的なアイディア
本質的には$d_e$次元であるような$D$次元($D\gt \gt d_e$)上のブラックボックス関数$f(\bf{x} )$の最適化問題を考える．通常のBOが問題なく働く次元の数は$D=10$程度である．この論文では$D=10$億程度であっても，本質的な次元が十分小さければ動くようなアルゴリズムが紹介されている．下記がそのアルゴリズムの概要である．

1. $d$を$d_e$以上になるように取る(実際には$d_e$は不明なので妥当な値を仮定する)
2. $D\times d$行列$A$を正規分布から生成する
3. $ {\bf y}_0 \in \mathcal{Y} \subset {\mathbb R}^d$をランダムにとり，$f(A{\bf y} )$を探索する．$A{\bf y}$が${\bf x}$の動く領域$\mathcal{X}$の外に出てしまった場合は，${\mathcal X}$内の最も近い点を探索する
4. 得られた点 ${\bf y}_0$,${\bf y}_1$,...,${\bf y}_t$を元に獲得関数$u$の最大値を取る点$\arg\max u({\bf y})$を計算する
5. 3と同様に$f(A{\bf y}_{t+1})$を探索する．
6. 4,5を繰り返す

![](/img/REMBO.png "rembo")

要するに，${\bf x}\in \mathbb{R}^D$は次元が大きすぎてBOで探索できないが，${\bf y}\in \mathbb{R}^d$であれば探索でき，スパース性（本質的な次元はとても小さいこと）を仮定するとランダムに埋め込んでその上で探索すれば問題ないということを論文中では解析的にも実験的にも示されている．

2点注意がある．
$\mathcal{Y}$を小さく取りすぎると大域解を含まなくなってしまう．論文中では$\mathcal{X}$を正規化した上で，$\mathcal{Y} = [-\sqrt{d},\sqrt{d}]^d$として実験を行っているが，この大きさだと26%程度の確率で大域解が含まれない．これを回避するために，Aを取り直して再度最適化を繰り返し行う．その中に大域解が含まれない確率は指数関数的に減少する．
ベイズ最適化は目的関数の値を得るのにコストがかかるという状況で使われるのに繰り返し行うというのは本末転倒な気がするかもしれないが，普通ベイズ最適化は並列化が難しいのに対し，Aを取り直して再度最適化を行うというのは完全に独立な処理であるから並列化が可能である．
もう一つは$d$の設定を本質的な次元$d_e$より小さく取ると通常のBO(全ての次元を含む)に比べてうまく働かないということである．これは難しい問題で，実用的に$d_e$がどの程度の大きさかはわからないことが多い．それに対する明確な対応策は述べられていない．ただ，そもそも通常のBOが動く状況であればなるべく通常のBOでやるべきなのかもしれない．
