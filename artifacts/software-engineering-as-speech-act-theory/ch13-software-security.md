# Chapter 13: Software Security — 言語行為としての読解

> SWEBOK v4 Chapter 13 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: セキュリティとは「発話の完全性・機密性・可用性の保護」である

ソフトウェアセキュリティは、ソフトウェアという発話が**不正な開示・改竄・利用不能化から保護される**ことを保証する活動である。言語行為の観点からは、セキュリティとは「発話が意図された聴き手にのみ正しく届き、不正な第三者によって傍受・改竄・妨害されない」ことの保証——**対話の信頼基盤の防衛**——である。

---

## 1. CIA三要素は「対話の信頼性の三条件」である

### SWEBOK の記述

> "Information security preserves confidentiality, integrity and availability of information. Other properties, such as authenticity, accountability, non-repudiation and reliability can also be involved." (§1.2)

### 言語行為としての意義

情報セキュリティの CIA 三要素は、対話の信頼性を保証する三つの条件に対応する:

- **機密性 (Confidentiality)**: 発話が意図された聴き手にのみ届くこと——**対話の秘密性**
- **完全性 (Integrity)**: 発話が改竄されずに届くこと——**発話の正確な伝達**
- **可用性 (Availability)**: 発話がいつでもアクセスできること——**対話の継続可能性**

追加的な特性——真正性 (authenticity)、説明責任 (accountability)、否認防止 (non-repudiation)——は、「誰がその発話を行ったか」の確実な特定と、「発話を行ったことを後から否定できない」ことの保証であり、**対話の帰属性**を確保する。

---

## 2. セキュリティ設計は「対話の防衛的設計」である

### SWEBOK の記述

> "Security design concerns how to prevent unauthorized disclosure, creation, change, deletion or denial of access to information and other resources." (§4.2)

> "To meet security requirements, developers conduct threat modeling, illustrating how a system is being attacked to specify a security design for the mitigation." (§4.2)

### 言語行為としての意義

セキュリティ設計は、対話が**悪意ある第三者によって攻撃される可能性**を前提として、防衛的に対話を設計する活動である:

- **脅威モデリング** = 「誰が、どのようにこの対話を攻撃するか」の分析——**悪意ある聴き手の想定**
- **アクセス制御** = 「誰が発話を聴く・変更する権限を持つか」の統制——**対話の参加資格の管理**
- **暗号技術** = 発話を符号化して不正な聴き手に理解不能にする——**対話の暗号化**

通常の対話設計が「正しい伝達」を志向するのに対し、セキュリティ設計は「不正な伝達の防止」を志向する——**対話の否定的条件の設計**。

---

## 3. セキュアコーディングは「発話の脆弱性を防ぐ記述規範」である

### SWEBOK の記述

> CERT/CC の Top 10 Software Security Practices: "1. Validate input. [...] 5. Default deny. 6. Adhere to the principle of least privilege. 7. Sanitize data sent to other software." (§4.4)

### 言語行為としての意義

セキュアコーディングの原則は、発話（コード）が**悪意ある入力（不正な発話）に対して頑健である**ことを保証する記述規範である:

- **入力の検証** = 聴き手が受け取る発話の正当性を確認する——「信頼できない話者の発話を鵜呑みにしない」
- **デフォルト拒否** = 明示的に許可されていない発話を拒否する——「許可されていなければ聴かない」
- **最小権限の原則** = 発話の権限を必要最小限に制限する——「必要なことだけを語り、必要な範囲だけで聴く」
- **出力のサニタイズ** = 他者に渡す発話の安全性を保証する——「自分の発話が他者を害さないよう注意する」

これらは本質的に、**対話における信頼の最小化原則 (zero trust)** の実現である。

---

## 4. 脆弱性管理は「発話の欠陥の体系的追跡と修復」である

### SWEBOK の記述

