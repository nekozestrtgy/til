## フォントの設定
cssの書き方
英語、日本語の順番で指定。
https://saruwakakun.com/html-css/basic/font-family-how-to

googlefont  
サイトでスクリプト作って、cssに書く
https://saruwakakun.com/html-css/basic/google-fonts

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
## overflow: hidden;
> `overflow`プロパティは、ボックスの範囲内に内容が収まらない場合に、はみ出た部分の表示の仕方を指定する際に使用します。
http://www.htmq.com/css/overflow.shtml
> `hidden` 内容がボックスに収まらない場合、収まらない部分は非表示となる。内容が収まらない場合にも、スクロールバーなどは表示されない

## translateプロパティ
> http://www.htmq.com/css3/transform_translate.shtml

```
transform: translate(-50%, 0);
```
x軸報告に-50%、y軸方向に0移動
正の時は、x軸のプラス方向(つまり→)に、y軸のマイナス方向(つまり↓)に移動する。

## word-break: break-word;
単語単位で折り返してくれる。

## white-space: normal;
ソース中のホワイトスペースを無視
ソース中の改行を1つの半角スペースとして表示
ボックスサイズが指定されている場合にはそれに合わせて自動改行する（初期値）

## background: linear-gradient(to right, rgba(255,255,255,0), #fff 72%);
線形グラデーションを指定する際に使用。
```css
linear-gradient(グラデーションの角度または方向, 開始色, 途中色, 終了色);
```
## animation
javascript使わなくてもスライド的なデザインをcssで実装できるっぽい
https://lopan.jp/css-animation-slideshow/

animationは一方向の変化のみ。
transitionは双方向の変化が可能。
```css
.sample {
  animation: name,duration,timingfunction,delay,iterationcount,direction;
}
```

```css
div.sample {
  animation: anime1 5s ease -2s infinite alternate;
}

@keyframes anime1 {
0% {width: 50px; height: 50px; background-color: aqua;}
100% {width: 200px; height: 50px; background-color: blue;}
}
```

http://www.htmq.com/css3/animation.shtml

## transition
cssだけでアニメーションがつけられる。https://www.halawata.net/2011/10/css3-transition/
```
transition: background-color 2s ease-out 0.5s;
```
変化させるプロパティ、変化にかける時間、イージング、遅延させる時間の順で指定
> 「イージング」は
> ease（開始と終了が滑らか、初期値）
> linear（一定）
> ease-in（ゆっくり始まる）
> ease-out（ゆっくり終わる）
> ease-in-out（ゆっくり始まってゆっくり終わる）
> といったキーワード指定の他、cubic-bezier(数値, 数値, 数値, 数値)による数値指定も可能です。

## object-fit
```css
object-fit: cover;
width: 213px;
height: 213px;
```
これで、どんな大きさの画像でも短い辺を合わせるかたちで、213pxの正方形に画像の中央でトリミングして表示してくれる

## text-shadow
> text-shadowプロパティでは、スペース区切りで<水平方向の距離> <垂直方向の距離> <影のぼかし半径> <影の色>を指定することができます。 長さの値には、pxやemやexなどの単位が利用できます。

```css
text-shadow: 5px 5px 2px blue;
```
右5px下5px移動した先に半径2pxの青い影がつく
https://www.yoheim.net/blog.php?q=20121103

## ネガティブマージンなるものがあるらしい
https://coliss.com/articles/build-websites/operation/css/css-using-negative-margins.html

## text-align 
> 適用対象 ブロックコンテナ
pやhを含むブロック要素に対して当てる

## text-overflow
親要素にはいりきらない内容をどう表示させるのかを決める
```
text-overflow: ellipsis;
 
```

これで、はいりきらない部分は・・・で表示されるようになった。

## :focus
要素がフォーカスされた時のcssを指定できる擬似要素。
フォーカスについては以下。基本的には、フォームの入力欄でカーソルが点滅している状態などのこと。
http://e-words.jp/w/フォーカス.html

## ウィンドウ幅に対応した中央配置
ブロック要素の中にブロック要素を使い、中にだけwidthを設定すれば良い。
