## フッターエリアの選択ボタン

選択ダイアログのフッターエリアに選択ボタンを設けている。
選択ボタンにより検索結果の選択行を前画面に渡す。
定義設定によりボタンを非表示させることは可能。

以下のJquery式で特定可能。
```
#{defId}_selectDialog_footer #btnSelect
```

選択結果の受け取りは、「タイトル操作」と「ボタン処理」などのアドオン関数にクライアントjavaScriptで対応する。
以下の例をご参考ください。
```js
function(formData){
  //戻り値のResultは画面表示と動作になり、必要に応じて設けることが可能。
  return (new Result()).eval(`
    USER_selectDialog.open({
      runat:"#K005_inputDialog",
      map:{
        "#fd承認社員番号":"ユーザid",
        "#fd社員名":"ユーザ名",
      }
    });
  `);
}
```

### ここだよ

[定義場所](https://efwgrp.github.io/ske_image/svg/footer.select.selectDialog.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/footer.select.selectDialog.svg)
