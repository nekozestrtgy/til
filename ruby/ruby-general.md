## render
部分テンプレート(_abcd.html.hamlとか)を読み込む時に使用する。
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

## スコープ演算子
:: メソッドを使用する環境（=名前空間）を指定することができる。

[![Image from Gyazo](https://i.gyazo.com/35f16210aaa87cb000988a324e998f50.png)](https://gyazo.com/35f16210aaa87cb000988a324e998f50)

## require
gemを外部ファイルを読み込む時に使用。
> bundlerはデフォルトで、Gem自身の名前を持つファイルをrequireするようになっている。  
そうじゃない使用のgemは、使いたいファイルの頭にrequireをつける必要がある。
```
require 'gemの名前'
```
```
require '相対パス（./abc.scssとか）'
```
https://teratail.com/questions/109039
https://www.sejuku.net/blog/16111

## bundler
gemのバージョン管理やインストールを行うgem
https://qiita.com/hisonl/items/162f70e612e8e96dba50

## params
inputのnameを元に

## コントローラーの作成
`rails generate controller コントローラ名`
