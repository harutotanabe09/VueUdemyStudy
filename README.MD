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

・v-ifは、直後にv-elseなどが必要。間に挟むのNG

・templateタグは表示されない。変数は、templateタグに入れ込むのが良いかなと思う。

```vue
<template v-for="(fruit,index) in fruits">
	<li>{{index}}{{fruit}}</li>
</template>
↑
同じ
↓
<li v-for="(fruit,index) in fruits">{{index}}{{fruit}}</li>
```

・v-showは、カチカチクリックする場合
　反対に、v-ifは、条件が一度読み込んで変わらない場合に使用する

・**常に `v-for` に対しては `key` を使用してください。**
　結構裏で色々やっているっぽい。

https://www.udemy.com/course/vue-js-complete-guide/learn/lecture/15371092#overview
https://jp.vuejs.org/v2/style-guide/index.html

・Vueインスタンスは、複数作れるし、共有できるが・・・




### スタイルガイドと向き合う


https://jp.vuejs.org/v2/style-guide/index.html