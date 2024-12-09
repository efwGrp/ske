## ダウンロードダイアログ

ダウンロードダイアログは標準部品の一つ。
標準利用は、一覧画面のダウンロードボタンで呼び出して、ダウンロードのテンプレートを選んで出力する。
テンプレートは、CSVとリポジトリ定義の一覧画面タブで登録されたExcelファイルで構成される。

<table>
<tr><th>テンプレート</th><th>説明</th></tr>
<tr><td>CSV（テーブル項目）</td><td>
一覧画面の検索条件に従う検索結果の出力。テーブル＆クエリ項目のビュー項目は出力から除外する。
</td></tr>
<tr><td>CSV（クエリ項目）</td><td>
一覧画面の検索条件に従う検索結果の出力。テーブル＆クエリ項目の全項目を含む。
</td></tr>
<tr><td>Excel（一覧用）{excelFileName}</td><td>
一覧画面の検索条件に従う検索結果の出力。テーブル＆クエリ項目の全項目を含む。
Excelテンプレートの「data」シートに出力し、表示用シートは「data」シートからリンクして利用する。
</td></tr>
<tr><td>Excel（単票用）{excelFileName}</td><td>
一覧画面の検索条件に従う検索結果に、選択行のデータのみを出力する。
テーブル＆クエリ項目の全項目を含む。
Excelテンプレートの「data」シートに出力し、表示用シートは「data」シートからリンクして利用する。
選択行１件ずつ出力Excelを作成する。
</td></tr>
</table>

ダウンロードボタンではない箇所から利用したい場合、以下のAPIをご参考ください。

<table>
<tr><th>メソッド名</th><th>インタフェース</th><th>戻り値</th><th>備考</th></tr>
<tr><th>呼び出し</th></tr>
<tr><td>開く</td><td>downloadDialog.open ( defId, selectIds )</td><td>void</td><td></td></tr>
<tr><th>フッター</th></tr>
<tr><td>ダウンロード</td><td>downloadDialog.download ( )</td><td>void</td><td></td></tr>
<tr><td>閉じる</td><td>downloadDialog.close ( )</td><td>void</td><td></td></tr>
</table>

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>defId</td><td>String</td><td>リポジトリ定義ID。</td></tr>
<tr><td>selectIds</td><td>Array</td><td>選択行の主キー配列のJSON文字列の配列。

```
//主キー配列のJSON文字列
[
	"[\"PK1_1\",\"PK1_2\"]",
	"[\"PK2_1\",\"PK2_2\"]",
	"[\"PK3_1\",\"PK3_2\"]"
]
```
</td></tr>
</table>
