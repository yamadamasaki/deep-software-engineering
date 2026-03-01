---
date: 2026-03-01
participants: [human, claude]
topic: emulsification-process.md の充実版レビュー
related:
  - artifacts/proposal-draft-2/emulsification-process.md
  - claude/summaries/2026-02-23-session-summary.md
---

## Human

前回のレビューも踏まえて, emulsification-prorcess.md の記述を大幅に充実させました. 再度意見をください

## Claude

（ファイルおよび前回セッション要約を確認の上、以下の点について意見を述べた）

### 全体評価
大幅な充実で、文書として読めるものになった。三つのセクション（requirement/architecture/emulsification の例）が埋まったことで、概念の輪郭が見えてきた。

### 評価した点
- 「executable が分散質、architecture が規定する社会が分散媒、全体が emulsion になる」という記述は、前版より格段に豊か
- 「常識アーキテクチャ」という分類は命名として鋭い
- 「semantic compiler」は良い造語
- 「これらの成立過程」（requirements の成立経緯を含める）という視点は本質的

### 指摘した問題点

1. **乳化剤が消えている**: 前回確立した「言語モデル = 乳化剤」が物理メタファーの説明部分から消えている。semantic compiler がその役を担っているとはいえ、冒頭の物理モデルで明示が必要。

2. **分散媒の定式の論理ズレ**: 「分散媒 = architecture が規定する社会」という定式で、architecture（入力）とそれが記述する社会（分散媒）を区別すべき。architecture は社会のモデルであり社会そのものではない。

3. **「はっきする」→「発揮する」**: 誤記と思われる。

4. **「少労力かつ高コスト」の逆説**: 人的労力とコンピュータ資源コストの区別を一文添えると良い。

5. **architecture vs context の問いが宙吊り**: 冒頭のメモ `___architecture ではなく context と呼んだ方がいいかもしれない___` を決断して解決すべき。"substrate"などの代替案も提示した。

6. **semantic compiler ステップ6のフィードバック**: 「semantic compiler 自体へのフィードバック」の説明が薄い。→ **ユーザーの回答: この説明は req/arch co-evolution で行う予定**。

7. **「常識アーキテクチャ」の説明不足**: 他の3種類と異なり、「何か」でなく「誰が提供するか」しか書いていない。

### まとめ
次の一手として最重要:
- 乳化剤（言語モデル）を本文の物理メタファー部分で明示する
- architecture vs context の問いに答える

## Human

ok, (6) の説明は req/arch co-evolution でする予定です. それ以外についてはまた改善します. 今日のところはいったん終了しましょう. thanx!
