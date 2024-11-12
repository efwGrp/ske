## 部品のタイトル

一覧画面と入力画面の場合、html＞head＞titleタグ中の文字にあたる。
入力ダイアログと選択ダイアログの場合、Jquery-UIのダイアログのタイトルにあたる。

部品のタイトルをプログラムで動的に値を設定することを推奨しないが、以下のクライアント
javaScriptを画面初期化のアドオンにevalで実行させるようにすれば対応可能になる。

```js
//一覧画面と入力画面の場合、タイトルタグに対して操作する
var title=$("title").text();
$("title").text("new title");
//入力ダイアログの場合、ダイアログIDは{defId}_inputDialogになる
var title=USER_inputDialog.dlg.dialog("option","title");
USER_inputDialog.dlg.dialog("option","title","new title");
//と選択ダイアログの場合、ダイアログIDは{defId}_selectDialogになる
var title=USER_selectDialog.dlg.dialog("option","title");
USER_selectDialog.dlg.dialog("option","title","new title");
```
画面初期化のアドオンは以下のようにリストする。

- 一覧画面＞検索エリア＞[検索条件](condition.conds.md)
- 入力画面＞入力エリア＞[入力項目](input.fds.md)
- 入力ダイアログ＞入力エリア＞[入力項目](input.fds.md)
- 選択ダイアログ＞検索エリア＞[検索条件](condition.conds.md)

### ここだよ
一覧画面：[定義場所](https://efwgrp.github.io/ske_image/svg/base.title.listPage.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.title.listPage.svg)

入力画面：[定義場所](https://efwgrp.github.io/ske_image/svg/base.title.inputPage.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.title.inputPage.svg)

入力ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/base.title.inputDialog.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.title.inputDialog.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/base.title.selectDialog.def.svg)、[イメージ](https://efwgrp.github.io/ske_image/svg/base.title.selectDialog.svg)

