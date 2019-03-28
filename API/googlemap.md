## 導入方法
https://qiita.com/Haruka-Ogawa/items/997401a2edcd20e61037

## You have exceeded your request quota for this APIが出た時は
請求先情報をgoogle consoleで登録する。
https://blog.goga.co.jp/2018/07/you-have-exceeded-your-request-quota.html


## Uncaught ReferenceError: google is not definedが出た時は
jsファイルを読み込む位置を、`title`のすぐ下にするとうまくいくことが多い。
https://none53.hatenablog.com/entry/20130125/1359112767

## svgをmarkerで使用する際のアンカー
基準は左上。(横、縦)の順で指定。横がプラスだとx軸マイナス方向(つまり左)、縦がプラスだとy軸プラス方向(つまり上)に動く。svgファイルをchromeとかで開き、widthとheightを確認してアンカーの位置を調整するとうまくいく。
https://lab.syncer.jp/Web/API/Google_Maps/JavaScript/Symbol/
https://cotodama.co/google-maps-apimarker_marker/
