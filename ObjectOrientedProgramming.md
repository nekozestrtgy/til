オブジェクトは、`情報`と`振る舞い`を持つ。
オブジェクト≒インスタンス≒実体
インスタンスは、クラスという設計図を元に作られる。
オブジェクトの`情報`と`振る舞い`は、設計図であるクラスに定義する。

### インスタンスフィールド
インスタンスの`情報`

### インスタンスメソッド
インスタンスの`振る舞い`
定義は設計図であるクラスに書いてあるが、実際に振る舞いを持つのはインスタンスである。


## カプセル化
使い手に必要ないものを隠すこと。
クラスの外でも使える機能は公開し、使って欲しくない機能はカプセル化を行いアクセスを制限する。
これにより、何かが壊れることを防ぐ。

## 継承
既存のクラスのフィールドやメソッドを別のクラスに引き継ぐこと。
継承されるクラスを`スーパークラス`、継承して新しくできるクラスを`サブクラス`と呼ぶ。

### 多態性
サブクラスのインスタンスは、スーパークラスのクラス型変数に代入することができる。
