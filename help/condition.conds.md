## 検索エリアの検索条件

一覧画面と選択ダイアログの検索エリアに
検索条件を設定できる。

定義内容は以下のようにリストする。
<table>
<tr><th>項目</th><th>説明</th></tr>
<tr><td colspan=2><a href="fds.md">入力項目の共通定義</a></td></tr>
<tr><td>SQLWhere</td><td>検索条件の部分SQL。該当条件入力の場合メインSQLに組込む。※１</td></tr>
<tr><td>クリア可否</td><td>クリアボタンを押す場合、該当条件の入力値を空白にするか否か。</td></tr>
</table>

※１、検索条件は、テーブル＆クエリ項目と入力値の判断式にする。以下は例。
like in between end not などWhere句に利用できる要素を分割して登録してください。
```sql
"ユーザID" =:condユーザID
```
### ここだよ
一覧画面：[定義場所](https://efwgrp.github.io/ske_image/svg/condition.conds.listPage.def.svg)、
[利用場所](https://efwgrp.github.io/ske_image/svg/condition.conds.listPage.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske_image/svg/condition.conds.selectDialog.def.svg)、
[利用場所](https://efwgrp.github.io/ske_image/svg/condition.conds.selectDialog.svg)

