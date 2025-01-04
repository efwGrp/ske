## ヘッダーの追加アイコン

一覧画面と入力画面のヘッダーにプロファイルアイコンの左側に
複数の追加アイコンを設定できる。

定義内容は以下のようにリストする。
|項目|説明|
|-|-|
|ID|アイコンID。未設定の場合自動採番。※１|
|タイトル|アイコンのツールチップ表示。|
|リンク|遷移先ページ。[内部ページ一覧](pages.md)|
|ターゲット|空白：自タブ遷移、_blank：別タブを開く。|
|アイコン|Bootstrap Iconsのcss設定。|

※１、IDは部品内でユニークする必要。

以下のJquery式で特定可能。
```
#{defId} #{iconId}
```

### ここだよ
一覧画面：[定義場所](https://efwgrp.github.io/ske/svg/header.icos.listPage.def.svg)、
[利用場所](https://efwgrp.github.io/ske/svg/header.icos.listPage.svg)

入力画面：[定義場所](https://efwgrp.github.io/ske/svg/header.icos.inputPage.def.svg)、
[利用場所](https://efwgrp.github.io/ske/svg/header.icos.inputPage.svg)

