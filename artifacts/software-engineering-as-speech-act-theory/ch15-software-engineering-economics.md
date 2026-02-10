# Chapter 15: Software Engineering Economics — 言語行為としての読解

> SWEBOK v4 Chapter 15 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 経済学とは「対話の価値判断の枠組み」である

ソフトウェア工学経済学は、ソフトウェアという発話が**経済的な価値を持つか、投資に見合う成果をもたらすか**を判断する枠組みを提供する。言語行為の観点からは、経済学とは「この対話に参加する価値があるか」「この発話にどれだけの資源を投じるべきか」という**対話の価値判断**のための体系的方法論である。

---

## 1. 提案と代替案は「対話の方向の選択肢」である

### SWEBOK の記述

> "A proposal — a single, separate course of action to be considered." (§1.1)

> "One special case is known as the do-nothing alternative. Sometimes the best course of action is not to carry out any of the proposals being considered." (§1.6)

### 言語行為としての意義

提案 (proposal) と代替案 (alternative) は、対話の**方向性に関する選択肢**である:

- 各提案 = 「この対話をこの方向に進めるべきだ」という主張的言語行為 (assertive)
- 代替案の比較 = 複数の対話の方向性の**経済的評価**
- **Do-nothing 代替案** = 「この対話を行わない」という選択肢——対話そのものの必要性の問い直し

ソフトウェア工学のあらゆる意思決定——アーキテクチャの選択、ライブラリの購入か自作か、リファクタリングか放置か——は、**対話をどのように進めるかの経済的選択**として表現できる。

---

## 2. 意思決定プロセスは「選択の対話の形式化」である

### SWEBOK の記述

> 意思決定プロセス: "Understand the real problem → Identify all reasonable technically feasible solutions → Define the selection criteria → Evaluate each alternative → Select the preferred alternative → Monitor the performance." (§2)

> "If the best solution is not among the set of solutions being considered, it cannot be selected." (§2.3)

### 言語行為としての意義

工学的意思決定プロセスは、**何を発話すべきか（何を構築すべきか）の選択を体系的に行う対話**である:

- **真の問題の理解** = 「何について語るべきか」の正確な把握——問いの正しい設定
- **解の同定** = 可能な発話の選択肢を網羅的に列挙する
- **選択基準の定義** = 発話の成功を何で測るかの合意
- **評価** = 各選択肢を基準に照らして分析する
- **監視** = 選択された発話が期待通りの効果をもたらしているかの確認

「高い帰結を伴う決定にはより多くの時間と注意を費やすべき」という指針は、**対話の重要度に応じた資源配分**の原則。

---

## 3. 無形資産は「対話の中に蓄積された暗黙知」である

### SWEBOK の記述

> "Intangible assets, also known as knowledge assets, are any knowledge that lies in the non-visible side of an organization but affects that organization's financial performance." (§1.7)

> "This can include, but is not limited to, policies, procedures, tools and specifications, as well as organizational culture, experience and know-how." (§1.7)

### 言語行為としての意義

無形資産は、組織の対話の中に蓄積された**暗黙知 (tacit knowledge) と制度化された知識 (explicit knowledge)** である:

- **方針、手続き、ツール、仕様** = 対話の**制度化された規範と道具**
- **組織文化、経験、ノウハウ** = 対話の**暗黙の前提と蓄積された知恵**
- 無形資産の同定と評価 = 「組織が過去の対話から何を学び、何を蓄積してきたか」の可視化

SIPAC (Strategic Intangible Process Assets Characterization) 方法論は、無形資産の品質と影響度を定量化する手法であり、「**対話の蓄積がビジネス目標にどう貢献しているか**」を客観的に評価する枠組みを提供する。

---

## 4. 見積もりは「対話の見通しの推定」である

### SWEBOK の記述

> "An estimate analytically predicts some quantity, like a project's size, cost or schedule." (§8)

> "All estimates are inherently uncertain. [...] Fortunately, estimates need not be perfect; they need only to be good enough to lead the decision-maker to make the right decision." (§8)

> "3.09. Ensure realistic quantitative estimates [...] and provide an uncertainty assessment of these estimates." (§8, citing Software Engineering Code of Ethics)

### 言語行為としての意義

見積もりは、対話の**将来の展開に関する推定的発話**であり、その本質は不確実性にある:

- 見積もりの手法（専門家判断、類推、分解、パラメトリック）= **推定の根拠の多様性**
- 見積もりの不確実性 = 未来の対話の展開は原理的に確定できない——**対話の未決定性**
- 「見積もりは完全である必要はない、十分に良ければよい」= **実用的な不確実性の管理**
- 複数の見積もりの併用 = **多声的な推定**による精度の向上

見積もりの倫理的要請——「現実的な見積もりを提供し、不確実性の評価を付随させること」——は、ch14 の倫理規範と直結し、対話における**誠実性の要請**の具体的形態。

---

## 5. 多属性意思決定は「複数の格率の重み付け」である

### SWEBOK の記述

> "Often, other criteria, other 'attributes,' need to be considered that can't be cast in terms of money." (§6)

> "Compensatory techniques [...] collapse all criteria into a single figure of merit." / "Non-compensatory techniques [...] do not allow trade-offs among the criteria." (§6.1, §6.2)

### 言語行為としての意義

多属性意思決定は、対話の成功を**複数の基準で同時に評価する**手法であり、これは対話の格率の重み付けに対応する:

- **補償的技法** = 一つの基準の低さを他の基準の高さで補える——格率間のトレードオフを許容
- **非補償的技法** = 各基準を独立に評価する——各格率を個別に満足させることを要求
- 金銭以外の基準 = 環境への配慮、従業員の福利、顧客忠誠度——**対話の多面的な価値**

「value does not always derive from money alone」という立場は、対話の成果を**経済的価値に還元しない**ことの表明であり、深ソフトウェア工学の「接地先」の価値を考える上で重要な示唆を含む。

---

## 6. 生産性と手戻りは「対話の効率と修復コスト」である

### SWEBOK の記述

> "Productivity is the ratio of output to input from an economic perspective." (§10.6)

> "Most software organizations are unaware that the single largest resource consumer is, in fact, rework." (§10.6)

> "The most effective way to increase productivity can be to simply reduce rework." (§10.6)

### 言語行為としての意義

生産性と手戻りは、対話の**効率性と、発話の修復にかかるコスト**の問題である:

- **生産性** = 対話が生み出す価値と投入される資源の比率——**対話の効率**
- **手戻り (rework)** = 発話の誤りを修正する活動——**対話の修復コスト**
- 手戻りが最大のコスト要因 = **発話の失敗の修復が最も資源を消費する**

「手戻りを減らすことが生産性向上の最も効果的な方法」という知見は、ch12 (Quality) の品質管理と直結し、**発話の質を最初から高めることが最も経済的である**ことを示す——まさに「言い直すより、最初から正しく言え」。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| 提案と代替案 | 対話の方向の選択肢 | 接地先を含む対話の方向はどう選ばれるか |
| 意思決定プロセス | 選択の対話の形式化 | 接地先を含む意思決定はどう行うか |
| 無形資産 | 対話の中に蓄積された暗黙知 | 接地先に関する暗黙知はどう評価するか |
| 見積もり | 対話の見通しの推定 | 接地先を含む開発の見積もりはどう行うか |
| 多属性意思決定 | 複数の格率の重み付け | 接地先の価値はどう評価基準に含めるか |
| 生産性と手戻り | 対話の効率と修復コスト | 接地先との対話における手戻りコストはどう削減するか |
