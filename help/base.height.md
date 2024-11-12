## 部品の高さ

一覧画面の場合、高さは100%固定で設定が必要ない。
入力画面の場合、高さの設定は入力エリアのサイズ調整に転用される。
入力ダイアログと選択ダイアログの場合、Jquery-UIのダイアログの高さにあたる。

部品の高さをプログラムで動的に値を設定することを推奨しないが、以下のクライアント
javaScriptを画面初期化のアドオンにevalで実行させるようにすれば対応可能になる。

```js
//入力画面の場合、下位divに対して設定する
var width=$("#USER_form>div>div").css("height");
$("#USER_form>div>div").css("height","500px");
//入力ダイアログの場合、ダイアログIDは{defId}_inputDialogになる
var width=USER_inputDialog.dlg.dialog("option","height");
USER_inputDialog.dlg.dialog("option","height","500px");
//と選択ダイアログの場合、ダイアログIDは{defId}_selectDialogになる
var title=USER_selectDialog.dlg.dialog("option","height");
USER_selectDialog.dlg.dialog("option","height","500px");
```
画面初期化のアドオンは以下のようにリストする。

- 一覧画面＞検索エリア＞[検索条件](condition.conds.md)
- 入力画面＞入力エリア＞[入力項目](input.fds.md)
- 入力ダイアログ＞入力エリア＞[入力項目](input.fds.md)
- 選択ダイアログ＞検索エリア＞[検索条件](condition.conds.md)

### ここだよ
入力画面：[定義場所](https://efwgrp.github.io/ske_image/svg/base.height.inputPage.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.height.inputPage.svg)

入力ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/base.height.inputDialog.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.height.inputDialog.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/base.height.selectDialog.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.height.selectDialog.svg)

