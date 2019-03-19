## config/database.yml
アプリケーションからデータベースを利用する時の設定を記述。

## db/schema.rb
これまで行われたマイグレートの履歴。現在のDBをそのまま再現するためのファイル。

## rake db:create
configディレクトリの中にあるdatabase.ymlを読み込み，そのファイルに基づいてデータベースを作成
mysql/SQliteなどの設定は、 `rails new アプリ名 -d データベース言語名` といった形で指定。

## rake db:migrate
db/migrateディレクトリの中にあるスクリプトファイルに基づいてデータベースにテーブルを作成する。

## rake db:seed
dbディレクトリ内にあるseed.rbファイルを実行してデータベースにデータを格納する。

## 外部キーとは
アソシエーションを組む際に使用。他テーブルとの関係を示す。
https://master.tech-camp.in/curriculums/1088

## rake db:reset
DBをdropして、現在の scheme をロードして DB を作り直す。

## rake db:migrate:reset
databaseを一度削除してもう一度作成し、db:migrate実行。

> 例えば、新しくマイグレートファイルを作成してマイグレートを実行した後、カラムのデータ型やオプション指定を修正したくなって、その作成したばかりのマイグレートファイル自体を修正してマイグレーションを新たに適用したい場合。
ここで、rake db:reset とやると、DB再作成が db/schema.rb をロードして行われるので、修正が適用されません。rake db:migrate:reset とやると、db/migrate/ 以下のファイルが全て実行されてマイグレートが行われるので、無事に修正が適用されてデータベースが作成される。

https://easyramble.com/difference-bettween-rake-db-migrate-reset.html

## カラムを追加するときは
```
rails g migration Addカラム名Toテーブル名 カラム名:データ型
rails generate migration AddPriceToProducts price:integer
```

## カラムを削除するときは
```
rails g migration Removeカラム名Fromテーブル名 カラム名:データ型
rails generate migration RemovePriceToProducts price:integer
```
