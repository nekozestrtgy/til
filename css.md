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
