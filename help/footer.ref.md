## フッターエリアの参照ボタン

一覧画面と選択ダイアログのフッターエリアに参照ボタンを設けている。
参照ボタンにより[入力画面](part.inputPage.md)または[入力ダイアログ](part.inputDialog.md)を呼び出して、
呼び出し元部品の選択行データを表示して、入力不可に設定する。
定義設定によりボタンを非表示させることは可能。

以下のJquery式で特定可能。
```
#{defId} #btnRef
#{defId}_selectDialog_footer #btnRef
```

参照をカスタマイズしたい場合、[CRUD前後イベントの設定](comm.beforeAfter.md)をご参考ください。

### ここだよ

一覧画面：[定義場所](https://efwgrp.github.io/ske_image/svg/footer.ref.listPage.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/footer.ref.listPage.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/footer.ref.selectDialog.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/footer.ref.selectDialog.svg)
