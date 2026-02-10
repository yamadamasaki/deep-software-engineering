# Chapter 08: Software Configuration Management — 言語行為としての読解

> SWEBOK v4 Chapter 8 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 構成管理とは「発話の版と履歴の管理」である

ソフトウェア構成管理 (SCM) は、ソフトウェアという発話の**同一性、版、変更履歴を管理する**制度的仕組みである。発話が一回限りの行為ではなく、継続的に改訂される生きたテクストであるとき、「どの版がいつ誰によって変更されたか」「現在の正典はどれか」を追跡する仕組みが不可欠となる。SCM は、対話の**記録と統制**の制度化である。

---

## 1. 構成項目 (CI) は「管理対象となる発話単位」の同定である

### SWEBOK の記述

> "A CI is an item or aggregation of hardware, software or both, designed to be managed as a single entity." (§2.1.2)

> "Software items with potential to become SCIs include plans, specifications and design documentation, testing materials, software tools, source and executable code, code libraries, data and data dictionaries, and documentation." (§2.1.2)

### 言語行為としての意義

構成項目の同定は、**どの発話を管理対象とするか**の決定である:

- 計画書、仕様書、設計文書、テスト資材、コード、ドキュメント——すべて「発話の記録」
- CI の選定は「管理すべき発話の粒度」の決定——細かすぎれば管理不能、粗すぎれば制御不能
- CI の一意識別子 = 発話への**名前の付与**——言及可能性 (referability) の確保

---

## 2. ベースラインは「合意された正典」の確立である

### SWEBOK の記述

> "A software baseline is a formally approved version of a CI (regardless of media type) that is formally designated and fixed at a specific time during the CI's life cycle." (§2.3)

> "The baseline can be changed only through formal change control procedures." (§2.3)

### 言語行為としての意義

ベースラインは、ある時点で**正式に合意された発話の正典**の確立である:

- ベースラインの確立 = **宣言的言語行為 (declarative)**: 「この版を公式とする」
- 変更には正式な手続きが必要 = **制度的統制** (institutional control)
- 複数のベースライン（開発、テスト、本番）= 対話の段階ごとの正典

これは、聖典のカノン化 (canonization) に類似する——何を権威ある版とするかの社会的合意の制度化。

---

## 3. 変更要求 (CR) プロセスは「改訂提案の審議プロトコル」である

### SWEBOK の記述

> "The software change request (SCR) process provides formal procedures for submitting and recording CRs; evaluating the potential cost and impact of a proposed change; and accepting, modifying, deferring or rejecting the proposed change." (§3.1)

> "The authority for accepting or rejecting proposed changes rests with an entity known as a configuration control board (CCB)." (§3.1.1)

### 言語行為としての意義

変更要求プロセスは、発話の**改訂提案を審議する形式的な対話プロトコル**である:

- **CR の提出** = 改訂の提案（「こう言い直すべきだ」という主張）
- **影響分析** = 改訂が他の発話に及ぼす効果の評価
- **CCB の審議** = 改訂の可否を決定する権威ある機関——**言語行為の統制機関**
- **承認/却下/延期** = 制度的な意思決定

CCB は、「誰が発話を変更する権限を持つか」という**発話の権威 (authority)** の制度化であり、無秩序な変更（矛盾する発話の乱立）を防ぐ。

---

## 4. CI 間の関係定義は「発話間の相互参照構造」の明示化である

### SWEBOK の記述

> "Relationships provide the connections required to create and sustain structure." (§2.5)

> "Dependencies: CI-1 and CI-2 depend mutually on each other." / "Derivation: One CI derives from another." / "Succession: Software items evolve as a software project proceeds." (§2.5)

### 言語行為としての意義

CI 間の関係スキーマは、発話間の**相互参照と依存関係の構造**を明示化する:

- **依存関係 (dependency)**: ある発話の意味が別の発話に依存する
- **導出関係 (derivation)**: ある発話が別の発話から派生した
- **継承関係 (succession)**: 発話の時間的な版の連鎖

**SBOM (Software Bill of Materials)** は、発話を構成する全要素（ライブラリ、モジュール等）の**目録**——「この発話は何から成り立っているか」の記録である。これは対話の透明性と追跡可能性を保証する仕組みであり、セキュリティの観点からも重要性が増している。

---

## 5. 構成監査は「発話の整合性の検証」である

### SWEBOK の記述

> "A software audit is an independent examination of a work product or set of work products to assess technical, security, legal and regulatory compliance with specifications, standards, contractual agreements or other criteria." (§5)

> "The software FCA ensures that the audited software item is consistent with its governing specifications." / "The software PCA ensures that the design and reference documentation are consistent with the as-built software product." (§5.1, §5.2)

### 言語行為としての意義

構成監査は、**発話の整合性を第三者が検証する**メタ対話的活動である:

- **機能構成監査 (FCA)**: 発話の内容が仕様（意図の記録）と一致するか——**意味的整合性**の検証
- **物理構成監査 (PCA)**: 設計文書と実際の成果物が一致するか——**形式的整合性**の検証
- 監査の独立性 = 発話の当事者以外による検証——**客観的な解釈の確認**

---

## 6. リリース管理は「発話の公式な公開」の統制である

### SWEBOK の記述

> "Release refers to distributing software and related artifacts outside the development activity." (§6)

> "The information documenting the physical contents of a release is known as a version description document (VDD)." (§6.2)

### 言語行為としての意義

リリース管理は、発話の**公式な公開 (publication)** を統制する活動である:

- リリース = 内部の草稿から外部への**公式発行**への移行
- VDD = 「この版に何が含まれるか」の目録——出版物の**奥付**に相当
- リリースノート = 「何が変わったか、何が既知の問題か」の説明——読者（利用者）への案内
- デジタル署名 = 発話の**真正性 (authenticity)** の保証——「この発話は確かにこの発話者から来た」

継続的デリバリーは、この公式発行のプロセスを自動化し、高頻度化する——**出版の民主化と加速化**。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| 構成項目 (CI) | 管理対象となる発話単位 | 接地先の成果物も CI として管理すべきか |
| ベースライン | 合意された正典の確立 | 接地先を含むベースラインは定義できるか |
| 変更要求プロセス | 改訂提案の審議プロトコル | 接地先からの変更要求はどう処理するか |
| CI 間の関係 | 発話間の相互参照構造 | 接地先の成果物との関係はどう追跡するか |
| 構成監査 | 発話の整合性の検証 | 接地先を含む整合性はどう監査するか |
| リリース管理 | 発話の公式な公開の統制 | 接地先に影響するリリースはどう統制するか |
