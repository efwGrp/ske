## 添付ダイアログ

添付ダイアログは標準部品の一つ。
標準利用は、一覧画面から検索結果の選択行に対して添付ファイルを追加すること。
標準利用の場合、一覧画面の[インポートダイアログ](base.imports.md)に「attachDialog」を登録して、
フッターエリアに添付ボタン非表示を外して、一覧画面フッターの添付ボタンから呼び出す可能になる。

添付ボタンではない箇所から利用したい場合、以下のAPIをご参考ください。

<table>
<tr><th>メソッド名</th><th>インタフェース</th><th>戻り値</th><th>備考</th></tr>
<tr><th>呼び出し</th></tr>
<tr><td>開く</td><td>attachDialog.open ( home, readOnly, selectCallbck, closeCallback )</td><td>void</td><td></td></tr>
<tr><th>フッター</th></tr>
<tr><td>選択</td><td>attachDialog.select ( )</td><td>void</td><td></td></tr>
<tr><td>閉じる</td><td>attachDialog.close ( )</td><td>void</td><td></td></tr>
</table>

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>home</td><td>String</td><td>Storageフォルダからの相対パス。</td></tr>
<tr><td>readOnly</td><td>Boolean</td><td>true：編集可、false：読取り専用。</td></tr>
<tr><td>selectCallbck</td><td>function ( filename )</td><td>選択コールバック。
設定される場合、選択ボタンが表示する。
選択ボタンを押す場合、選択されたファイルのパスと名称をfilename引数として
選択コールバックに渡して実行する。</td></tr>
<tr><td>closeCallback</td><td>function ( )</td><td>閉じるコールバック。設定される場合、
添付ダイアログを閉じる前実行する。
</td></tr>
</table>
