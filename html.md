## nav
## section
## ul / li
## heightとwidhtの親子の受け渡し
## aタグの装飾
```
text-decoration: none;
```
これでリンク文字の下線がなくなる
```
text-decoration: underline;
```
これでリンク文字の下線を設定

## HTML&CSSでは「カーソルを当てたとき」のことをホバー時と呼んだりします。
```
img:hover {
 opacity: 0.7
}
```
imgにカーソルが乗った時にimgが半透明になる

## ::afterとか::beforeとか
> CSS の 疑似要素Pseudo-elementsはセレクターに付加するキーワードで、選択された要素の特定の部分にスタイル付けできるようにするものです。
https://developer.mozilla.org/ja/docs/Web/CSS/Pseudo-elements
https://developer.mozilla.org/ja/docs/Web/CSS/::after

floatを使う親要素に:afterを設定し、その親要素以下にfloatの影響を与えないようにする。
```
.parent:after {
  display: block;
  clear: both;
  content: "";
}
```
→上記で結果的に、親要素の最後にclear: both;が当たった空白の要素が追加される。この手法を、cleafixという。
http://creator.aainc.co.jp/archives/4721
共通要素として、下記を設定しておくと便利。「float使いそうだな」と思ったら、その親要素のクラス名にclearfixを与えれば便利。
```
.clearfix:after {
  display: block;
  clear: both;
  content: "";
}
```
