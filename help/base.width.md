## 部品の幅

一覧画面の場合、幅は100%固定で設定が必要ない。
入力画面の場合、幅の設定は入力エリアのサイズ調整に転用される。
入力ダイアログと選択ダイアログの場合、Jquery-UIのダイアログの幅にあたる。

部品の幅をプログラムで動的に値を設定することを推奨しないが、以下のクライアント
javaScriptを画面初期化のアドオンにevalで実行させるようにすれば対応可能になる。

```js
//入力画面の場合、下位divに対して設定する
var width=$("#USER_form>div>div").css("width");
$("#USER_form>div>div").css("width","500px");
//入力ダイアログの場合、ダイアログIDは{defId}_inputDialogになる
var width=USER_inputDialog.dlg.dialog("option","width");
USER_inputDialog.dlg.dialog("option","width","500px");
//と選択ダイアログの場合、ダイアログIDは{defId}_selectDialogになる
var title=USER_selectDialog.dlg.dialog("option","width");
USER_selectDialog.dlg.dialog("option","width","500px");
```
画面初期化のアドオンは以下のようにリストする。

- 一覧画面＞検索エリア＞[検索条件](condition.conds.md)
- 入力画面＞入力エリア＞[入力項目](input.fds.md)
- 入力ダイアログ＞入力エリア＞[入力項目](input.fds.md)
- 選択ダイアログ＞検索エリア＞[検索条件](condition.conds.md)

### ここだよ
入力画面：[定義場所](https://efwgrp.github.io/ske_image/svg/base.width.inputPage.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.width.inputPage.svg)

入力ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/base.width.inputDialog.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.width.inputDialog.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/base.width.selectDialog.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.width.selectDialog.svg)

