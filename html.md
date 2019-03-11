## nav
## section
## ul / li
## heightとwidhtの親子の受け渡し

## script
`src`で外部リソースを読み込み、ファイル内でリソースを使用することができる。

```html
<script type="text/javascript" src="https://js.pay.jp/"></script>
<script type="text/javascript">Payjp.setPublicKey('pk_test_0383a1b8f91e8a6e3ea0e2a9');</script>
```
`Payjp.setPublicKey`は外部リソース`https://js.pay.jp/`に記述されているメソッド。読み込みファイル内で定義されていなくても、使用することができる。

