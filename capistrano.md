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
