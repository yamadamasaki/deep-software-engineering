# Chapter 09: Software Engineering Management — 言語行為としての読解

> SWEBOK v4 Chapter 9 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 管理とは「対話の組織化と統制」である

ソフトウェア工学管理は、ソフトウェア開発という対話的過程を**計画し、組織し、監視し、制御する**活動である。管理そのものが、ステークホルダー間の要求交渉、チーム内のコミュニケーション、進捗報告など、多層的な**対話の組織化**として遂行される。

---

## 1. ソフトウェアの特異性は「発話の可塑性」に由来する

### SWEBOK の記述

> "Software is intangible because it has no physical properties and is malleable because of the relative ease with which code can be modified." (Introduction)

> "Software is made by people and for people, so digital talent matters." (Introduction)

> "A significant number of software projects failed due to social issues." (Introduction)

### 言語行為としての意義

ソフトウェア管理の固有の難しさは、ソフトウェアが**可塑的 (malleable) な発話**であることに由来する:

- 物理的成果物と異なり、いつでも容易に「言い直せる」——これが強みでもあり弱みでもある
- 「people and for people」= ソフトウェアは本質的に**人間間の対話の媒体**
- プロジェクトの失敗が「social issues」に帰せられる = 対話の失敗がプロジェクトの失敗

管理とは、この可塑的な発話の過程を秩序立てることであり、本質的に**対話の統制**である。

---

## 2. 要求の決定と交渉は「対話の開始と合意形成」である

### SWEBOK の記述

> "Determining and negotiating the project requirements are the overarching goals of the tasks undertaken during this phase." (§1.1)

> "Given the inevitability of change, stakeholders should agree on how requirements and scope will be reviewed and revised." (§1.3)

### 言語行為としての意義

プロジェクトの開始は、ステークホルダー間の**対話の枠組みの合意**である:

- 要求の「決定」は一方的ではなく「交渉 (negotiation)」——**対話的合意形成**
- 変更の不可避性を前提として、レビューと改訂の手続きを先に合意する——**メタ対話のルール設定**
- Project Charter = 「何について、どのように対話するか」の**対話の契約**

「clients often do not know what is needed or what is feasible」は、要求が対話を通じて初めて明確化されること——対話の前には完全な意図は存在しないこと——を示す。

---

## 3. 計画と見積もりは「対話の見通しの形成」である

### SWEBOK の記述

> "The effort required for any given software project depends almost entirely on human elements: individuals' experience and capabilities, team members' interactions, and the culture of the software development environment." (§2.3)

> "Software project managers should use multiple estimation approaches and then reconcile the differences among the estimates." (§2.3)

### 言語行為としての意義

見積もりが困難である根本的理由は、ソフトウェア開発が**対話的過程**であり、その成果が人間の相互作用に依存するからである:

- 見積もりの変数: 個人の経験、チームの相互作用、文化——すべて**対話の質**に関わる要素
- 複数の見積もり手法の併用 = **多角的な視点からの対話**による収束
- adaptive SDLC では見積もりが反復的に更新される = **対話を通じた漸進的な理解の深化**

---

## 4. リスク管理は「対話の不確実性への対処」である

### SWEBOK の記述

> "Risk is effect of uncertainty on objectives that has negative (threats) or positive (opportunities) consequences." (§2.5)

> "Risk management entails identifying risk factors, analyzing probability and potential impact of each risk factor, prioritizing risk factors, and developing risk mitigation strategies." (§2.5)

### 言語行為としての意義

リスク管理は、対話における**不確実性——意図が正しく伝わらない、文脈が予期せず変化する——への体系的対処**である:

- リスクの同定 = 対話が失敗しうる場面の特定
- 影響分析 = 対話の失敗がもたらす帰結の評価
- 緩和戦略 = 対話の失敗を防ぐ、あるいはその影響を最小化する方策
- 「software engineers' tendency to add unneeded features」= **聴き手が求めていないことを語る**傾向——Grice の量の格率に反するリスク

---

## 5. 監視・制御・報告は「対話のメタレベルの管理」である

### SWEBOK の記述

> "Adherence to the scope, project plan and related plans should be assessed continually and at predetermined intervals." (§3.4)

> "Progress to date should be reported at specified and agreed-upon times [...] Reports should focus on the information needs of the target audience." (§3.6)

### 言語行為としての意義

監視・制御・報告は、プロジェクトという対話の**メタレベルの管理活動**である:

- **監視 (monitoring)**: 対話が計画通りに進んでいるかの観察
- **制御 (control)**: 対話の逸脱を修正する介入
- **報告 (reporting)**: 対話の進捗についての「報告的発話 (assertive)」——聴衆（ステークホルダー）に合わせた報告

「Reports should focus on the information needs of the target audience」は、報告という発話が**聴き手 (audience) を意識して構成されるべき**ことの表明である。

---

## 6. クロージャと回顧は「対話の総括と反省」である

### SWEBOK の記述

> "Closure occurs when the specified tasks for a project, a phase or an iteration have been completed and satisfactory achievement of the completion criteria has been confirmed." (§5.1)

> "A project, phase or iteration retrospective analysis should be undertaken so that issues, problems, risks and opportunities encountered can be analyzed. Lessons learned should be drawn from the project and fed into organizational learning." (§5.2)

### 言語行為としての意義

クロージャは、対話の**終結宣言**と**回顧的メタ対話**の二つの行為から成る:

- **クロージャの宣言** = 「この対話は完了した」という宣言的言語行為 (declarative)
- **回顧 (retrospective)** = 対話全体を振り返るメタ対話——「何がうまくいき、何がうまくいかなかったか」
- **Lessons learned** = 将来の対話に向けた知見の蓄積——**組織的学習**

回顧は ch06 のインシデント管理における post mortem と同様、対話の質を継続的に改善するメカニズムである。

---

## 7. 測定は「対話の効果の定量化」である

### SWEBOK の記述

> "Management without measurement (qualitative and quantitative) suggests a lack of discipline, and measurement without management suggests a lack of purpose or context." (Introduction)

> "Measurement refers to the assignment of values and labels to software engineering work products, processes and resources, plus the models derived from them." (Introduction)

### 言語行為としての意義

測定は、対話の効果（成果物の品質、プロセスの効率、リソースの使用）を**定量化**する行為である:

- 「management without measurement = lack of discipline」= 対話の効果を確認せずに対話を続けることの非合理性
- 「measurement without management = lack of purpose」= 測定データ（報告的発話）が目的なく集められることの無意味さ
- 測定情報モデル (ISO/IEC/IEEE 15939) = 何を測り、どう分析し、どう報告するかの**メタ対話の形式化**

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| ソフトウェアの可塑性 | 発話の可塑性 | 接地先に関わる発話の可塑性はどの程度か |
| 要求の交渉 | 対話の開始と合意形成 | 接地先はどのように交渉に参加するか |
| 見積もり | 対話の見通しの形成 | 接地先を含む開発の見積もりは可能か |
| リスク管理 | 対話の不確実性への対処 | 接地先に関するリスクはどう管理するか |
| 監視・制御・報告 | メタレベルの対話管理 | 接地先との対話の進捗はどう測るか |
| クロージャ・回顧 | 対話の総括と反省 | 接地先を含む回顧はどう行うか |
| 測定 | 対話の効果の定量化 | 接地先との対話の効果はどう測定するか |
