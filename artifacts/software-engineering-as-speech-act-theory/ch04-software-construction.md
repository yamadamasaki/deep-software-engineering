# Chapter 04: Software Construction — 言語行為としての読解

> SWEBOK v4 Chapter 4 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 構築とは「人間が計算機に対して行う発話行為」の実行である

ソフトウェア構築は、設計や要求で練り上げられた意図を、最終的に計算機が実行できる形式で発話する段階である。SWEBOK は構築言語を「a human can specify an executable solution to a problem」ためのあらゆる形式と定義しており、これは文字通り**人間から計算機への言語行為**の定義である。

---

## 1. 構築言語は人間から計算機への発話形式の分類体系である

### SWEBOK の記述

> "Construction languages include **all forms of communication by which a human can specify an executable solution** to a problem." (§3.2)

三つの記法分類: linguistic（テキスト的）、formal（形式的）、visual（視覚的）。さらに構築言語の階層: 設定言語 → ツールキット言語 → スクリプト言語 → プログラミング言語。

### 言語行為としての意義

これは**人間→計算機の発話形式の分類体系**である:

- **設定言語**: 選択肢からの選択——最も制約された発話形式（「はい/いいえ」の応答に近い）
- **プログラミング言語**: 最も自由度の高い発話形式——しかし「application area についての情報を最も少なく含む」
- **DSL**: 特定領域の語彙と文法を持つ発話形式——接地先の言葉に最も近い

linguistic 記法について「each string should have a **strong semantic connotation** providing an **immediate intuitive understanding**」と述べられている。良いコードとは、人間にとって「意味が直観的にわかる」発話である。

---

## 2. 「複雑さの最小化」は発話の明晰さの要請である

### SWEBOK の記述

> "All people have **limited ability to hold complex structures and information** in their working memories." (§1.1)

> "Reduced complexity is achieved by creating **simple and readable code** rather than clever code." (§1.1)

### 言語行為としての意義

構築の第一原則「複雑さの最小化」は、Grice の**様態の格率 (maxim of manner)**——「明晰に語れ、曖昧を避けよ」——のコード版である。

- コードは二重の聴衆を持つ: **計算機**（正確に実行するため）と**人間**（理解し保守するため）
- 「clever code よりも readable code」は、**発話の目的が伝達にある**ことの宣言
- コーディング規約（命名規則、インデント、構造化）は**対話の礼儀作法**

---

## 3. Design by Contract は文字通りの契約的言語行為である

### SWEBOK の記述

> "Design by contract is a development approach in which **preconditions and postconditions** are included for each routine. When preconditions and postconditions are used, each routine or class is said to **form a contract** with the rest of the program." (§4.4)

### 言語行為としての意義

Design by Contract (DbC) は、言語行為理論の**約束 (commissive)** を形式化した構築技法である:

- **事前条件**: 「こう呼ばれたら」——発話の前提条件 (preparatory condition)
- **事後条件**: 「こう応答する」——約束 (promise)
- **不変条件**: 「常にこれは成り立つ」——宣言 (declaration)

DbC は、モジュール間の相互作用を**明示的な約束の交換**として形式化する。これは、暗黙の了解ではなく明文化された契約に基づくコミュニケーション——まさに言語行為の制度化である。

---

## 4. API は行為者間の「会話のプロトコル」である

### SWEBOK の記述

> "An API is a set of signatures that are exported and available to the users of a library or a framework. Besides signatures, an API should always include statements about the program's **effects and/or behaviors** (i.e., its semantics)." (§4.1)

> "The API-first approach [...] is usually accomplished by using an API description language to establish **a contract** for how the API is supposed to behave." (§4.1)

### 言語行為としての意義

API は**行為者（コンポーネント）間の対話プロトコル**である:

- シグネチャ = 語彙（何を言えるか）
- セマンティクス = 語用論（言ったらどうなるか）
- API-first approach = **対話のルールを先に決めてから実装する**

OpenAPI のような標準は、**行為者間の共通語 (lingua franca)** の制定に相当する。

---

## 5. LLM によるコード生成: 新たな行為者の参入

### SWEBOK の記述

> "Modern IDEs are often equipped with **AI-assisted programming** which is boosted by the recent advances in **Large Language Models (LLMs)**. [...] A programmer can define a function in pseudocode comments or outline its implementation as a prompt for an LLM to generate or complete the code." (§5.1)

### 言語行為としての意義

SWEBOK v4 は LLM によるコード生成を公式に認めている。これは深ソフトウェア工学にとって極めて重要:

- 従来: 人間→計算機の一方向的発話（コーディング）
- LLM 時代: **人間↔LLM↔計算機の三者間対話**
- プロンプトは「意図の言語化」、生成コードは「LLM による翻訳」、レビューは「人間による検証」

ただし SWEBOK は「programmer still reviews the generated code」と明記しており、**人間が最終的な発話の責任者**であるという前提を維持している。

---

## 6. フィードバックループ: 構築は対話的過程である

### SWEBOK の記述

> "Early and continuous feedback for the construction activity is one of the most important advantages of agile development and DevOps." (§4.17)

### 言語行為としての意義

構築を一方向的な「命令発出」ではなく、**継続的な対話的過程**として捉える動き:

- アジャイル: 頻繁なイテレーションによる「構築→フィードバック→修正」の対話ループ
- DevOps: 運用環境からのフィードバック——**計算機（実行環境）からの応答を聴く**
- CI/CD: 統合とデプロイの自動化——**対話の速度の最大化**

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| 構築言語 | 人間→計算機の発話形式 | 接地先→計算機の発話形式はありうるか |
| 複雑さの最小化 | 発話の明晰さの要請 | 接地先にとっての「明晰さ」とは何か |
| Design by Contract | 約束的言語行為の形式化 | 接地先との「契約」は可能か |
| API | 行為者間の対話プロトコル | 接地先が参加する API とは何か |
| LLM コード生成 | 三者間対話の出現 | LLM は接地先の「翻訳者」となるか |
| フィードバックループ | 構築の対話的過程化 | 接地先からのフィードバックは得られるか |
| DSL | 接地先の語彙の計算機への持込み | DSL は接地先自身の言語となるか |
