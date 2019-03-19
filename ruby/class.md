## super
特殊なメソッド。スーパークラスのメソッドがサブクラスでオーバーライドされた場合に、スーパークラスのメソッドを明示的に呼び出すことができる。

```test.rb
class Car
  def accele
    print("アクセルを踏みました¥n")
  end
end

class Soarer < Car
  def accele
    super
    print("加速しました¥n")
  end
end

soarer = Soarer.new
soarer.accele


soarer = Soarer.new
soarer.accele
```
実行結果
```:実行結果
アクセルを踏みました
加速しました
```

https://www.javadrive.jp/ruby/inherit/index3.html
