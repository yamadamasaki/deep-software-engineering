# Chapter 02: Software Architecture — 言語行為としての読解

> SWEBOK v4 Chapter 2 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: アーキテクチャは行為者間の「共有言語の制定」である

ソフトウェア・アーキテクチャとは、本質的に**多様な行為者（ステークホルダー）が一つのシステムについて語り合うための言語を制定し、維持する営み**である。SWEBOK はこの章を通じて、アーキテクチャが単なる技術的構造の記述ではなく、コミュニケーション行為の基盤であることを繰り返し示している。

---

## 1. アーキテクチャ記述 (Architecture Description) は遂行的発話である

### SWEBOK の記述

> "A principal use of a software system's architecture is to give those working with it a **shared understanding** of the system to guide its design and construction." (§1.3)

> "ADs document an architecture for a software system. It is targeted to those **stakeholders** of the system who have concerns about the software system which are answered by the architecture." (§2)

### 言語行為としての意義

アーキテクチャ記述 (AD) は、確認的発話 (constative) ——すなわち事実を述べる行為——ではない。それは**遂行的発話 (performative)**である。AD を書くという行為は:

- **宣言 (declaration)**: 「このシステムはこのように構成される」——現実をつくる発話
- **約束 (commissive)**: 「この構造に従って構築する」——設計者・開発者の義務を生む
- **指示 (directive)**: 「このインターフェースに従え」——後続の行為者への命令

AD は「システムの現状を記述する」以上に、**システムのあるべき姿を現実化する言語行為**である。設計文書は参照されるだけでなく、それに従って行為が遂行される。

---

## 2. ビューポイント (Viewpoint) は言語ゲームの規則体系である

### SWEBOK の記述

> "Each viewpoint provides a **vocabulary or language** for talking about a set of concerns and the mechanisms for addressing them. The viewpoint language gives stakeholders a **shared means of expression**." (§2.1)

> "Viewpoints guide the **creation, interpretation and uses** of architecture views." (§2.1)

### 言語行為としての意義

SWEBOK は明示的にビューポイントを「言語」と呼んでいる。これはウィトゲンシュタインの**言語ゲーム (Sprachspiel)** の概念と直接対応する:

- 各ビューポイントは、特定の関心事について語るための**語彙・文法・ルール**を定める
- 論理ビューポイント、デプロイメントビューポイントなど、それぞれが異なる「言語ゲーム」を構成する
- 同じシステムについて語っていても、異なるビューポイントでは異なる「事実」が見える

ここで重要なのは、ビューポイントは**行為者ごとに異なる**ということである。ユーザ、設計者、運用者——それぞれが自分の言語ゲームを持ち、自分の関心事について語る。**「接地先」が対話から排除されているのは、接地先のためのビューポイント（言語ゲーム）が用意されていないから**、とも読める。

---

## 3. ステークホルダーと関心事: 「誰が語るか」の問題

### SWEBOK の記述

> "A software system has many **stakeholders** with varying roles and interests relative to that system. These varying interests are termed **concerns**." (§1.2)

> "What is fundamental about a system varies according to **stakeholders' concerns and roles**." (§1.2)

### 言語行為としての意義

言語行為理論において、発話の意味は「何を言ったか」だけでなく「**誰が言ったか**」「**どのような立場で言ったか**」によって決まる（適切性条件: felicity conditions）。

SWEBOK はステークホルダーとして「customer」「users」「designers and programmers」「those responsible for safety」を列挙するが、ここに**システムの接地先（grounding target）——すなわちソフトウェアが作用する現実の領域そのもの——は含まれていない**。

深ソフトウェア工学の視点から見れば、これは重大な欠落である。接地先は「語られる対象」としてのみ存在し、**「語る主体」としての地位を与えられていない**。

---

## 4. Conway の法則: 組織の対話構造がアーキテクチャを決める

### SWEBOK の記述

> "Conway's Law posits that 'organizations which design systems … are constrained to produce designs which are **copies of the communication structures** of these organizations.'" (§1.3)

### 言語行為としての意義

これはソフトウェア工学において最も直接的に「言語行為→構造」の関係を示す法則である。

- アーキテクチャは、組織内の**対話パターンの物質化**である
- システムの境界は、**発話が届く範囲の境界**と一致する
- モジュール分割は、**誰が誰と話すか（話さないか）**の反映である

逆に言えば、**新しい行為者（接地先、言語モデル）が対話に参加することは、必然的にアーキテクチャの変容を要求する**。これは Conway の法則の帰結として理論的に導かれる。

---

## 5. アーキテクチャ上の決定 (Significant Decisions) は約束的言語行為である

### SWEBOK の記述

> "Architects make many decisions that **profoundly affect** the architecture, the downstream development process and the software system." (§2.4)

> "Architecture rationale captures **why** an architectural decision was made. This includes assumptions made before the decision, alternatives considered, and trade-offs or criteria used to select an approach and reject others." (§2.4)

### 言語行為としての意義

アーキテクチャ上の決定は、典型的な**約束的言語行為 (commissive speech act)** である:

