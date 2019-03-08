## rubyのバージョンを設定する

現在のバージョンの確認
```
$ ruby --version
ruby 2.1.1p76 (2014-02-24 revision 45161) [x86_64-darwin12.0]

```

インストール済みのバージョンの確認
```
$ rbenv versions
  system
  2.0.0-p195
* 2.1.1 (set by /Users/user_name/.rbenv/version)
```

rbenvでインストールできるrubyのバージョンを確認
```
$ rbenv install -l
Available versions:
  1.8.6-p383
  1.8.6-p420
  1.8.7-p249
  1.8.7-p302
  1.8.7-p334
  .
  .
```
### インストールしたいバージョンがリストにない場合
```
$ brew update
$ brew upgrade rbenv ruby-build
```
もう一度確認
```
$ rbenv install -l
Available versions:
  1.8.6-p383
  1.8.6-p420
  1.8.7-p249
  1.8.7-p302
  1.8.7-p334
  .
  .
  .
  2.1.5
```

### インストール
```
$ rvenb install 2.1.5
Downloading ruby-2.1.5.tar.gz...
-> http://dqw8nmjcqpjn7.cloudfront.net/4305cc6ceb094df55210d83548dcbeb5117d74eea25196a9b14fa268d354b100
Installing ruby-2.1.5...
Installed ruby-2.1.5 to /Users/user_name/.rbenv/versions/2.1.5
```
確認
```
$ rbenv versions
  system
  2.0.0-p195
* 2.1.1 (set by /Users/user_name/.rbenv/version)
  2.1.5
```
インストールしたバージョンに変更
```
$ rbenv local 2.1.5
```
確認
```
$ rbenv --version
ruby 2.1.5p273 (2014-11-13 revision 48405) [x86_64-darwin12.0]
```

### 動かない場合
```
$ rbnev exec gem install bundle
```

### 参考
https://qiita.com/_am_/items/c1dbeb11f40bbbac8fd9
