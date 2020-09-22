### Vueのあれこれメモ

・v-onceとどう向き合うべきか
　→　JS内で変数に複数回代入すると値がブレる

.v-htmlは使わないほうがよい？
　→　XSSの脆弱性あり

・v-bind,v-onは省略すべきか？
　→　ディレクティブの短縮記法 
　　　(v-bind: に対する : 、 v-on: に対する @ 、 v-slot: に対する #)は、
　　　常に使うか、まったく使わないかのどちらかにするべきです。

.イベントオブジェクト

・computedプロパティとMethodの使い分け？
  メソッドの２重括弧だと再読込される。ひとつひとつ実行される。関係なくても！

  computedとメソッド違い
  ：onclick="countUp" 
  ：onclick="countUp()"

・クラス名は切り替えられる

・Style属性でHTMLにもかけるし、JSにもかける。


### スタイルガイドと向き合う


https://jp.vuejs.org/v2/style-guide/index.html