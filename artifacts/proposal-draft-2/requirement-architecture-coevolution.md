# requirement と architecture の共進化

___「共進化」という用語は検討が必要かもしれない___

emulsification はこのモデルでの最小単位のプロセスであったが, requirement と architecture の共進化は最小単位のプロセスの集まりをどのようにして構造化するかを扱う.

一回限りの emulsification で望みのものを手に入れられるとは限らない (というよりは, ほとんどの場合手に入れられない). また, 一回の emulsification はできる限り短い時間で行われるべきである. そのために, 最小単位である emulsification を繰り返すことになる.　その繰り返し方を規定するのが requirement と architecture の共進化である.

一回の emulsification が終わると, その過程と結果は, requirement と architecture にフィードバックされる. それに応じて requirement が変更される場合がある. また, architecture も選択を変更したり, より詳細な調査と分析を行ったり, さらには architecture から requirement に移動される (すなわち, 所与の条件として扱うのではなく, 自前で扱う) 場合もある.

requirements も architectures も変化を被り得るという点が重要である. ただし, それは複雑さを招き寄せるかもしれない.

## 共進化のトポロジ

複数の連続する emulsification を構成する方法もいくつか考えられる.

- 直線
  - 後戻りせず, 一本道で変更を積み重ねる
- 木
  - 複数の選択肢を実験して, その中から一つを選択して先に進む
- 束
  - 複数の選択肢を実験して, その中の複数の良い点悪い点を取捨選択し, 合成して先に進む
- グラフ
  - 後戻りや循環を許す
- それらの組み合わせ
