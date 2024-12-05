## フッターエリアのコピー新規ボタン

一覧画面と選択ダイアログのフッターエリアにコピー新規ボタンを設けている。
コピー新規ボタンにより入力画面または入力ダイアログを呼び出して、呼び出し元部品の選択行データを表示して、主キーをクリアする。
定義設定によりボタンを非表示させることは可能。

以下のJquery式で特定可能。
```
#{defId} #btnCopyAdd
#{defId}_selectDialog_footer #btnCopyAdd
```

新規をカスタマイズしたい場合、[CRUD前後イベントの設定](comm.beforeAfter.md)をご参考ください。

### ここだよ

一覧画面：[定義場所](https://efwgrp.github.io/ske_image/svg/footer.copyAdd.listPage.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/footer.copyAdd.listPage.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/footer.copyAdd.selectDialog.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/footer.copyAdd.selectDialog.svg)
