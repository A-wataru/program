# program
パケットロス率に関するソースコード

①main.m

収容数毎のパケットロス率をグラフで表示するプログラム

図4.1を出力する

②pakettofunc.m

収容数等を引数としてパケットロス率を出力する関数

③sanpuzu.m

収容数を指定して、その際にパケットロス率が上限を超えるかを３次元プロットで示すプログラム
9行目alphakの値の1/35200の分母と85行目のif文のなかの数値を変更する。
(alphak,if文,図番号)＝(0.8倍,17,4.2)(0.8倍,18,4.3)(0.8倍,19,4.4)(0.8倍,20,4.5)(0.9倍,17,4.6)(0.9倍,18,4.7)(0.9倍,19,4.8)(1.25倍,17,4.9)(1.25倍,18,4.10)(1.5倍,17,4.11)(1.5倍,18,4.12)

④pakettokitaiti.m

パケットロス率の期待値を表示するプログラム

呼損率に関するソースコード

⑤sanjigenn.m

各呼の呼損率を計算している。呼の種類を増減させない限り、いじる必要なし。2とセットで運用する。

⑥sanjigenn2.m

各呼の定常確率を計算している。

⑦sanjisannnnn2.m

閾値を総当たりするプログラム。また、各呼のトラヒック密度や上限呼損率、退去率等を設定している。
現在は何の縛りもなくすべての状態における各呼の呼損率を表示している。
もし、ある一定の呼損率以下の場合のみ実数値を格納したい場合は、100～122行目のコメントマークを解除し、自分で各種条件を設定する。

⑧simulation.m

シミュレーション用のプログラム。各呼のトラヒック密度の条件を設定すれば結果が出る。しかし、呼の到着部分に関しては、各呼が独立して到着するように修正をしなければならない。



動作一覧

・収容数毎のパケットロス率をグラフで表示：①を実行(①と②が動作する)

・収容数を指定し、パケットロス率が上限を超えるかを３次元プロットで表示：③を実行(②と③が動作する)

・収容数毎のパケットロス率をグラフで表示：①を実行(①と②が動作する)

・収容数を指定し、パケットロス率の期待値を返す：④を実行(④と②と⑥が動作する)

・閾値を総当たりした時の呼損率をグラフで表示：⑤を実行(④と⑤が動作する)
