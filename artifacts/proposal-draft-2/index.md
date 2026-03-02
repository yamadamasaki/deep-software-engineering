# 深ソフトウェア工学の一モデルの提案

## 概要

[proposal-draft-1](./proposal-draft-1.md) (本リポジトリ内) あるいは [深ソフトウェア工学](https://yamadamasaki.github.io/deep-software-engineering/) (外部リンク) で述べたような, 新たなソフトウェア工学の一つのモデル (model01 と呼ぶ. 可能ならば複数のモデルを提出し, それらを比較検討したい) を提案する.

このモデルでは, requirement と context という (わたしたちにとっては馴染みのある用語である) 二種類の材料 (material) から出発する. これらの実体はともに, 広い意味での言語による表現の集合である.

context は技術的および社会的な (広い範囲で) 共有可能な言明の集合であり, requirement は今眼前に対象 (あるいはその理想像) としてあるものについての固有な言明の集合である. この二つはかなり異なるものであり, 材料としてはそれぞれに本質的ではあるが, そのままでは混じり合わないし, 何らかの構築物を構成するものではない.

いわゆる「ソフトウェア構築 (開発)」をわたしたちはこの二種類の材料の「乳化過程」(もちろん比喩である) として考える ([emulsification process](./emulsification-process.md)).

この「乳化過程」は一段階で完了するとは限らず, 完成 (があるとすれば, そこ) に至るまで複数の段階を必要とする場合もある. 複数の段階の構成にはさまざまなパタンがあり得る. 例えば

- 線形 (直線的)
- 木
- 束

このとき, この過程によって requirement も context も変化 (transformation) を被り, context から requirement へのフィードバックが生じることになる ([requirement/context coevolution](./requirement-context-coevolution.md)).

これら二階層のプロセスを貫くのが, 定期的, あるいは事態の進展に応じて召集され, すべての行為者 (一部にその代表者) が集まって行われる対話である. そこでは, 行為者間の言語行為によってプロセス全体の方向性や次のプロセスの実装が決定されていく ([dialogue](./dialogue.md)).

このモデルの三つの基本概念 (とそれらの統合) のより詳細は以下を参照のこと.

1. [emulsification process](./emulsification-process.md)
2. [requirement/context coevolution](./requirement-context-coevolution.md)
3. [dialogue](./dialogue.md)

## 深ソフトウェア工学との整合性

## 古典的ソフトウェア工学との関係

## 後アジャイル・ソフトウェア工学との関係

## 本モデル提案の今後の展望
