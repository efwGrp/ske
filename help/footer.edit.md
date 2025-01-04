## フッターエリアの編集ボタン

一覧画面と選択ダイアログのフッターエリアに編集ボタンを設けている。
編集ボタンにより[入力画面](part.inputPage.md)または[入力ダイアログ](part.inputDialog.md)を呼び出して、
呼び出し元部品の選択行データを表示する。
定義設定によりボタンを非表示させることは可能。

以下のJquery式で特定可能。
```
#{defId} #btnEdit
#{defId}_selectDialog_footer #btnEdit
```

編集をカスタマイズしたい場合、[CRUD前後イベントの設定](comm.beforeAfter.md)をご参考ください。

### ここだよ

一覧画面：[定義場所](https://efwgrp.github.io/ske/svg/footer.edit.listPage.def.svg)、[利用場所](https://efwgrp.github.io/ske/svg/footer.edit.listPage.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske/svg/footer.edit.selectDialog.def.svg)、[利用場所](https://efwgrp.github.io/ske/svg/footer.edit.selectDialog.svg)
