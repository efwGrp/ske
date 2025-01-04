## CRUD前後イベントの設定

一覧画面と選択ダイアログは、検索ボタンを押す場合、SELECTを発行する。
入力画面と入力ダイアログは、新規モードを除いて初期化時、SELECTを発行する。
一覧画面と選択ダイアログは、削除ボタンを押す場合、DELETEを発行する。
入力画面と入力ダイアログは、保存ボタンを押す場合、INSERTあるいはUNPDATEを発行する。
これらのSELECT発行はメインテーブルまたはクエリに対するもので、実行前後にイベント挿入が可能。

SQL実行前のイベントは主に実行可否のチェック検索条件・保存値の加工のため。戻り値がある場合、チェックがパスできない意味にする。

SQL実行後のイベントは検索結果の加工またはほかの処理を行うため。専用の画面表示またはアクションが必要の場合戻り値で行う。

|イベント名|インタフェース|戻り値|
|-|-|-|
|検索前|function( condition, type ){ }|void \| Result|
|検索後|function( condition, aryData, type ){ }|void \| Result|
|削除前|function( [deleteConditionData](param.deleteConditionData.md) ){ }|void \| Result|
|削除後|function( [deleteConditionData](param.deleteConditionData.md) ){ }|void \| Result|
|保存前|function( [saveFormData](param.saveFormData.md) ){ }|void \| Result|
|保存後|function( [saveFormData](param.saveFormData.md) ){ }|void \| Result|

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>condition</td><td>Object</td><td>
searchタイプの場合<a href="param.searchConditionData.md">searchConditionData</a>を参照。
inputタイプの場合<a href="param.initFormData.md">initFormData</a>を参照。
</td></tr>
<tr><td>type</td><td>String</td><td>search | input</td></tr>
<tr><td>aryData</td><td>Array</td><td>
	<table>
	<tr><th>属性</th><th>説明</th></tr>
	<tr><td>obj</td><td>レコードオブジェクトのJSON文字列、選択ダイアログ戻り値用。</td></tr>
	<tr><td>primarykey</td><td>主キー項目配列のJSON文字列、検索結果の行特定用。</td></tr>
	<tr><td colspan=2>＜以下は<a href="comm.tableQuery.md">テーブル＆クエリ</a>の項目＞</td></tr>
	<tr><td>項目ID</td><td>値</td></tr>
	<tr><td>・・・</td><td>・・・</td></tr>
	</table>

</td></tr>
</table>

### ここだよ

[定義場所](https://efwgrp.github.io/ske/svg/comm.beforeAfter.svg)