> "Common security defects are categorized and shared with databases: the Common Vulnerabilities and Exposures (CVE), Common Weakness Enumeration (CWE), and Common Attack Pattern Enumeration and Classification (CAPEC)." (§4.6)

### 言語行為としての意義

脆弱性管理は、発話の中に存在する**セキュリティ上の欠陥を体系的に分類・追跡・修復する**活動である:

- **CVE** = 発見された具体的な「言い間違い」（脆弱性）のカタログ
- **CWE** = 「言い間違い」の類型学——同じ種類の誤りを体系的に分類
- **CAPEC** = 「言い間違い」を悪用する攻撃パターンのカタログ——悪意ある聴き手の手口の分類

これは ch12 のエラー・欠陥・故障の分類学のセキュリティ版であり、特に**悪意ある利用者による欠陥の悪用**という、通常の品質管理にはない次元を追加する。

---

## 5. DevSecOps は「セキュリティ対話の統合」である

### SWEBOK の記述

> "DevSecOps (meaning the integration of development, security and operations) has emerged. Beyond SDLC, DevSecOps includes an approach to culture, automation and platform design." (§3.1)

> "Security needs to become an enabler instead of a blocker." (§2.3)

### 言語行為としての意義

DevSecOps は、セキュリティを対話のプロセスに**最初から統合する**文化的・技術的転換である:

- セキュリティを「後から追加する検閲」から「対話の一部」へ——**シフトレフト**
- 「セキュリティは阻害要因ではなく促進要因」= セキュリティは対話を制限するものではなく、**対話の信頼を高めるもの**
- アジャイルなセキュリティ = セキュリティに関する対話もまた**反復的・適応的**に行われるべき

これは ch06 (Operations) および ch10 (Process) で論じた DevOps のセキュリティへの拡張であり、**対話のあらゆる側面にセキュリティを織り込む**という原則の表明。

---

## 6. ドメイン固有のセキュリティは「対話の文脈に応じた防衛」である

### SWEBOK の記述

> "Cloud infrastructure and services are often inexpensive and easy to provision, which can quickly lead to having many assets strewn all over the world and forgotten. These forgotten assets are like a ticking time bomb." (§6.1)

> "Attackers can change the decisions of machine learning models. There are two kinds of attacks: model poisoning, which attacks training data, and evasion, which attacks inputs to trained models." (§6.3)

### 言語行為としての意義

ドメイン固有のセキュリティは、**対話の文脈（クラウド、IoT、機械学習）に応じた特有の脅威に対処する**活動である:

- **クラウド**: 発話（データ・サービス）が物理的に分散し、「忘れられた発話」が脅威となる——**発話の管理範囲の拡大**
- **IoT**: 多数のデバイスが対話に参加し、弱いリンクが全体を危険にさらす——**対話参加者の信頼性の不均一性**
- **機械学習**: 対話の「理解」（モデル）そのものが攻撃対象となる——**解釈の改竄**という新しい脅威

特に機械学習への攻撃（モデルポイズニング、回避攻撃）は、**聴き手の理解そのものを歪める攻撃**であり、従来の「発話の保護」を超えた新しいセキュリティの地平を開く。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| CIA 三要素 | 対話の信頼性の三条件 | 接地先との対話における機密性・完全性・可用性とは何か |
| セキュリティ設計 | 対話の防衛的設計 | 接地先を含む脅威モデリングはどうなるか |
| セキュアコーディング | 発話の脆弱性を防ぐ記述規範 | 接地先からの入力の信頼性はどう検証するか |
| 脆弱性管理 | 発話の欠陥の体系的追跡 | 接地先に影響する脆弱性はどう管理するか |
| DevSecOps | セキュリティ対話の統合 | 接地先を含むセキュリティの統合はどうあるべきか |
| ドメイン固有セキュリティ | 対話の文脈に応じた防衛 | 接地先のドメインに固有のセキュリティ脅威は何か |
