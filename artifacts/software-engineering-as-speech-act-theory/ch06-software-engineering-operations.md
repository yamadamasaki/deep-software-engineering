# Chapter 06: Software Engineering Operations — 言語行為としての読解

> SWEBOK v4 Chapter 6 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 運用とは「発話が現実の中で生き続ける」ための営みである

ソフトウェア運用は、開発段階で完成した発話（ソフトウェア）が、実際の使用環境の中で意図通りに機能し続けることを保証する活動である。構築が「発話の生成」であるなら、運用は「発話が現実世界の中で生き続けるための支援」——発話の**パフォーマティブな持続**——である。

---

## 1. Infrastructure as Code は「環境の宣言的記述」である

### SWEBOK の記述

> "Having end-to-end resources and desired state configuration managed like code, using practices such as IaC and PaC, provides value in the form of improved repeatability, consistency/standardization, known security policies, self-documentation (transparency), single source of truth." (§Introduction)

> "From an engineering perspective, the important point is that nearly anything that impacts a software product directly or indirectly should be considered for representation as code." (§Introduction)

### 言語行為としての意義

Infrastructure as Code (IaC) は、実行環境自体を**宣言的言語行為**として記述するアプローチである:

- 環境構成を「コード（発話）」として明文化する——暗黙知の言語化
- **Self-documentation**: 環境それ自体が自己を語る——自己参照的な発話
- **Single source of truth**: 唯一の正典——発話の権威ある版の確立

これは、対話の文脈（環境）そのものを形式化し、再現可能にする試みである。

---

## 2. DevOps は「開発と運用の対話統合」である

### SWEBOK の記述

> "Progressive organizations now co-locate software development, software maintenance and some software engineering operations activities (often provided as a service and often coined DevOps). Benefits of this approach are the elimination of the organizational silos that separated these software activities." (§Introduction)

### 言語行為としての意義

DevOps は、開発者と運用者という**異なる行為者間の対話の障壁を除去する**組織的取組みである:

- 従来: 開発（発話の生成者）と運用（発話の管理者）が分離——「投げ渡し」モデル
- DevOps: 生成者と管理者が同一チーム——**継続的対話**モデル
- サイロの解消 = 対話のチャネルの統合

Conway の法則の逆適用として読める: 対話構造を変えることで、ソフトウェアのあり方を変える。

---

## 3. 監視・テレメトリは「計算機からの応答を聴く」行為である

### SWEBOK の記述

> "Monitoring and telemetry are key aspects of software engineering operations. They collect data at all layers of the software system (including application, operating system and server) and extract information that can be used to analyze and monitor different aspects." (§6.4)

> "In a DevOps mindset, hope should not be a strategy; instead, engineers should be informed about system quality and operational health with evidence." (§4.3)

### 言語行為としての意義

監視とテレメトリは、**計算機（実行環境）からの応答を体系的に聴く**仕組みである:

- ログ、メトリクス、トレース = 計算機が発する**報告的発話 (assertive)**
- ダッシュボード = 計算機の発話を人間が理解できる形式に翻訳する
- アラート = 計算機による**警告的発話** ——「異常が発生している」という報告

「hope should not be a strategy」は、**計算機の声を無視して希望的観測に頼ってはならない**という宣言である。

---

## 4. SLA はサービス提供者と利用者の間の「契約的言語行為」である

### SWEBOK の記述

> "Defining, agreeing to and documenting service-level agreements (SLAs) can help clarify the full range of operations services obligations provided." (§2.3)

### 言語行為としての意義

SLA は ch04 で論じた Design by Contract の運用版——**運用段階における約束の形式化**である:

- **SLI (Service-Level Indicators)**: 何を測定するか——語彙の定義
- **SLO (Service-Level Objectives)**: どの水準を約束するか——約束の内容
- **SLA**: 約束の法的形式化——**契約的言語行為 (commissive)**

---

## 5. インシデント管理は「異常報告と修復の対話プロトコル」である

### SWEBOK の記述

> "Incident management is the process of recording, prioritizing and assessing the business impact, resolution, escalation and closure of software incidents." (§4.1)

> "When an incident occurs, proper analysis and/or post mortems must be conducted to find the source of the incident." (§4.1)

### 言語行為としての意義

インシデント管理は、**システムの異常を報告し対処する対話のプロトコル**である:

- インシデント報告 = 計算機（または利用者）からの**異常通知**（報告的発話）
- 優先順位付け = 報告の**重要性の評価**
- Post mortem = **事後的なメタ対話** ——何が起こり、なぜ起こり、どう防ぐかの振り返り

Post mortem は、対話の失敗（システム障害）からの学習メカニズムであり、対話の質の継続的改善に寄与する。

---

## 6. ロールバックは「発話の撤回」の制度化である

### SWEBOK の記述

> "Software engineers ensure that when a new version of the software and its databases have been modified and deployed to production, they can easily and quickly be rolled back in case the new version is causing defects." (§3.3)

### 言語行為としての意義

ロールバックは、**発話の撤回 (retraction)** を制度的に可能にする仕組みである:

- デプロイ = 新しい発話の発出
- ロールバック = 発話の撤回と以前の発話への復帰
- Canary release = 発話を**限定的な聴衆に向けて試行**する——対話の「予行演習」

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| Infrastructure as Code | 環境の宣言的記述 | 接地先の環境も「コード」として記述できるか |
| DevOps | 対話の組織的統合 | 接地先を含む DevOps は可能か |
| 監視・テレメトリ | 計算機の応答を聴く | 接地先からのテレメトリは取得できるか |
| SLA | 運用段階の契約的言語行為 | 接地先との SLA は定義できるか |
| インシデント管理 | 異常報告と修復の対話プロトコル | 接地先の「異常」をどう検知するか |
| ロールバック | 発話の撤回の制度化 | 接地先に影響する変更の撤回は可能か |
