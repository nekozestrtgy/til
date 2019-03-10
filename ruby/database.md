## config/database.yml
アプリケーションからデータベースを利用する時の設定を記述。

## rake db:create
configディレクトリの中にあるdatabase.ymlを読み込み，そのファイルに基づいてデータベースを作成
mysql/SQliteなどの設定は、 `rails new アプリ名 -d データベース言語名` といった形で指定。

## rake db:migrate
db/migrateディレクトリの中にあるスクリプトファイルに基づいてデータベースにテーブルを作成する。

## rake db:seed
dbディレクトリ内にあるseed.rbファイルを実行してデータベースにデータを格納する。
