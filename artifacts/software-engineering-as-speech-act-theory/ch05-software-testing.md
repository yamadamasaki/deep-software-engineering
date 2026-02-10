# Chapter 05: Software Testing — 言語行為としての読解

> SWEBOK v4 Chapter 5 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: テストとは「発話の検証」——意図と実行の照合行為である

ソフトウェアテストは、構築段階で計算機に向けて発せられた発話（コード）が、意図された意味（要求仕様）を正しく実現しているかを検証する行為である。テストは本質的に**メタ言語的活動**——発話についての発話——であり、「言ったことが伝わったか」を確認する対話的営みである。

---

## 1. テストの基本定義は「発話の受理確認」である

### SWEBOK の記述

> "Software testing consists of the dynamic validation that a system under test (SUT) provides expected behaviors on a finite set of test cases suitably selected from the usually infinite execution domain." (Introduction)

### 言語行為としての意義

テストとは、人間が計算機に向けて発した発話（プログラム）に対し、計算機が**意図通りに応答しているか**を確認する行為である:

- **Expected behaviors**: 発話者の意図 (illocutionary force) が正しく伝達されたか
- **Dynamic validation**: 実際に計算機に「発話を実行させる」ことによる検証
- **Finite test cases**: 無限の発話可能性から有限の確認点を選ぶ——言語行為の**サンプリング検証**

---

## 2. Oracle 問題は「聴き手の理解の正しさをどう判定するか」の問題である

### SWEBOK の記述

> "An oracle can be any human or mechanical agent that decides whether the SUT behaved correctly in each test and according to the expected outcomes." (§1.2.7)

> "The oracle provides a 'pass' or 'fail' verdict." (§1.2.7)

### 言語行為としての意義

Oracle 問題は、言語行為理論における**了解の判定問題**に相当する:

- Oracle = 発話が正しく了解されたかを判定する第三者（審判）
- 「正しい応答」の基準はどこにあるか？——要求仕様（明示的な意図の記録）、行動モデル（暗黙の期待）、コード注釈（発話者の補足説明）
- Oracle の自動化が困難なのは、**意図の正確な形式化が困難**だからである

Dijkstra の「テストはバグの存在を示せるが、不在を示せない」という格言は、**発話の意図が完全に形式化できない**ことの帰結である。

---

## 3. テストレベルは「対話の粒度」の階層である

### SWEBOK の記述

> "Four test stages can be distinguished: unit, integration, system, and acceptance." (§2.1)

### 言語行為としての意義

テストレベルは、発話の検証を行う**対話の粒度**の階層に対応する:

- **Unit testing**: 個々の語句（関数・モジュール）が正しい意味を持つか
- **Integration testing**: 語句の組合せ（モジュール間の対話）が文法的に正しいか
- **System testing**: 全体としての発話（システム全体）が意図を伝えているか
- **Acceptance testing**: **聴き手（利用者）が発話を受理するか**——最も重要な検証

Acceptance testing は、言語行為理論でいう**発語内効力 (perlocutionary effect)** の検証——発話が聴き手に意図した効果を及ぼしたかの確認——に相当する。

---

## 4. テスト技法の分類は「検証の視点」の分類である

### SWEBOK の記述

> "specification-based techniques, also known as black-box techniques [...] structure-based, also called white-box [...] techniques" (§3)

> "Experience-based techniques [...] depend on different factors, such as human knowledge of the SUT and its context and the tester's experience and intuition." (§3.3)

### 言語行為としての意義

三つのテスト技法カテゴリは、発話の検証における**異なる解釈戦略**に対応する:

- **Specification-based (black-box)**: 発話の**意味**（何を言おうとしたか）から検証——語用論的アプローチ
- **Structure-based (white-box)**: 発話の**構造**（どう言ったか）から検証——統語論的アプローチ
- **Experience-based**: 検証者の**経験と直観**に基づく検証——実践的知識 (phronesis) によるアプローチ

Exploratory testing——「simultaneous learning, test design and test execution」——は、テスターが SUT との**対話を通じて**問題を発見する手法であり、最も明示的に対話的なテスト形式である。

---

## 5. Acceptance Test-Driven Development は「受理条件の先行宣言」である

### SWEBOK の記述

> "Defining acceptance tests before implementing the corresponding functionality is a key activity of the acceptance test-driven development (ATDD)." (§2.1.4)

### 言語行為としての意義

ATDD と TDD は、言語行為の**適切性条件 (felicity conditions) を先に定める**アプローチである:

- TDD: 「この発話が正しいとはどういうことか」を先に定義してからコードを書く
- ATDD: 「この発話が聴き手（利用者）に受理されるとはどういうことか」を先に定義する
- これは、対話の**成功条件を先に合意する**という、きわめて理性的なコミュニケーション戦略

---

## 6. AI/ML テストは「非決定的発話の検証」という新問題を提起する

### SWEBOK の記述

> "Because of their peculiarities (for instance their non-deterministic nature), testing such applications is challenging and might be very expensive." (§7.1)

### 言語行為としての意義

AI/ML システムのテストは、**同じ入力に対して異なる応答をする行為者**の検証という新しい問題を提起する:

- 従来のテスト: 発話（入力）→応答（出力）の対応が決定的
- AI/ML テスト: 発話に対する応答が確率的・文脈依存的
- これは、人間同士の対話に近い状況——同じ質問に対して状況により異なる答えが返る

深ソフトウェア工学にとって、AI/ML テストの問題は**行為者としての計算機の応答の非決定性**をどう扱うかという問いに直結する。

---

## 7. ドメイン固有テストは「接地先の文脈に依存した検証」である

### SWEBOK の記述

> "Usually, an application domain is strictly connected to a certain reality. Therefore, testing approaches could be tailored to the needs of the domain." (§6.2)

> "involving legal domain experts in test case generation is common practice to ensure a focus on desired characteristics and quality." (§6.2)

### 言語行為としての意義

ドメイン固有テスト——医療、航空、金融、法律——は、**接地先の文脈を知る専門家**がテストに参加することの必要性を示している:

- 法律ドメイン: 「specific nomenclature and jargon」——接地先固有の語彙が検証に必要
- 医療ドメイン: HIPAA, GDPR など規制準拠——**社会的文脈**が検証基準を規定
- 自動車ドメイン: 安全性基準——**物理的現実**が検証基準を規定

これは、接地先を対話に含めない限り、適切な検証ができないことの証左である。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| テストの基本定義 | 発話の受理確認 | 接地先による「受理確認」は可能か |
| Oracle 問題 | 了解の正しさの判定問題 | 接地先にとっての「正しい応答」とは何か |
| テストレベル | 対話の粒度の階層 | 接地先はどの粒度で検証に参加するか |
| テスト技法分類 | 検証の解釈戦略 | 接地先に適した検証戦略は何か |
| TDD/ATDD | 適切性条件の先行宣言 | 接地先との適切性条件の合意は可能か |
| AI/ML テスト | 非決定的発話の検証 | 行為者の応答の非決定性をどう扱うか |
| ドメイン固有テスト | 接地先の文脈に依存した検証 | 接地先自身がテストに参加する方法はあるか |
