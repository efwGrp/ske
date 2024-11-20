## ヘッダーの追加リンク

一覧画面と入力画面のヘッダーと検索条件の間に
複数の追加リンクを設定できる。

定義内容は以下のようにリストする。
|項目|説明|
|-|-|
|ID|リンクID。未設定の場合自動採番。※１|
|タイトル|リンクのラベル表示。|
|リンク|遷移先ページ。[内部ページ一覧](pages.md)|
|ターゲット|空白：自タブ遷移、_blank：別タブを開く。|

※１、IDは部品内でユニークする必要。

以下のJquery式で特定可能。
```
#{defId} #{linkId}
```
### ここだよ
一覧画面：[定義場所](https://efwgrp.github.io/ske_image/svg/header.lnks.listPage.def.svg)、
[利用場所](https://efwgrp.github.io/ske_image/svg/header.lnks.listPage.svg)

入力画面：[定義場所](https://efwgrp.github.io/ske_image/svg/header.lnks.inputPage.def.svg)、
[利用場所](https://efwgrp.github.io/ske_image/svg/header.lnks.inputPage.svg)

