; = 「。」
セミコロンは「。」の役割。文の終わりに必ずつける。抜けがあると、処理が行われなくなる。

printlnは、プリントライン

### データ型
String 文字(Sは大文字)
int 数字(iは小文字)
double 小数
boolean 真偽値

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
```
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
```
int number = 1;

//以下全部同じ意味
number = number + 1;
number += 1;
number++; //足す値が1の時はこう書ける。
```

int型同士の計算は、int型で出力される。
```
println(5/2);
//→2
```
int型とdouble型だと、double型で出力される。
```
pringln(5.0/2);
//→2.5
```

### キャスト
キャストとは、強制的に型変換を行うこと。
```
println((double)7 / 2;
//→3.5　double型で出力される。
```
この場合、7のデータ型がdoubleに変換され、double型とint型の計算で、double型が出力される。

### 比較演算子
```
x == y →xとyが等しい時true
x != y →xとyが等しくない時true
x >= y →xがy以上の時true
```
`&&`や`||`など、複雑な論理演算子を用いた範囲の時は、図で数直線を書いて考えるとわかりやすい。

### 条件分岐
```
if (条件) {
  (処理);
}
```
ブロック`{}`の後ろには、`;`不要

### switch文
`xが２と一致する時`などの条件を使用する時に、if文より簡潔に記述ができる。
```
switch (条件) {
  case 値1:
    処理;
    break;
  case 値2:
    処理;
    break;
  case 値3:
    処理;
    break;
}
```
値の後ろには`:`を忘れない。また処理の後には`break`を書かないと次の処理が実行されてしまうので忘れない。