## render
https://qiita.com/shizuma/items/1c655dadd2e04b3990a8

```
render partial: "post", locals: {bgcolor: "lightsteelblue", post: post}
```
上記では、`bgcolor`に`"lightsteelblue"`を、`post`に`post`を代入して、`_post.html`を呼び出している。

```
parial: "_ファイル名のファイル名部分"
locals: {ローカル変数名: "代入する値", ローカル変数名: インスタンス変数}
collection: （繰り返し使うインスタンス）
as: ローカルで使う変数の別名
```
asはローカルの変数を代入する変数とは別名で使用する際に使用する。