# Chapter 01: Software Requirements — 言語行為としての読解

> SWEBOK v4 Chapter 1 を「ソフトウェア工学は人と計算機との間の言語行為である」という立場から読み、重要なポイントを抽出する。

## 総括: 要求とは「意図の伝達」という言語行為そのものである

ソフトウェア要求の章は、SWEBOK の全章の中で最も直接的に言語行為の問題を扱っている。要求工学が取り組む二大問題——**不完全性 (incompleteness)** と**曖昧性 (ambiguity)**——は、どちらも言語行為の失敗形態に他ならない。この章は、明示的に「intent（意図）」の伝達をソフトウェア要求の本質的役割と位置づけており、言語行為理論の中核概念と直結する。

---

## 1. 要求の二大問題は言語行為の病理である

### SWEBOK の記述

> "Real-world software projects tend to suffer from two primary requirements-related problems:
> 1. **incompleteness**: stakeholder requirements, and necessary detail, exist that are not revealed and communicated to the software engineers;
> 2. **ambiguity**: requirements are communicated in a way that is open to multiple interpretations, with only one possible interpretation being correct." (Introduction)

### 言語行為としての意義

- **不完全性** = **言われなかった発話**: ステークホルダーの頭にある要求が言語化されず、ソフトウェアエンジニアに届かない。発話行為 (locutionary act) そのものが成立していない
- **曖昧性** = **発語内行為の不確定**: 発話はなされたが、その発語内の力 (illocutionary force) が聞き手において一意に定まらない

ソフトウェア要求工学の全プロセス——引き出し、分析、仕様化、検証、管理——は、この二つの言語行為的病理を体系的に克服するための方法論である。

---

## 2. 要求文書の目的は「意図の保存と伝達」である

### SWEBOK の記述

> "The role of requirements documentation throughout the service life of the software is to **capture and communicate intent** for software engineers who maintain the code but might not have been its original authors." (Introduction)

> "What is generally referred to as a bug — but is better called a defect — is simply an **observable difference between what the software is intended to do and what it does**." (Introduction)

### 言語行為としての意義

SWEBOK は「intent（意図）」を明示的に要求文書の本質と位置づけている。これは言語行為理論における**発語内の力 (illocutionary force)** にそのまま対応する。

- **バグの定義**: 「意図されたこと」と「実際に行われたこと」のずれ。すなわち、**発語内行為（こうせよ、という指示）と発語媒介行為（実際の効果）との不一致**
- 要求文書は「何が書かれているか」ではなく「何が意図されているか」を伝えなければならない——形式ではなく力 (force) の伝達が本質

深ソフトウェア工学的に重要なのは、**「意図」は誰の意図か**という問いである。現在の枠組みでは、意図の源泉はステークホルダー（人間）に限定されている。接地先の「意図」——もしそれがありうるとすれば——はこの枠組みには入らない。

---

## 3. 要求開発は「合意形成」という言語行為である

### SWEBOK の記述

> "Requirements development, as a whole, can be thought of as '**reaching an agreement on what software is to be constructed**.'" (§1.11)

> "Requirements management can be considered '**maintaining that agreement over time**.'" (§1.11)

### 言語行為としての意義

SWEBOK 自身が要求プロセスの全体を**合意 (agreement)** として定義している。合意は典型的な**約束的言語行為 (commissive)** の相互的形態である:

- 要求開発 = 「何をつくるか」についての**合意の形成** = 相互的約束の成立
- 要求管理 = **合意の維持** = 約束の履行監視と再交渉

これは、要求が「ソフトウェアの性質の記述」（確認的発話）であるという素朴な理解を超えている。要求は本質的に**行為者間の約束**であり、その成立には双方の合意が必要とされる。

---

## 4. 引き出し (Elicitation) は沈黙から発話を引き出す行為である

### SWEBOK の記述

> "Elicitation is not a passive activity. Even if cooperative and articulate stakeholders are available, the software engineer must work hard to elicit the right information. **Many product requirements are tacit** or can be found only in information that has yet to be collected." (§2.2)

> "Users might have difficulty describing their tasks, **leave important information unstated** or be unwilling or unable to cooperate." (§2.2)

### 言語行為としての意義

引き出しは、**まだ発話されていないもの——暗黙知 (tacit knowledge)——を言語化する行為**である。これは通常の言語行為理論が扱う「発話の分析」の前段階にある問題:

