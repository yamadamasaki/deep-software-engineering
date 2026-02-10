# Chapter 03: Software Design — 言語行為としての読解

> SWEBOK v4 Chapter 3 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 設計とは「語彙の創造」による問題と解の表現である

この章が言語行為理論の観点で最も重要なのは、設計思考 (Design Thinking) の核心を**語彙の創造**として明示的に位置づけている点である。Ross, Goodenough & Irvine の5ステップは、設計が本質的に言語的営みであることを示している。設計とは、問題を語る言葉と、解を語る言葉を、同時に発明する行為である。

---

## 1. 設計思考の5ステップは言語創造の過程である

### SWEBOK の記述

> "This process consists of five basic steps: (1) crystallize a purpose or objective; (2) formulate a concept for how the purpose can be achieved; (3) devise a mechanism that implements the conceptual structure; (4) **introduce a notation** for expressing the capabilities of the mechanism and invoking its use; (5) describe the **usage of the notation** in a specific problem context to invoke the mechanism so the purpose is achieved." (§1.1)

> "This is particularly appropriate because **much of software design consists of creating the necessary vocabulary to express a problem, express its solution and implement that solution**. The steps emphasize the **linguistic nature** of software design problem solving." (§1.1)

### 言語行為としての意義

SWEBOK 自身が「linguistic nature」と明言している。設計の5ステップは:

1. **目的の結晶化** = 問題を語る枠組みの確定
2. **概念の定式化** = 解の言語の基本文法の策定
3. **メカニズムの考案** = 語彙への意味論の付与（言葉が「動く」ようにする）
4. **記法の導入** = 語彙と文法の統語論の確定
5. **記法の使用** = その言語での発話の実行

これは**言語ゲームの創設**に他ならない。設計者は、問題領域と解領域のそれぞれについて新しい言語ゲームを創り、両者を翻訳可能にする。

---

## 2. 設計記述 (SDD) は「伝達の媒体」である

### SWEBOK の記述

> "The SDD is used as **a medium for communicating** software design information and can be thought of as a blueprint or model of the system." (Introduction)

> "A fundamental aspect of software design is **communication about the design** among designers, and to customers, implementers and other stakeholders." (§4)

### 言語行為としての意義

SDD は単なるドキュメントではなく、**行為者間のコミュニケーションの媒体**である。SWEBOK はその対象者 (audience) の多様性を強調する:

- 設計チーム内の working specification（内的対話のためのメモ）
- ステークホルダー向けの final design products（外的対話のための成果物）
- 将来の保守者向けの記録（時間を超えた対話）

アジャイルにおいて設計が「開発者の頭の中」にのみ存在する場合、設計という言語行為は**暗黙的 (implicit)** である——語られはするが書かれない。SWEBOK はこれが他のステークホルダー（テスト担当者、品質保証担当者）の仕事を妨げると指摘する。**言語行為が記録されなければ、対話の範囲は制約される。**

---

## 3. 設計原則は対話の格率 (maxim) である

### SWEBOK の記述

> "A principle is 'a fundamental truth or proposition that serves as the foundation for a system of belief or behavior or for a chain of reasoning.'" (§1.4)

原則として挙げられるのは: 抽象化、関心の分離 (SoC)、モジュール化、カプセル化、インターフェースと実装の分離、結合度、凝集度、均一性、完全性、検証可能性。

### 言語行為としての意義

これらの設計原則は、Grice の**対話の格率 (conversational maxims)** に対応する:

| 設計原則 | 対応する対話の格率 |
|---|---|
| 抽象化 | 関係性の格率: 目的に関連する情報だけを語れ |
| 関心の分離 | 様態の格率: 一度に一つのことを明晰に語れ |
| 完全性 | 量の格率: 必要十分な量を語れ |
| 均一性 | 様態の格率: 一貫した方法で語れ |
| カプセル化 | 量の格率: 必要以上に語るな |
| 結合度・凝集度 | 関係性の格率: 関連するものをまとめ、無関係なものを分離せよ |

設計原則は「どう設計すべきか」のルールであると同時に、「設計について、設計を通じて、どう語るべきか」の対話規範でもある。

---

