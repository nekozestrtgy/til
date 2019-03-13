## どこに書けば良いの？
application.jsに
```
= require_tree .
```
の記述があれば、app/javascript直下のどのファイルに処理を書いても良い。
app/assets/javascriptsディレクトリ以下のjsファイルをすべて読み込むという意味。
