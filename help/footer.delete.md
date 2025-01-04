## フッターエリアの削除ボタン

一覧画面と選択ダイアログのフッターエリアに削除ボタンを設けている。
削除ボタンにより選択行データを削除する。
定義設定によりボタンを非表示させることは可能。

以下のJquery式で特定可能。
```
#{defId} #btnDelete
#{defId}_selectDialog_footer #btnDelete
```

削除をカスタマイズしたい場合、[CRUD前後イベントの設定](comm.beforeAfter.md)をご参考ください。

### ここだよ

一覧画面：[定義場所](https://efwgrp.github.io/ske/svg/footer.delete.listPage.def.svg)、[利用場所](https://efwgrp.github.io/ske/svg/footer.delete.listPage.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske/svg/footer.delete.selectDialog.def.svg)、[利用場所](https://efwgrp.github.io/ske/svg/footer.delete.selectDialog.svg)
