## 追加ボタン

各エリアに追加ボタンの設定があり、まとめて説明する。

定義内容は以下のようにリストする。
<table>
<tr><th>項目</th><th>説明</th></tr>
<tr><td>ID</td><td>部品内でユニークな識別子。</td></tr>
<tr><td>タイトル</td><td>ボタンの表示ラベル。</td></tr>
<tr><td>アイコン</td><td>Bootstrap Iconsのcss設定。</td></tr>
<tr><td>確認メッセージ</td><td>クリックの場合、設定される確認メッセージを表示し、OKの場合処理を継続する。</td></tr>
<tr><td>ボタン処理</td><td>
<table>
	<tr><th>部品</th><th>インタフェース</th><th>戻り値</th></tr>
	<tr><td>一覧画面</td>
		<td rowspan=2>function( <a href="param.touchConditionData.md">touchConditionData</a> ){ }</td><td rowspan=4><a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a></td>
	<tr><td>検索ダイアログ</td></tr>
	<tr><td>入力画面</td>
		<td rowspan=2>function( <a href="param.touchFormData.md">touchFormData</a> ){ }</td>
	<tr><td>入力ダイアログ</td></tr>
</table>
</td></tr>
</table>

