## asset precompileでエラー
masterにマージしてるか確認。

## Uglifier::Error: Unexpected token: keyword (const). To use ES6 syntax, harmony mode must be enabled with Uglifier.new(:harmony => true).
`config/environments/production.rb` を以下に修正
```ruby
config.assets.js_compressor = :uglifier
↓
config.assets.js_compressor = Uglifier.new(harmony: true)
```
https://obel.hatenablog.jp/entry/20180530/1527672119

## Can't connect to local MySQL server through socket '/tmp/mysql.sock' (2)
リモートのディレクトリにsockファイルがないのが問題。
```
アプリ名 $ sudo touch /tmp/mysql.sock
```
ファイルを作成。
```
アプリ名 $ sudo service mysqld restart
```
mysql再起動すればオーケー。
https://qiita.com/carotene4035/items/e00076fe3990b9178cc0

