## ヘッダーのプロファイルアイコン

一覧画面と入力画面のヘッダーにプロファイルアイコンは設けている。
このアイコンによりログインユーザの入力画面を開いて、自己情報
編集したり、パスワードをリセットしたりなどができる。もし自己
情報の修正は不都合の場合、定義設定によりアイコンを非表示させることは可能。

以下のJquery式で特定可能。
```
#{defId}_header td:eq(2) i.bi-person-circle
```

### ここだよ
一覧画面：[定義場所](https://efwgrp.github.io/ske/svg/header.profile.listPage.def.svg)、[利用場所](https://efwgrp.github.io/ske/svg/header.profile.listPage.svg)

入力画面：[定義場所](https://efwgrp.github.io/ske/svg/header.profile.inputPage.def.svg)、[利用場所](https://efwgrp.github.io/ske/svg/header.profile.inputPage.svg)
