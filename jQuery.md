## そもそもjqueryとは
javascriptのプラグイン。javascriptより簡単な記述が可能。
```
document.getElementById("test").innerHTML = "hello world!";
```
```
$("#test").text("hello world!");
``` 
上記２つは同じ内容。
http://www.jquerystudy.info/tutorial/intro/merit.html


## jqueryを使うには
基本的にはheadタグ内に以下のような記述が必要。
```
<script type="text/javascript" src="jquery-1.9.1.min.js"></script>
```
http://www.jquerystudy.info/tutorial/intro/merit.html

railsであれば、`jquery-rails`というgemを入れ、`application.js`に`//= require jquery`を記入することで使用することができる。ファイルの読み込みは
を記入することで使用することができる。
`application.html.erb`も確認。以下の記述がなければ追記。これを実行することでスクリプトファイルを読み込むためのスクリプトタグを自動的に生成してくれます。
```
<%= javascript_include_tag 'application', 'data-turbolinks-track': 'reload' %>
```

https://qiita.com/ngron/items/95846bd630a723e00038

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

## if()
```
if(条件式) {
  処理
} else if(条件式) {
  処理
} else {
  処理
}
```
```
$(function() {
 
  // 年齢を変数に格納
  var age = 65;
 
  // if文で条件を比較
  // 年齢が20歳未満だったら
  if (age < 20) {
 
    // コンソールに未成年と表示
    console.log('未成年です。');
 
   // 年齢が65歳以上だったら
  } else if (age >= 65) {
 // コンソールにシニアと表示
    console.log('シニアです。');
  // 年齢がそれ以外だったら
  } else {
    // コンソールに成人と表示
    console.log('成人です。');
  }
});

```
https://www.flatflag.nir87.com/if-2-1102

## セレクタの指定方法
http://www.hp-stylelink.com/news/2013/11/20131122.php
ある親要素内の子要素を指定するときは、`$('親要素 子要素')`で指定。
