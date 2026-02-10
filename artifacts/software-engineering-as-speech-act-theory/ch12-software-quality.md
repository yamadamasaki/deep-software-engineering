# Chapter 12: Software Quality — 言語行為としての読解

> SWEBOK v4 Chapter 12 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 品質とは「発話がその意図を正しく実現しているか」の総合的評価である

ソフトウェア品質は、ソフトウェアという発話が**ステークホルダーの期待（意図された了解）を正しく実現しているか**の総合的評価である。品質の多義性——「要求への適合」「用途への適合性」「顧客が最終審判者」——は、発話の成功条件が**聴き手によって、文脈によって異なる**ことの反映である。

---

## 1. 品質の定義は「発話の成功条件」の多面的記述である

### SWEBOK の記述

> "Phil Crosby defined quality as 'conformance to requirements.' Watts Humphrey referred to it as 'achieving excellent levels of fitness for use.' Meanwhile, IBM coined the phrase 'market-driven quality,' where the 'customer is the final arbiter.'" (Introduction)

> "Quality depends upon the degree to which those established requirements accurately represent stakeholder needs, wants, and expectations." (Introduction)

### 言語行為としての意義

品質の多様な定義は、言語行為の**成功条件 (felicity conditions)** の異なる側面を捉えている:

- **要求への適合**: 発話が宣言された意図を実現しているか——**発語内効力 (illocutionary force)** の実現
- **用途への適合性**: 発話が聴き手に意図された効果をもたらすか——**発語媒介効果 (perlocutionary effect)** の達成
- **顧客が最終審判者**: 発話の成功は最終的に聴き手が判定する——**了解の主権は聴き手にある**

「requirements accurately represent stakeholder needs」という条件は、品質が要求の正しさにも依存すること——**意図の言語化の正確さ**——を示す。

---

## 2. エラー・欠陥・故障の区別は「発話の失敗の分類学」である

### SWEBOK の記述

> "Error: 'Human action that produces an incorrect result.'" / "Defect: 'An imperfection or deficiency in a work product.'" / "Failure: 'The termination of the ability of a system to perform a required function.'" (§1)

### 言語行為としての意義

この三層の区別は、言語行為の**失敗の分類**に対応する:

- **エラー (Error)**: 発話者の行為の誤り——「言い間違い」の原因行為
- **欠陥 (Defect)**: 発話の中に潜む不完全さ——「言い間違い」そのもの（テクストに残る痕跡）
- **故障 (Failure)**: 発話が聴き手に伝わった時の失敗——「通じなかった」「誤解を招いた」

人間のエラーが欠陥を生み、欠陥が実行時に故障を引き起こす——**意図の失敗が発話の欠陥に、発話の欠陥が伝達の失敗に**至る因果連鎖。

---

## 3. 品質の文化と倫理は「対話の誠実性」の制度的基盤である

### SWEBOK の記述

> "A strong software engineering ethic assumes that engineers accurately report information, conditions and outcomes related to quality." (§1.1)

### 言語行為としての意義

品質文化と倫理は、対話における**誠実性 (sincerity)** の制度的基盤である:

- 正確な報告 = Grice の**質の格率**——真実を語れ、根拠なきことを語るな
- 倫理規範 = 対話における**信頼の基盤**
- 「trade-offs among cost, schedule and quality」の理解 = 対話における制約の誠実な認識

品質に関する対話が不誠実であれば（問題を隠蔽する、楽観的な報告をする等）、プロジェクト全体の対話の基盤が崩れる。

---

## 4. V&V は「発話の二重の検証」である

### SWEBOK の記述

> "Verification ensures that the product is built correctly [...] Validation ensures that the right product is built." (§3.4)

### 言語行為としての意義

V&V は、発話の正しさを**二つの異なる観点**から検証する:

- **Verification**: 発話が文法的・意味論的に正しいか——「言おうとしたことを正しく言えているか」
- **Validation**: 発話が意図した効果をもたらすか——「言うべきことを言えているか」

静的分析・動的分析・形式手法という三つの検証技法は:
- **静的分析**: 発話を実行せずにテクストとして検査する——「読んで確認する」
- **動的分析**: 発話を実行して結果を観察する——「言わせてみて確認する」
- **形式手法**: 発話の正しさを数学的に証明する——「論理的に証明する」

---

## 5. レビューと監査は「第三者による発話の検証」である

### SWEBOK の記述

> "Peer reviews are defined as 'the review of work products performed by peers during development of the work products to identify defects for removal.'" (§3.4.5)

> レビュータイプ: ad hoc, checklist-based, scenario-based, perspective-based, role-based (§3.4.5)

### 言語行為としての意義

レビューは、発話（成果物）の正しさを**第三者が検証する対話的プロセス**である:

- **Ad hoc レビュー**: 自由な読解による検証
- **チェックリストベース**: 体系的な検査項目に基づく検証
- **シナリオベース**: 想定される利用場面に沿った検証
- **視点ベース (perspective-based)**: 特定のステークホルダーの視点からの検証——**異なる聴き手の立場に立つ**
- **役割ベース**: 特定の役割の視点からの検証

ペアプログラミングは「継続的レビュー」として、**コーディング（発話の生成）と検証を同時に行う**革新的な対話形式である。

---

## 6. ディペンダビリティは「発話の信頼性への要請」である

### SWEBOK の記述

> "System and software dependability regroups several related quality characteristics: availability, reliability, maintainability and supportability, safety and security." (§1.4.1)

### 言語行為としての意義

ディペンダビリティは、発話が**信頼に値する**ことへの総合的な要請である:

- **可用性 (availability)**: 発話がいつでもアクセスできること
- **信頼性 (reliability)**: 発話が一貫して正しく機能すること
- **保守性 (maintainability)**: 発話が修正可能であること
- **安全性 (safety)**: 発話が害を与えないこと
- **セキュリティ (security)**: 発話が不正に改竄されないこと

安全性重要システムにおけるインテグリティレベルは、「この発話がどれほど信頼されなければならないか」の**信頼度等級**であり、レベルに応じて検証の厳密さが段階的に要求される。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| 品質の定義 | 発話の成功条件の多面的記述 | 接地先にとっての「品質」とは何か |
| エラー・欠陥・故障 | 発話の失敗の分類学 | 接地先に影響する失敗はどう分類されるか |
| 品質文化・倫理 | 対話の誠実性の制度的基盤 | 接地先との対話における誠実性とは何か |
| V&V | 発話の二重の検証 | 接地先を含む検証と妥当性確認はどう行うか |
| レビュー・監査 | 第三者による発話の検証 | 接地先はレビューにどう参加するか |
| ディペンダビリティ | 発話の信頼性への要請 | 接地先に影響するシステムの信頼度をどう保証するか |
