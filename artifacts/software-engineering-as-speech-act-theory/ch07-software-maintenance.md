# Chapter 07: Software Maintenance — 言語行為としての読解

> SWEBOK v4 Chapter 7 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 保守とは「過去の発話を現在の文脈で生かし続ける」営みである

ソフトウェア保守は、過去に発せられた発話（ソフトウェア）を、変化する環境・要求の中で意味あるものとして維持し、進化させる活動である。構築が「発話の生成」、運用が「発話の持続」であるなら、保守は**発話の解釈と改訂**——時間の経過とともに変わる文脈の中で、発話の意図を再確認し、必要に応じて発話そのものを修正する営み——である。

---

## 1. 保守の本質は「他者の発話の理解」から始まる

### SWEBOK の記述

> "Limited understanding describes a software engineer's initial comprehension of software someone else developed. This is reflected in how quickly a software engineer can understand where to change or correct the software." (§2.1.1)

> "Research suggests a significant portion of total maintenance effort is devoted to understanding the software to be modified." (§2.1.1)

### 言語行為としての意義

保守の中核的課題は**他者が発した発話（コード）の理解**——言語行為理論でいう**解釈 (interpretation)** の問題——である:

- 保守者は開発者とは別の行為者であることが多い——**発話者不在の状況での解釈**
- 理解の困難さの要因: ドメイン知識、実装慣行、ドキュメント、構造——すべて**対話の文脈情報**
- 開発者が去った後の保守 = **原著者のいないテクストの解釈**——解釈学的状況

「Comprehension is more difficult in text-oriented representation」という指摘は、コードが発話の一形態であり、その理解が本質的に**解釈行為**であることを示している。

---

## 2. Lehman の進化法則は「発話の生態学」を記述している

### SWEBOK の記述

> "Continuing Change — Software must be continually adapted, or it becomes progressively less satisfactory." (§1.5)

> "Increasing Complexity — As software evolves, its complexity increases unless work is done to maintain or reduce that complexity." (§1.5)

> "Feedback System — Software evolution processes constitute multilevel, multiloop, multi-agent feedback systems and must be treated as such." (§1.5)

### 言語行為としての意義

Lehman の8つの進化法則は、ソフトウェアという発話が現実世界の中で辿る**生態学的過程**を記述している:

- **Continuing Change**: 発話は文脈が変わると意味が変わる——環境に適応し続けなければ発話は無意味になる
- **Increasing Complexity**: 改訂を重ねた発話は次第に複雑化する——明晰さの格率への継続的な努力が必要
- **Conservation of Familiarity**: 関係者全員が発話の内容と振る舞いに精通し続けなければならない——**共有された理解の維持**
- **Feedback System**: 進化は「多層・多ループ・多行為者のフィードバック系」——まさに**多者間対話**

「software programs are never complete and continue to evolve」は、ソフトウェアが**終わりのない対話**であることの宣言である。

---

## 3. 保守カテゴリは「改訂の動機の分類」である

### SWEBOK の記述

> 5つのカテゴリ: corrective（修正的）、preventive（予防的）、adaptive（適応的）、additive（追加的）、perfective（完全化）。さらに emergency（緊急）。(§1.6)

### 言語行為としての意義

保守カテゴリは、発話の**改訂動機の類型学**に対応する:

- **Corrective**: 発話の誤りの修正——「言い間違い」の訂正
- **Preventive**: 潜在的な誤りの事前修正——「誤解を招きうる表現」の改善
- **Adaptive**: 文脈の変化に合わせた発話の調整——環境変化への**語用論的適応**
- **Additive**: 新しい内容の追加——発話の**拡張**
- **Perfective**: 表現の洗練——同じ意味をより良く伝える
- **Emergency**: 緊急の応急措置——「とりあえず通じるように」する暫定的修正

80%以上が enhancement（corrective 以外）であるという事実は、保守が「バグ修正」ではなく**発話の継続的進化**であることを示す。

---

## 4. 技術的負債は「発話の質の劣化」の蓄積である

### SWEBOK の記述

> "Technical debt often accumulates when the need to quickly address corrective, emergency, and additive maintenance tasks, constrained by limited time and understanding of the software, leads to compromises." (§2.1.4)

> "Technical debt represents the effort required to fix problems that remain in the code when an application is initially released." (§2.3.1)

### 言語行為としての意義

技術的負債は、**発話の質に関する妥協の蓄積**である:

- 時間的制約下での不十分な表現——Grice の格率に反する発話の蓄積
- 「readable code よりも quick fix」を選ぶことの代償
- 負債の返済 = 過去の不明瞭な発話を明晰に書き直すこと——**遡及的な表現の改善**

SWEBOK が提示する改善策——legibility, structured code, reducing code complexity, accurate code comments——はすべて**発話の明晰さ**の回復を目指すものである。

---

## 5. リバースエンジニアリングは「発話からの意図の復元」である

### SWEBOK の記述

> "Reverse engineering is the process of analyzing software to identify its components and their interrelationships, as well as creating representations of the software in another form or at higher levels of abstraction." (§4.3)

### 言語行為としての意義

リバースエンジニアリングは、**発話（コード）から発話者の意図を復元する**行為——言語行為理論における**発語内行為 (illocutionary act) の再構成**——である:

- Re-documentation = 発話に失われた文脈情報を補完する
- Design recovery = 発話の背後にある設計意図を復元する
- Data reverse engineering = データ構造から意味論を復元する

これは、保守者が**考古学者**のように過去の発話を発掘し解読する営みであり、発話が記録（コード）として残ることの価値と、文脈（ドキュメント、開発者の知識）が失われることのリスクを同時に示している。

---

## 6. 継続的統合・デプロイは「対話の速度の制度化」である

### SWEBOK の記述

> "CI is a software engineering practice that continually merges artifacts, including source code updates from all members of a team, into a shared mainline for evolving and testing the developed system." (§4.4)

> "The biggest risk to any software effort is that you end up building something that isn't useful. The earlier and more frequently you get working software in front of real users, the quicker you get feedback." (§4.4, Martin Fowler)

### 言語行為としての意義

CI/CD は、保守における**対話の速度を制度的に最大化する**仕組みである:

- CI = 複数の行為者の発話を継続的に統合する——**共同執筆のリアルタイム同期**
- Continuous delivery = 発話の受け手（利用者）に素早く届ける
- Continuous testing = 発話の正しさを継続的に検証する
- Fowler の言葉は「発話を聴き手に早く届け、フィードバックを得よ」という対話の基本原則

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| 限られた理解 | 他者の発話の解釈問題 | 接地先の「発話」をどう理解するか |
| Lehman の進化法則 | 発話の生態学 | 接地先の変化にどう追従するか |
| 保守カテゴリ | 改訂動機の類型学 | 接地先起因の保守カテゴリはあるか |
| 技術的負債 | 発話の質の劣化の蓄積 | 接地先との対話における「負債」とは何か |
| リバースエンジニアリング | 発話からの意図の復元 | 接地先の意図をコードから復元できるか |
| CI/CD | 対話の速度の制度化 | 接地先を含む継続的対話は可能か |
