## ヘッダのタイトル

一覧画面と入力画面のヘッダに画面名称としてタイトルを表示している。

部品のタイトルをプログラムで動的に値を設定することを推奨しないが、以下のクライアント
javaScript、またはサーバjsで画面初期化のアドオンに実行させるようにすれば対応可能になる。

クライアントjs
```js
//一覧画面と入力画面の場合、タイトル位置を特定して操作する
var title=$("#USER_header td:eq(1)").text();//ヘッダは{defId}_headerになる
$("#USER_header td:eq(1)").text("ユーザ一覧 テスト");
```
サーバjs
```js
//一覧画面と入力画面の場合、タイトル位置を特定して操作する
return new Result()
	.runat("#USER_header")//ヘッダは{defId}_headerになる
	.withdata({
		"td:eq(1)":"ユーザ一覧 テスト"
	});
```

画面初期化のアドオンは以下のようにリストする。

- 一覧画面＞検索エリア＞[検索条件](condition.conds.md)
- 入力画面＞入力エリア＞[入力項目](input.fds.md)

### ここだよ
一覧画面：[定義場所](https://efwgrp.github.io/ske_image/svg/header.title.listPage.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/header.title.listPage.svg)

入力画面：[定義場所](https://efwgrp.github.io/ske_image/svg/header.title.inputPage.def.svg)、[利用場所](https://efwgrp.github.io/ske_image/svg/header.title.inputPage.svg)