- インタビュー、ワークショップ、プロトタイプ、観察、徒弟制など——これらはすべて**沈黙を破るための手法**
- 5-whys 技法: 「なぜそれが要求なのか」と繰り返し問うことで、表面的な発話の背後にある**真の発語内の力**を掘り出す
- デザイン思考の「共感 (empathize)」フェーズ: 相手の立場に立つことで、相手が語れないものを代わりに語る

深ソフトウェア工学の核心的問いは、ここにある。**接地先は「語れない」のではなく、「語る言語を持っていない」のかもしれない。** 言語モデルが接地先の代弁者 (proxy speaker) となりうるか、という問いは、引き出しの問題の拡張である。

---

## 5. 要求仕様の形式は「発話の厳密さ」のスペクトルである

### SWEBOK の記述

SWEBOK は要求仕様の形式を厳密さの昇順で列挙する:

1. **非構造的自然言語**: "The system shall ..." (§4.1)
2. **構造的自然言語**: actor-action 形式、ユースケース、ユーザストーリー (§4.2)
3. **受入基準ベース**: ATDD, BDD — "Given...When...Then..." (§4.3)
4. **モデルベース**: アジャイルモデリング → 準形式的モデル → 形式的モデル (§4.4)

### 言語行為としての意義

これは**言語行為の形式化の段階**に正確に対応する:

| 形式 | 言語行為的特徴 | 曖昧性 | 表現力 |
|---|---|---|---|
| 非構造的自然言語 | 日常的発話——文脈依存、暗黙の前提 | 高 | 高 |
| 構造的自然言語 | 構文が制約された発話——主語・動詞・条件が明示 | 中 | 中〜高 |
| 受入基準ベース | 具体的シナリオとしての発話——検証可能 | 低 | 中 |
| 形式的モデル | 形式言語による発話——機械的に検証可能 | 最低 | 低 |

特に重要なのは SWEBOK の以下の指摘:

> "If we simply modify that phrase to say, 'the software **shall** produce,' ... what first looked like a test case now looks like a requirement." (§4.3)

「〜すべし (shall)」は**指示的言語行為 (directive)** の標識である。テストケースの「期待される」と要求の「すべし」の違いは、発語内の力の差異——記述 vs. 指示——に過ぎない。SWEBOK はこの境界の薄さを明示的に認めている。

---

## 6. 派生要求: 設計上の決定が次の階層への指示となる

### SWEBOK の記述

> "An architect's decision to use a pipes-and-filters architecture style would not be a requirement from the perspective of the overall project stakeholders, but a design decision. But that same decision, when seen from the perspective of a sub-team responsible for constructing a particular filter, would be considered a requirement." (§1.10)

### 言語行為としての意義

同じ発話が、文脈（聞き手の立場）によって**記述的発話 (constative)** にも**指示的発話 (directive)** にもなりうる。

- アーキテクトが「パイプ＆フィルタを採用する」と言うとき、プロジェクト全体から見ればそれは**宣言 (declaration)**
- サブチームから見れば、それは**指示 (directive)** ——「フィルタとして実装せよ」
- 言語行為の力は**発話者と聞き手の関係**によって変化する

これは組織内での**言語行為のカスケード**——一つの発話が連鎖的に新たな指示を生む構造——を示している。

---

## 7. 要求の衝突と交渉: 対抗する発語内行為の調停

### SWEBOK の記述

> "When a project has more — and more diverse — stakeholders, **conflicts among the requirements** are more likely." (§3.4)

> "One approach is to **negotiate** a resolution among the conflicting stakeholders." (§3.4)

> もう一つのアプローチは product family development——不変要求と可変要求を分離する (§3.4)

### 言語行為としての意義

要求の衝突は、**異なる行為者からの指示的発話が矛盾する状況**である。解決法は二種類:

1. **交渉**: メタ言語的行為——「何を言うべきか」についての対話。Fisher & Ury の *Getting to Yes* が参照されていることは、要求工学が本質的に**交渉学**であることを物語る
2. **プロダクトファミリ**: 不変要求（全員が合意する発話）と可変要求（文脈依存の発話）を分離し、矛盾を構造的に吸収する

---

## 8. 要求検証は発話の適切性条件の確認である

### SWEBOK の記述

