## find()
対象要素の子孫要素から、指定の要素を取得するメソッド。
子要素に限らず、孫要素、そのまた子要素など、対象要素の下の書いそうであればどこの階層からも検索が可能。
https://www.sejuku.net/blog/37474

## prop() / attr()
https://www.sejuku.net/blog/36294
https://qiita.com/kbyay_/items/7a7ce9547f29b34a63b1

`prop()`は、指定した属性の値の取得・変更や、`disable`や`checked`などのプロパティの真偽を取得してくれる。
`attr()`は、指定した属性の値の取得・変更や、`disable`や`checked`などのプロパティそれ自体を取得してくれる。

## removeAttr()
属性を削除する。指定した値のみではなく、属性そのものを削除する。
 
## append()
引数で指定したコンテンツ(文字列やhtml、jQuery)を要素に追加する。
http://semooh.jp/jquery/api/manipulation/append/content/

## val()
指定した要素のvalue属性の値を取得・変更・設定する。
valueは、その要素の初期値を設定する。
https://www.sejuku.net/blog/45297
```html
<button id="btn-a" value="a">ボタンA</button>
```
```
var btn = $('#btn-a').val(); 
console.log( btn );
```
結果
```
a
```
## get()
引数にインデックスを取り、ひとつのDOMエレメントを参照する。
[![Image from Gyazo](https://i.gyazo.com/7711ddabcde386717266ecc3390b09e2.gif)](https://gyazo.com/7711ddabcde386717266ecc3390b09e2)
http://semooh.jp/jquery/api/core/get/index/

## submit()
submitの実行。もしくは関連付け。
http://js.studio-kingdom.com/jquery/events/submit#2