- 決定は「こうする」という**宣言**であり、それに伴う**義務**を生む
- 決定の記録（rationale）は、**なぜその発話がなされたか**のメタ言語的記述
- 技術的負債 (architectural technical debt) とは、**約束の先送り**——言うべきことを言わなかった、あるいは言ったが履行しなかったことの蓄積

SWEBOK は「Recording rejected decisions and the reasons for their rejection can also be useful」と述べるが、これは**言われなかった発話の記録**——沈黙の構造化——でもある。

---

## 6. パターンとスタイル: 言語行為の定型表現 (idiom)

### SWEBOK の記述

> "A unifying notion is that both patterns and styles are **idioms** in those languages for expressing particular aspects of architectures." (§2.2)

> "An architectural pattern or style uses a vocabulary, drawn from the viewpoint's language, in a specified way." (§2.2)

### 言語行為としての意義

SWEBOK 自身が「idiom（慣用句）」という語を使っている。これは言語行為理論的に極めて正確な表現である:

- パターンは**言い回しの定型化**——繰り返し成功した発話行為の結晶
- MVC、パイプ＆フィルタ、マイクロサービスなどは、それぞれが**特定の対話構造の型**
- パターンカタログは**成語辞典**に相当する

パターンの共有は、行為者間で**共通の語彙と文法を持つ**ことを意味し、コミュニケーションコストを劇的に下げる。

---

## 7. ADL (Architecture Description Language): 形式言語による発話の厳密化

### SWEBOK の記述

> "An architecture description language (ADL) is a **domain-specific language** for expressing software architectures." (§2.3)

> "ADLs arose from **module interconnection languages** for programming in the large." (§2.3)

### 言語行為としての意義

ADL は、アーキテクチャに関する言語行為を**形式化**する試みである。自然言語による曖昧な発話を、機械検証可能な形式言語に置き換える。

これは言語行為理論の観点からは二面的である:

- **利点**: 発話の意味が一意に定まり、誤解が排除される。「model-based architecting」では各ビューがビューポイントに対して機械的に検証可能になる
- **損失**: 形式化できない関心事（美しさ、理解しやすさ、組織的文脈）が表現から排除される。SWEBOK 自身が Vitruvius の venustas（美）を引用しているにもかかわらず、それを形式化する ADL は存在しない

---

## 8. アーキテクチャ評価: 構造化された対話としてのレビュー

### SWEBOK の記述

> "Parnas and Weiss proposed an effective approach to conducting reviews, called **active reviews**, where instead of checklists, each evaluation item entails a **specific activity by a reviewer** to obtain the needed information." (§4.3)

> 「アーキテクチャは堅固か (robust)、用途に適しているか (fit for use)、構築可能か (feasible)、理解可能か (clear and understandable)」(§4.1)

### 言語行為としての意義

アーキテクチャ評価は、**対話の質を問う対話**——メタ対話——である。ATAM、SAAM、QAW などの評価手法は:

- **質問の体系化**: ステークホルダーの関心事に対して、アーキテクチャが「答えている」かを検証する
- **能動的レビュー**: 受動的なチェックリストではなく、レビュアが**自ら発話し、応答を引き出す**
- シナリオベースの評価は、**仮想的な対話の遂行**——「もしこうなったら、システムはどう応答するか」

---

## 9. 多重ビュー問題: 言語間の不整合

### SWEBOK の記述

> "A consequence of introducing multiple views into an AD is a potential mismatch between the views. Are they consistent? Are they describing the same system? This has been called the **multiple views problem**." (§2.1)

### 言語行為としての意義

これは、**異なる言語ゲームの間での一貫性問題**に他ならない。

- 異なるビューポイントから同じシステムについて語るとき、それぞれの「言語」が異なるため、矛盾が生じうる
- 統合的アプローチ (projective approach) は「一つの言語から派生させる」、合成的アプローチ (synthetic approach) は「複数の言語間の翻訳規則を定める」
- これは深ソフトウェア工学における**行為者間の翻訳コスト**の問題と直結する

言語モデルは、この多重ビュー問題——異なる言語ゲーム間の翻訳——において道具となりうる。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| Architecture Description | 遂行的発話（宣言・約束・指示） | 接地先は AD に「声」を持てるか |
| Viewpoint | 言語ゲームの規則体系 | 接地先のためのビューポイントは何か |
| Stakeholder | 対話の参加者 | 接地先を参加者として含められるか |
| Conway's Law | 対話構造の物質化 | 新たな行為者の参加はアーキテクチャをどう変えるか |
| Significant Decision | 約束的言語行為 | 接地先との「約束」は可能か |
| Pattern/Style | 言語行為の慣用句 | 接地先を含む新たなパターンは何か |
| ADL | 形式化された言語行為 | 接地先の「声」を形式化できるか |
| Architecture Evaluation | メタ対話 | 接地先はレビューに参加できるか |
| Multiple Views Problem | 言語ゲーム間の翻訳問題 | 言語モデルは翻訳者となるか |