## 4. 設計パターンは「解の定型表現」であり語彙を成す

### SWEBOK の記述

> "A pattern is 'a common solution to a common problem in a given context.'" (§4.4)

> "Design patterns can be used to reflect idioms that have proven useful in solving particular design problems in the past, **establish a solution vocabulary**, and **document and explain design decisions**." (§4.4)

### 言語行為としての意義

SWEBOK は明示的にパターンを「solution vocabulary（解の語彙）」と呼ぶ。パターン名（Observer、Factory、Strategy...）は、設計者間の対話を効率化する**共有の辞書項目**である:

- 「Observer パターンを使う」という一言が、複雑な設計構造を一気に伝達する
- パターンは ch02 でも指摘した「慣用句 (idiom)」の設計版
- GoF の23パターンは、オブジェクト指向設計という言語ゲームの**基本語彙集**

---

## 5. ドメイン特化言語 (DSL) は接地先の言葉を計算機に持ち込む試み

### SWEBOK の記述

> "Part of the design process is **codifying concepts and constructs of a specific application domain to create a computer language** for that domain so that representing the design using these constructs leads to an animated or executable implementation." (§4.5)

> "DSLs blur the lines among modeling languages, design languages and programming languages." (§4.5)

### 言語行為としての意義

DSL は、深ソフトウェア工学にとって最も示唆的な概念の一つである:

- DSL は**接地先の語彙を直接計算機の言語に取り込む**試み
- 「翻訳」のステップを省略し、ドメインの言葉でそのまま実装を記述する
- これは、接地先が計算機と「直接対話」する可能性の萌芽である

Domain-Driven Design (§5.10) も「a domain-specific language **shared with** analysts and other stakeholders」を使うと述べる。ここでの鍵は **shared**——言語が行為者間で**共有**されること——である。

---

## 6. 設計根拠 (Design Rationale) は「なぜそう語ったか」の記録

### SWEBOK の記述

> "Design rationale captures **why** a design decision was made. This includes prior assumptions made, alternatives considered, and trade-offs and criteria analyzed to select one approach and reject others." (§4.6)

> "It can also be useful to capture **rejected decisions** and the reasons for rejection." (§4.6)

### 言語行為としての意義

ch02 で指摘したのと同様、設計根拠は**メタ言語的記録**である:

- なされた発話（決定）の理由の記録
- なされなかった発話（却下された代替案）の記録
- 将来の行為者（保守者）に向けた**時間を超えた対話**

FOSS プロジェクトにおいて設計根拠が特に重要なのは、「large, distributed teams with frequent turnover」——対話の参加者が絶えず入れ替わる状況——だからである。

---

## 7. 倫理的設計 (Ethically Aligned Design): 対話の聴衆の拡大

### SWEBOK の記述

> "Approaches to Ethically Aligned Design have been developed to address concerns including **universal human values, political self-determination, and data agency** and technical dependability." (§1.4)

> 原則: human rights, well-being, data agency, effectiveness, transparency, accountability, awareness of misuse, competence

### 言語行為としての意義

倫理的設計は、設計という言語行為の**聴衆 (audience) を社会全体に拡大する**ものである:

- 従来の設計は client, user, developer が聴衆
- 倫理的設計は「社会への影響を受ける人々すべて」を聴衆に含める
- transparency（透明性）と accountability（説明責任）は、**発話者に対する誠実性要求の拡張**

深ソフトウェア工学の視座から見れば、これは接地先を対話に含める動きの一形態とも読める。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| Design Thinking の5ステップ | 言語ゲームの創設過程 | 接地先を含む言語ゲームをどう創るか |
| SDD | 行為者間コミュニケーションの媒体 | 接地先に届く設計記述とは何か |
| 設計原則 | 対話の格率 (maxim) | 接地先との対話の格率は何か |
| 設計パターン | 解の定型表現・共有語彙 | 接地先を含むパターンは存在するか |
| DSL | 接地先の語彙の計算機への持込み | DSL は接地先の「声」の代弁となるか |
| Design Rationale | メタ言語的記録 | 接地先に向けた根拠説明は必要か |
| Ethically Aligned Design | 聴衆の社会への拡大 | 接地先は倫理的対話の当事者か |
