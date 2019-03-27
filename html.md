## nav
## section
## ul / li
## heightとwidhtの親子の受け渡し

## script
`src`で外部リソースを読み込み、ファイル内でリソースを使用することができる。

```html
<script type="text/javascript" src="https://js.pay.jp/"></script>
<script type="text/javascript">Payjp.setPublicKey('pk_test_0383a1b8f91e8a6e3ea0e2a9');</script>
```
`Payjp.setPublicKey`は外部リソース`https://js.pay.jp/`に記述されているメソッド。読み込みファイル内で定義されていなくても、使用することができる。

## input
`type属性`省略時は、`type = text`となる。
`type="hidden`を指定すると、 ブラウザ上に表示されない非表示データを送信することができる。valueで、送信する値を設定。

## select
セレクトボックスを作成するタグ。選択肢は`option`タグで指定。
http://www.htmq.com/html/select.shtml

## render
:paritalを使う時は、:localも使う。どっちかしか指定しない場合には、エラーになる。
https://qiita.com/mm36/items/2d89aa3b77e740e671c2

```
render partial: "相対パス", locals: {renders先の変数名: 値 }
```
```products_controller.rb
render partial: "middle_category", locals: {division: params[:middle_category]}
```
`products/_middle_category.html.haml`を`render`している。また、`params[:middle_category]`を`division`という名前の変数で渡している。

変数を繰り返して使用する際は、`collection`を使用すると便利。
```
= render partial: "テンプレート名", collection: (繰り返し表示させるインスタンス)
```
```article/index.html.haml
= render partial: "article", collection: @articles
```
```:article/_article.html.haml
%p
  articleのタイトルは、#{article.title}です
```
