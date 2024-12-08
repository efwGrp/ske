## ダウンロードダイアログ

ダウンロードダイアログは標準部品の一つ。
標準利用は、一覧画面のダウンロードボタンで呼び出して、ダウンロードの種類を選んで出力する。

ダウンロードボタンではない箇所から利用したい場合、以下のAPIをご参考ください。

<table>
<tr><th>メソッド名</th><th>インタフェース</th><th>戻り値</th></tr>
<tr><td>開く</td><td>downloadDialog.open ( defId, selectIds )</td><td>void</td></tr>
<tr><td>閉じる</td><td>downloadDialog.close ( )</td><td>void</td></tr>
<tr><td>選択</td><td>downloadDialog.download ( )</td><td>void</td></tr>
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
