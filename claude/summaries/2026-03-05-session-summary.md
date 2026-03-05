# 2026-03-05 セッション要約

## 実施内容

1. `emulsification-process.md` の更新版レビュー
2. `requirement-context-coevolution.md` の新規作成内容レビュー
3. 用語「共進化」「相互形成」についての議論

## emulsification-process.md の現状

前回からの更新で以下が確立済み:
- requirement と context の対比表 (domain / tense / volatileness / explicitness)
- context の4分類 (技術・社会・領域・常識)
- `semantic compiler` という技術非依存の抽象名称

残課題 (後で対応予定):
- requirement の責務「言語を拡張する」の具体例
  - 意味: context にはなかった単語・イディオム・構文・発話を追加していくこと
- context の責務の記述 (requirement に対応する形で)
- 参照リンクの整備 (後でまとめて)

## requirement-context-coevolution.md の内容

繰り返し乳化サイクルと, その間の対話・決定構造が整理された。

**誤字**: line 20「次の入荷過程」→「次の乳化過程」(未修正)

### トポロジの整理

| 名前 | 構造 | 備考 |
|------|------|------|
| 線形 | sequence | 後戻りなし |
| 木 | tree | 実験→選択 |
| 束 | lattice | 複数親許容, DAG より制約強い (上界/下界あり) |
| グラフ | graph | 後戻り・循環あり, 「何でもあり」 |

## 用語の決定

**「共進化」を採用し, 冒頭に機構説明の一文を加える** (合意済み):

> requirement の実現は context を変化させ, context の変化は requirement の更新を促す. この相互的な応答関係を, ここでは生物学の共進化になぞらえて呼ぶ.

補足概念:
- **ニッチ構築 (niche construction)**: executable が context を変え, それが次の requirement に影響するという流れの説明として有用
- **相互形成 (mutual shaping)**: STS (科学技術社会論) の概念. 深ソフトウェア工学は STS にも依拠しているため, 社会的側面を語る際に「相互形成」を使い分ける方針

## モデル構造の変化

現在のモデルの三要素は「乳化 / 共進化 / 対話」だったが, 「乳化と共進化だけでもいいかもしれない」という考えが生まれた (未決定).

## 次のステップ

- 具体化のために, 具体的なプロセスへのモデル適用を行う