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


## ローカルでrailsコマンド動かない時は、、、
gemfileの先頭と、.ruby-versionのバージョンを揃えて2.5.1にすると解決。


## bundle exec有りと無しの違い
有りの場合、そのRailsプロジェクトのGemfileで指定された環境で実行する事ができる
https://qiita.com/windhorn/items/0f58866291f8273f18fb
