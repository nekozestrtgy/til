; = 「。」
セミコロンは「。」の役割。文の終わりに必ずつける。抜けがあると、処理が行われなくなる。

printlnは、プリントライン

### データ型
String 文字(Sは大文字)
int 数字(iは小文字)

### 変数の定義

```
(データ型) (変数名);
```
例
```
int number;
String name;
```

変数の定義と同時に、値を代入することもできる。これを、変数の初期化と言う。
````
int number = 3;
String name = "Hello World";
```

変数の値を上書きするときは、データ型をつけない。データ型をつけると、新しい変数を定義することになってしまう。同じ名前の変数は定義できない。
```
//good
int number = 3;
number = 5;

//error
int number = 3;
int number = 5;
```

変数名には、キャメルケースを用いる。
```
//good
userName

//error or bad
1name 数字開始
user_name スネークケース
namae ローマ字
名前 日本語
```


### 計算
````
int number = 1;

//以下全部同じ意味
number = number + 1;
number += 1;
number++; //足す値が1の時はこう書ける。
```
