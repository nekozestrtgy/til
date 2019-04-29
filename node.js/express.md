## 基本的な使い方
https://qiita.com/nkjm/items/723990c518acfee6e473

>1. モジュールをロードしてインスタンス化。
>2. ポート番号を指定して待ち受け開始。
>3. アプリケーションの処理を記述。

```js
/*1.expressモジュールをロードし、インスタンス化してappに代入。*/
var express = require("express");
var app = express();

/*2. listen()メソッドを実行して3000番ポートで待ち受け。*/
var server = app.listen(3000, function(){
  console.log("Node.js is listening to PORT:" + server.address().port );
});

/*3. 以後、アプリケーション固有の処理*/
//写真のサンプルデータ
var photoList = [
  {
    id: "001",
    name: "photo001.jpg",
    type: "jpg",
    dataUrl: "hogehoge"
  }
]

//写真リストを取得するAPI
app.get("/api/photo/list", function(req, res, next) {
  res.json(photoList);
});
```
この例では、写真リストを提供するAPIを記述している。 `/api/photo/list` にアクセスした際、写真のサンプルデータすべてをJSON形式で返す仕様になっています。

## middleware
には、大きくappレベルとrouteレベルがある。
appレベルは、どのルーティングでも適用するmiddleware。app.use(〜となる。
routerレベルは、特定のルーティングで適用するmiddlewar。router.get(〜などになる。
https://expressjs.com/ja/guide/using-middleware.html


## express-generator
routesが、railsで言うcontrollerのような役割。どのパスでどんな処理を行うのか記述。
https://qiita.com/moomooya/items/00f89e425a3034b8ea14


## app.js
が、railsで言うroute.rb的な要素を担っているっぽい。
`var indexRouter = require('./routes/index');` でパスを変数に定義して、
`app.use('/', indexRouter);`でルーティング、的な。
実際の処理内容は、`routes`以下の書くファイルに記述する感じ。`routes`がrailsでいうcontroller。
上記の場合は、`index.js`に処理の記述がある。
