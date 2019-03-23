## rubyのバージョン確認
```
$ ruby -v
```

## gemのバージョン確認
```
$ gem -v
```

## railsのバージョン確認
```
$ rails -v
```

## gitのバージョン確認
```
$ git --version
```

qiita.com/Matteneko3/items/b2ad0caa6cb792c03649


## rubyとrailsの最新バージョンをダウンロードする
### ruby最新バージョンのインストール
```
#rbenvとruby-buildを更新
$ brew update && brew upgrade ruby-build

#最新のrubyバージョンが出てくるか確認
$ rbenv install -l

#最新のrubyをインストール
$ rbenv install (最新バージョン)
```
### rails最新バージョンのインストール
```
$ gem install rails

# "rbenv exec"＝「rbenvの設定で現在有効なrubyのbundler」をインストール
$ rbenv exec gem install bundler
```
https://qiita.com/rry/items/12d794437cde733f8ece

