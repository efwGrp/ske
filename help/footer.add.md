## フッターエリアの新規ボタン

一覧画面と選択ダイアログのフッターエリアに新規ボタンを設けている。
新規ボタンにより[入力画面](part.inputPage.md)または[入力ダイアログ](part.inputDialog.md)を呼び出す。
定義設定によりボタンを非表示させることは可能。

以下のJquery式で特定可能。
```
#{defId} #btnAdd
#{defId}_selectDialog_footer #btnAdd
```

新規をカスタマイズしたい場合、[CRUD前後イベントの設定](comm.beforeAfter.md)をご参考ください。

### ここだよ

一覧画面：[定義場所](https://efwgrp.github.io/ske_image/svg/footer.add.listPage.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/footer.add.listPage.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/footer.add.selectDialog.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/footer.add.selectDialog.svg)
