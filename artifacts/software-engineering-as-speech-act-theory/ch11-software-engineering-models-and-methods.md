# Chapter 11: Software Engineering Models and Methods — 言語行為としての読解

> SWEBOK v4 Chapter 11 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: モデルとは「ソフトウェアについての構造化された発話」である

ソフトウェア工学のモデルとメソッドは、ソフトウェアを**体系的に表現し、分析し、構築する**ための枠組みを提供する。モデリングは本質的に**ソフトウェアについて語る行為**——ソフトウェアの特定の側面を、定められた言語で、特定の聴衆に向けて表現する言語行為——である。

---

## 1. モデリング原則は「対話の基本規範」である

### SWEBOK の記述

> 三つの原則: "Model the essentials," "Provide perspective," "Enable effective communications." (§1.1)

### 言語行為としての意義

モデリングの三原則は、Grice の対話の格率に直接対応する:

- **Model the essentials** = **関係性の格率**: 目的に関連する情報のみを語れ——抽象化は不要な情報を除去する
- **Provide perspective** = **様態の格率**: 明確な視点から語れ——構造的、振る舞い的、時間的などの視点の使い分け
- **Enable effective communications** = **対話の根本目的**: モデリングの目的はステークホルダーとの効果的なコミュニケーションである

SWEBOK が「application domain vocabulary」と「modeling language」と「semantic expression」を列挙していることは、モデリングが**複数の語彙体系を意識的に使い分ける多言語的行為**であることを示す。

---

## 2. 構文・意味論・語用論はモデリング言語の三層構造である

### SWEBOK の記述

> "Syntactic and semantic rules define modeling languages." (§1.3)

> "Pragmatics explains how meaning is embodied in the model and its context and how it is communicated effectively to other software engineers." (§1.3)

### 言語行為としての意義

SWEBOK はモデリング言語を**構文 (syntax)・意味論 (semantics)・語用論 (pragmatics)** の三層で明示的に記述しており、これは言語学の基本構造そのものである:

- **構文**: BNF やメタモデルで定義される——「正しい文の形式」
- **意味論**: 構文要素に付与される意味——「文が何を指すか」
- **語用論**: 文脈の中でどう意味が伝達されるか——「モデルが特定の状況で何を伝えるか」

「imported modeling syntax might be the same, it might mean something quite different in the new environment」という警告は、同じ言葉でも**文脈が異なれば意味が異なる**という語用論の基本的教訓である。

---

## 3. 事前条件・事後条件・不変条件は「発話の約束の形式化」である

### SWEBOK の記述

> "Preconditions are conditions that must be satisfied before execution..." / "Postconditions are conditions guaranteed to be true after..." / "Invariants are conditions within the operational environment that persist..." (§1.4)

### 言語行為としての意義

これは ch04 の Design by Contract と同じ構造であり、モデリングのレベルで**言語行為の適切性条件を形式化する**手法である:

- 事前条件 = 発話の**準備条件** (preparatory condition)
- 事後条件 = 発話の**約束** (promise)
- 不変条件 = 対話の**前提** (background assumption)

---

## 4. モデルの分析は「発話の品質検証」の体系化である

### SWEBOK の記述

> 分析項目: completeness, consistency, correctness, traceability, interaction (§3)

### 言語行為としての意義

モデルの分析は、ソフトウェアについての発話（モデル）が**十分で、矛盾なく、正しく、追跡可能で、整合的か**を検証する体系的な活動である:

- **完全性 (completeness)**: 必要なことがすべて語られているか——量の格率
- **一貫性 (consistency)**: 矛盾なく語られているか——質の格率
- **正確性 (correctness)**: 正しく語られているか——質の格率
- **追跡可能性 (traceability)**: 発話間の関係が辿れるか——発話の相互参照構造の維持
- **相互作用分析 (interaction)**: 発話の各部分が適切に連携するか——対話の整合性

---

## 5. 形式手法は「数学的に厳密な発話」を志向する

### SWEBOK の記述

> "Formal methods are software engineering methods that apply rigorous, mathematically based notation and language to specify, develop and verify the software." (§4.2)

### 言語行為としての意義

形式手法は、ソフトウェアについての発話を**数学的に厳密な言語**で行うことで、曖昧さを排除しようとする試みである:

- 仕様記述言語 = 曖昧さのない発話形式——自然言語の多義性を排除
- プログラム洗練 (refinement) = 高水準の発話を段階的に詳細な発話に変換する
- 形式検証 = 発話の正しさを数学的に証明する——Oracle 問題への一つの回答
- 軽量形式手法 (Alloy など) = 実用性と厳密性のバランス——「完全な証明」ではなく「有限の検査」

---

## 6. アジャイルメソッドは「対話中心のメソッド」である

### SWEBOK の記述

> "Agile methods are considered lightweight because of their short, iterative development cycles, self-organizing teams, simpler designs, code refactoring, test-driven development, frequent customer involvement and emphasis on creating a demonstrable working product." (§4.4)

### 言語行為としての意義

アジャイルメソッドは、**対話を中心に据えた開発方法論**である:

- 短いイテレーション = 対話の頻度の最大化
- 自己組織化チーム = 対話の主体性の確保
- 顧客の頻繁な参加 = 聴き手を対話に常時含める
- 動作するプロダクト = 対話の成果を具体的に示す
- XP のストーリー = 利用者の言葉（語彙）で要求を表現する
- ペアプログラミング = 二人の行為者による**同時的対話的コーディング**

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| モデリング原則 | 対話の基本規範 | 接地先を含むモデリングの規範は何か |
| 構文・意味論・語用論 | モデリング言語の三層構造 | 接地先の語彙はモデルにどう取り込まれるか |
| 事前/事後条件・不変条件 | 発話の約束の形式化 | 接地先との約束はどう形式化するか |
| モデル分析 | 発話の品質検証 | 接地先を含むモデルの品質はどう検証するか |
| 形式手法 | 数学的に厳密な発話 | 接地先の記述に形式手法は適用できるか |
| アジャイルメソッド | 対話中心のメソッド | 接地先を含むアジャイル開発は可能か |
