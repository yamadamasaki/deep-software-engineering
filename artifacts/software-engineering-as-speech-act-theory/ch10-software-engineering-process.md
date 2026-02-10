# Chapter 10: Software Engineering Process — 言語行為としての読解

> SWEBOK v4 Chapter 10 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: プロセスとは「対話の手順の体系化」である

ソフトウェア工学プロセスは、ソフトウェアの構築・運用・保守における作業活動を体系的に定義し、管理するための枠組みである。言語行為の観点からは、プロセスとは**対話の手順を明文化し、再現可能にする**営みであり、ライフサイクルモデルは**対話の全体構造を規定する設計図**である。

---

## 1. プロセス定義は「対話の手順の明文化」である

### SWEBOK の記述

> "A process is a 'set of interrelated or interacting activities that transforms inputs into outputs.'" (§1.2)

> "The specification should be useful to humans so that they can communicate with one another using this specification." (§2.2)

### 言語行為としての意義

プロセス定義は、ソフトウェア開発という対話を**再現可能な手順として明文化する**行為である:

- プロセスの入力・活動・出力 = 対話における「問い→応答→成果」の形式化
- 「useful to humans so that they can communicate」= プロセス記述そのものが**コミュニケーションの媒体**
- プロセスの合意とは、「どのような対話をどのような順序で行うか」の**メタ対話による合意**

---

## 2. ライフサイクルモデルは「対話の全体構造のパラダイム」である

### SWEBOK の記述

> ウォーターフォール、V-モデル、インクリメンタル、スパイラル、アジャイルなど。(§2.4, §2.5)

> "The Agile Manifesto effected a disruption in the software engineering community by creating an abrupt change of mindset." (§2.5)

### 言語行為としての意義

ライフサイクルモデルの選択は、対話の**全体構造をどう設計するか**というパラダイム選択である:

- **ウォーターフォール**: 一方向的・逐次的な対話——「まず全部聴いてから、全部語る」
- **インクリメンタル/反復**: 反復的な対話——「少し聴いて、少し語り、確認してまた聴く」
- **アジャイル**: 継続的で適応的な対話——「常に聴き、常に語り、常に変化を受け入れる」
- **スパイラル**: リスク駆動の対話——「最も不確実なことから先に確認する」

アジャイルマニフェストの核心は、**対話のあり方の根本的転換**——計画的な独白から適応的な対話へ——であった。

---

## 3. アジャイルの本質は「コミュニケーションの優先」である

### SWEBOK の記述

> "Communication and mutual trust between team/customer were essential. Signatories claimed that team communication, often face-to-face, and communication with the customer were key." (§2.5)

> "The Agile mindset is based on a number of values and principles (e.g., the importance of communication, being open to change or commitment to technical excellence and always delivering value to the customer)." (§2.5)

### 言語行為としての意義

アジャイルは、ソフトウェア開発における**コミュニケーション（対話）を最優先する**宣言である:

- face-to-face のコミュニケーション = 最も直接的な対話形式の優先
- 「being open to change」= 対話を通じて意見（要求）が変わることの受容
- 「delivering value to the customer」= 対話の成果が聴き手に価値をもたらすことの要請

これは、ソフトウェア工学が本質的に**対話的営み**であるという深ソフトウェア工学の立場と強く共鳴する。

---

## 4. DevOps は「対話のサイロを打破する原則」である

### SWEBOK の記述

> "DevOps, defined as a 'set of principles and practices which enable better communication and collaboration between relevant stakeholders for the purpose of specifying, developing, and operating software and systems products and services.'" (§2.5)

### 言語行為としての意義

DevOps は ch06 でも論じたが、プロセスの観点からは**対話のサイロを組織的に打破する原則と実践の体系**である:

- 開発・セキュリティ・運用の統合 (Dev/Sec/Ops) = 分断されていた対話チャネルの統合
- 継続的デリバリー = 対話のサイクルの高速化
- Dev/Sec/Ops は「security/quality を最初から対話に含める」という**シフトレフト**——品質に関する対話を後ろから前に移動する

---

## 5. プロセス評価と改善は「対話の質の継続的向上」である

### SWEBOK の記述

> "The idea that any executed process can be improved was present in the classic Shewhart-Deming plan-do-check-act (PDCA) paradigm." (§3.1)

> "The objective of the retrospective is to analyze what went well and what did not go well, to understand why, and to set a number of actions for learning and improvement." (§3.4)

### 言語行為としての意義

プロセス評価と改善は、対話の質を**継続的に向上させる**メタ対話的活動である:

- **PDCA**: 「計画→実行→確認→改善」= 対話の質の改善サイクル
- **GQM (Goal-Question-Metric)**: 目標を設定し、問いを立て、指標で測る——対話の効果の定量的評価
- **レトロスペクティブ**: 「何がうまくいき、何がうまくいかなかったか」の振り返り——対話についての対話
- **CMMI/ISO 33000**: 対話の成熟度を段階的に評価する枠組み

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| プロセス定義 | 対話の手順の明文化 | 接地先を含む対話の手順は定義できるか |
| ライフサイクルモデル | 対話の全体構造のパラダイム | 接地先を含むライフサイクルはどうなるか |
| アジャイル | コミュニケーションの優先 | 接地先との「アジャイルな」対話は可能か |
| DevOps | 対話のサイロの打破 | 接地先を含む DevOps はどうあるべきか |
| プロセス改善 | 対話の質の継続的向上 | 接地先との対話の質はどう改善するか |