> "Requirements validation concerns gaining confidence that the requirements **represent the stakeholders' true needs** as they are currently understood." (§5)

> 各要求は「unambiguous, testable, binding, atomic」であるべきで、全体は「complete, concise, internally consistent, externally consistent, feasible」であるべき (§3.1)

### 言語行為としての意義

これは言語行為理論における**適切性条件 (felicity conditions)** の体系的チェックに他ならない:

| 要求の望ましい性質 | 対応する適切性条件 |
|---|---|
| unambiguous（曖昧でない） | 命題内容条件: 発話内容が一意に特定できる |
| testable（検証可能） | 発語内行為が観察可能な効果を持つ |
| binding（拘束力がある） | 本質条件: 発話者が義務を引き受ける意図を持つ |
| represents true needs | 誠実性条件: 発話者が本当にそう信じている |
| complete（完全） | すべての適切な発話がなされている |
| consistent（一貫） | 発話間に矛盾がない |

レビュー、シミュレーション、プロトタイプは、いずれも**「この発話は本当に意図通りか」を問い直すメタ対話**の手法である。

---

## 9. ステークホルダー分析: 「誰が発話権を持つか」の制度設計

### SWEBOK の記述

ステークホルダーとして列挙されるのは: clients, customers, users, SMEs, operations staff, support staff, regulatory agencies, special interest groups, developers, さらに「people who can be negatively affected if the project is successful」(§2.1)

> "Requirements are not limited to only coming from people. Other, **non-person requirements sources** can include: documentation, other systems, larger business context, computing environment." (§2.1)

### 言語行為としての意義

SWEBOK は「人でない要求源」を認めている。これは重要な転換点だが、限定的である。「他のシステム」や「規制」は要求の**源泉 (source)** としては認められているが、**発話者 (speaker)** としては認められていない——これらは「参照される」のであって、対話に参加するのではない。

深ソフトウェア工学の視座からは、ここに問いが立つ: **要求の源泉と発話者の区別を崩すとき、何が起きるか。** 接地先が「参照される対象」ではなく「自ら要求を述べる行為者」になるとき、引き出し・分析・仕様化・検証のすべてのプロセスが変容する。

---

## 10. 暗黙知と Perfect Technology Filter: 言語化の境界

### SWEBOK の記述

> "Functional requirements are those that would still need to be stated **even if a computer with infinite speed, unlimited memory, zero cost, no failures, etc., existed**." (§1.8)

### 言語行為としての意義

Perfect Technology Filter は、**テクノロジーに依存する発話と、接地先の本質に根ざす発話とを分離する**思考実験である。

- 機能要求 = 接地先の論理に根ざす発話（「口座残高は負になってはならない」——これは銀行業の本質）
- 非機能要求 = テクノロジー制約に根ざす発話（「応答時間は3秒以内」——これは計算機の制約）

この区別は、深ソフトウェア工学が求める**接地先の声**と、それを媒介する道具（計算機・言語モデル）の制約とを峻別する枠組みとなりうる。

---

## まとめ: この章が示唆する深ソフトウェア工学への問い

| SWEBOK の概念 | 言語行為としての読替え | 深ソフトウェア工学への問い |
|---|---|---|
| 不完全性 (incompleteness) | 発話されなかった言語行為 | 接地先の「沈黙」をどう聴くか |
| 曖昧性 (ambiguity) | 発語内の力の不確定 | 行為者間の翻訳は曖昧性を解消できるか |
| Intent（意図） | 発語内の力 (illocutionary force) | 接地先に「意図」はあるか |
| 合意 (agreement) | 相互的約束行為 | 接地先との合意は成立しうるか |
| 引き出し (elicitation) | 沈黙から発話を引き出す行為 | 言語モデルは接地先の代弁者となるか |
| "shall" 仕様 | 指示的言語行為 | 接地先からの「shall」は何か |
| 派生要求 | 言語行為のカスケード | 接地先→人間→計算機のカスケードは可能か |
| 要求の衝突 | 発語内行為の矛盾 | 接地先の「要求」は他と衝突するか |
| 検証 | 適切性条件の確認 | 接地先の「真のニーズ」とは何か |
| ステークホルダー | 発話者 vs. 発話の源泉 | 接地先を発話者として認めるとき何が変わるか |
| Perfect Technology Filter | 接地先の論理 vs. 道具の制約 | 接地先固有の論理をどう抽出するか |
