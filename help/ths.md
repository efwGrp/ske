## 検索結果

一覧画面と選択ダイアログは、検索結果の表示列を設定できる。

定義内容は以下のようにリストする。
<table>
<tr><th>項目</th><th>説明</th></tr>
<tr><td>タイトル</td><td>検索結果列ヘッダの表示内容。</td></tr>
<tr><td>幅</td><td>列の幅。未定義は自動調整。</td></tr>
<tr><td>列ソート項目</td><td>列ヘッダ押下時のソート処理に利用するテーブル項目。
<a href="comm.fields.md">テーブル＆クエリ項目</a></td></tr>
<tr><td>初期ソート順</td><td>初期表示時のソート処理に利用する列ソート項目を表記する。ASC | DESC</td></tr>
<tr><td>SQLSelect</td><td>列の表示内容にマッピングするテーブル項目。
<a href="comm.fields.md">テーブル＆クエリ項目</a></td></tr>
<tr><td>揃え</td><td>列の揃え。left | center | right 未定義の場合leftと同じ取り扱い。</td></tr>
<tr><td>フォーマット</td><td>数字と日付項目の表示フォーマット。
例：#,##0.0　yyyy/MM/dd HH:mm　
参考：<a href="https://github.com/efwGrp/efw4.X/blob/master/help/formatter&rounder.md">formatter&rounder</a>
変換処理を登録可能。インタフェースは以下。
	<table>
	<tr><th>部品</th><th>インタフェース</th></tr>
	<tr><td>一覧画面</td><td rowspan=2>String | function(data){}</td></tr>
	<tr><td>検索ダイアログ</td></tr>
</td></tr>
</table>

以下のJquery式で特定可能。
```
${defId} .MAIN-TABLE TH:nth-child(n),${defId} .MAIN-TABLE TD:nth-child(n)
${defId}_selectDialog .MAIN-TABLE TH:nth-child(n),${defId}_selectDialog .MAIN-TABLE TD:nth-child(n)
```
選択結果列はIDがないから、順番nで特定する。1番目列はシステム用なので、2からスタートしてください。

### ここだよ
一覧画面：[定義場所](https://efwgrp.github.io/ske/svg/ths.listPage.def.svg)、
[利用場所](https://efwgrp.github.io/ske/svg/ths.listPage.svg)

選択ダイアログ：[定義場所](https://efwgrp.github.io/ske/svg/ths.selectDialog.def.svg)、
[利用場所](https://efwgrp.github.io/ske/svg/ths.selectDialog.svg)

