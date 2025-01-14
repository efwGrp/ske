## テーブル＆クエリ項目の設定

後続の設定に利用するため、テーブルまたはクエリの項目を定義する。
項目の保存値は、画面取得ではない場合、モード別に設定できる。

<table>
	<tr><th>項目</th><th>説明</th></tr>
	<tr><td>項目</td><td>テーブルまたはクエリの項目名。※１</td></tr>
	<tr><td>役割</td><td>
		以下の役割を設定できる。
		<table>
			<tr><th>項目</th><th>説明</th></tr>
			<tr><td>[空白]</td><td>一般項目。</td></tr>
			<tr><td>排他制御キー</td><td>更新日時、保存時先勝ちで排他。</td></tr>
			<tr><td>削除フラグ</td><td>0/1の文字フラグ、1：削除済み、0 or Null：未</td></tr>
			<tr><td>ビュー項目</td><td>保存不要項目。</td></tr>
		</table>
	</td></tr>
	<tr><td>タイプ</td><td>項目のデータタイプを表す。CSVアップロー機能を利用する場合、数字と日付に対して設定する必要。</td></tr>
	<tr><td>各モードの設定値</td><td>
		以下の各モードの保存時、保存値を設定できる。
		<table>
			<tr><th>モード</th><th>説明</th><th>設定値</th></tr>
			<tr><td>add</td><td>新規</td><td>null | 固定値 | function( <a href="param.saveFormData.md">saveFormData</a> ){ }</td></tr>
			<tr><td>copyAdd</td><td>コピー新規</td><td>null | 固定値 | function( <a href="param.saveFormData.md">saveFormData</a> ){ }</td></tr>
			<tr><td>edit</td><td>編集</td><td>null | 固定値 | function( <a href="param.saveFormData.md">saveFormData</a> ){ }</td></tr>
		</table>
		関数の場合、関数の戻り値を利用する。
		未設定(undefined)の場合、画面取得可能であれば画面値を利用する。
		サンプル　※２
	</td></tr>
</table>

※１：名称に特殊文字を含む場合、各DBのSQL規則に従ってコーテーションをつけてください。
```sql
--postgreSqlの場合、特殊文字を含むエンティティ名はダブルクォーテーションで囲む
"ユーザID"
```

※２：各モードの設定値のサンプル。
```js
//例１、新規の場合１、コピー新規の場合１、編集の場合自動。
{"add": 1,"copyAdd": 1}
//例２、新規の場合システム日付、コピー新規の場合システム日付、編集の場合自動。
{"add": function(){return new Date();},"copyAdd": function(){return new Date();}}

```

### ここだよ

[定義場所](https://efwgrp.github.io/ske/svg/comm.fields.svg)