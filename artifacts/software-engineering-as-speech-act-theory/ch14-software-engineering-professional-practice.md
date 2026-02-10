# Chapter 14: Software Engineering Professional Practice — 言語行為としての読解

> SWEBOK v4 Chapter 14 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 専門職実践とは「対話の倫理的・制度的基盤」の確立である

ソフトウェア工学の専門職実践は、ソフトウェア開発という対話を**倫理的に、責任を持って、制度的な枠組みの中で**遂行するための知識・態度・技能の体系である。対話の質は、技術的側面だけでなく、対話者の**誠実性、能力、社会的責任意識**に依存する。

---

## 1. 倫理規範は「対話の根本的な格率」である

### SWEBOK の記述

> "Codes of ethics and professional conduct describe the values and behavior that an engineer's professional practice and decisions should embody." (§1.2)

> "Violations may be acts of commission, such as concealing inadequate work, disclosing confidential information, falsifying information, or misrepresenting abilities." (§1.2)

### 言語行為としての意義

倫理規範は、ソフトウェア工学という対話における**根本的な格率**——Grice の対話の格率の倫理的拡張——である:

- **不適切な成果物の隠蔽** = **質の格率への違反**——真実でないことを語る
- **機密情報の漏洩** = **対話の信頼条件の侵害**——対話の文脈を無視した情報の開示
- **情報の偽造** = **誠実性条件の根本的違反**——意図的な虚偽の発話
- **能力の虚偽表示** = **準備条件の詐称**——発話の前提（能力）を偽る

倫理規範の違反は、個別の発話の失敗ではなく、**対話の信頼基盤そのものの毀損**であり、それゆえに厳しい制裁が伴う。

---

## 2. 認証・資格・免許は「対話者の能力の制度的保証」である

### SWEBOK の記述

> "Professional certification can verify the holder's ability to meet professional standards and to apply professional judgment in solving or addressing problems." (§1.1.2)

> "Engineers are licensed to protect the public from unqualified individuals." (§1.1.3)

### 言語行為としての意義

認証・資格・免許の制度は、**対話者が信頼に値する能力を持つことの制度的保証**である:

- **認定 (Accreditation)** = 教育機関が「対話者を正しく育成できる」ことの保証
- **認証 (Certification)** = 個人が「対話に必要な能力を持つ」ことの確認
- **免許 (Licensing)** = 個人が「対話を公式に行う権限を持つ」ことの認可

これは、言語行為論における**準備条件 (preparatory condition)** の制度化である。発話者が「適切な権限と能力を持つ」ことは、発話の適切性（felicity）の前提条件であり、その前提を社会的に保証する仕組みが免許制度。

---

## 3. コミュニケーションスキルは「対話の質を直接決定する能力」である

### SWEBOK の記述

> "A software engineer must communicate well, both orally and in reading and writing." (§3)

> "Clear, concise writing is important because writing is often the primary method of communication among relevant parties." (§3.2)

> "The software engineer's ability to convey concepts effectively in a presentation influences product acceptance, management, and customer support." (§3.4)

### 言語行為としての意義

コミュニケーションスキルは、ソフトウェア工学を言語行為として見た場合、最も直接的に対話の質を決定する能力である:

- **読解力** = 他者の発話を正確に理解する能力——**解釈の能力**
- **文書作成力** = 発話を正確・明確に記録する能力——**発話の精密さ**
- **プレゼンテーション力** = 発話を効果的に伝達する能力——**発語媒介効果の最大化**
- **チームコミュニケーション** = 多者間の対話を円滑に行う能力——**多声的対話の調整**

「reading and comprehending source code are also components of information-gathering」は、コードの読解が**他者の発話の解釈**であることを明確に示す。

---

## 4. チーム力学は「対話の社会的条件」である

### SWEBOK の記述

> "Performing teams — those who demonstrate a consistent quality of work and progress toward goals — are cohesive and possess a cooperative, honest and focused atmosphere." (§2.1)

> "Team members facilitate this atmosphere by being intellectually honest, using group thinking, admitting ignorance, and acknowledging mistakes." (§2.1)

### 言語行為としての意義

チーム力学は、対話が成立し質を保つための**社会的・心理的条件**である:

- **知的誠実性** = Grice の質の格率——「わからないことはわからないと言う」
- **無知の承認** = 対話における**準備条件の誠実な表明**——「語る能力が不十分であると認める」
- **誤りの承認** = 発話の失敗を率直に認める——**対話の修復可能性の確保**
- **建設的なレビュー** = 他者の発話を人格攻撃ではなく改善の観点から評価する——**対話の非対立的な改善**

これらは、ソフトウェア開発という対話が**心理的に安全な空間**で行われることの条件であり、対話の質の根本的な前提。

---

## 5. 不確実性と曖昧性への対処は「対話の不完全性との共存」である

### SWEBOK の記述

> "Software engineers must often deal with and resolve uncertainty and ambiguities while providing services and developing products." (§2.5)

> "Often, uncertainty reflects a lack of knowledge. If that is the case, investigating the issue by reading formal sources [...] or consulting with teammates and peers can likely solve the problem." (§2.5)

### 言語行為としての意義

不確実性と曖昧性は、対話において**意味が完全に確定しない**状況である:

- **不確実性** = 必要な情報が不足している——対話の**情報的空白**
- **曖昧性** = 複数の解釈が可能である——対話の**多義性**
- 対処法: 情報収集、ステークホルダーへの問い合わせ、チームとの相談——すべて**追加的な対話**による解決

不確実性を解消できない場合はリスクとして扱う——これは、対話の不完全性を**管理すべき不確定性**として受け入れる態度。

---

## 6. 多様性と包摂性は「対話の開放性の条件」である

### SWEBOK の記述

> "Multicultural environments are prevalent in software engineering, perhaps more than in other engineering fields." (§2.6)

> "For a software project to succeed, team members must embrace tolerance of different cultural and social norms." (§2.6)

### 言語行為としての意義

多様性と包摂性は、対話の**開放性と参加の平等性**の条件である:

- **多文化環境** = 異なる言語・文化・規範を持つ行為者が対話に参加する状況
- **包摂性** = すべての参加者が対話に平等にアクセスし貢献できること
- **ダークパターン**（§1.7.9 で言及）の禁止 = 利用者を欺く対話の禁止——**対話の誠実性の要請**

ソフトウェアが「people and for people」であるならば、対話の参加者の多様性を尊重し、対話から排除される者がいないことが、対話の正当性の条件となる。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| 倫理規範 | 対話の根本的な格率 | 接地先との対話における倫理はどう定義されるか |
| 認証・資格・免許 | 対話者の能力の制度的保証 | 接地先と対話する能力はどう保証するか |
| コミュニケーションスキル | 対話の質を直接決定する能力 | 接地先との対話に必要な能力は何か |
| チーム力学 | 対話の社会的条件 | 接地先を含むチームの力学はどう変わるか |
| 不確実性への対処 | 対話の不完全性との共存 | 接地先に関する不確実性はどう扱うか |
| 多様性・包摂性 | 対話の開放性の条件 | 接地先の多様性はどう尊重されるか |
