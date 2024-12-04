## 入力項目の共通定義

検索エリアの検索条件と入力エリアの入力項目は、
ほとんどの設定内容が同じだから、まとめて説明する。

<table>
<tr><th>項目</th><th>説明</th></tr>
<tr><td>ID</td><td>項目ID、部品内ユニークな識別子。</td></tr>
<tr><td>タイトル</td><td>
表示ラベル。文字列または初期化処理を登録可能。
初期化処理関数のインタフェースは以下。
<table>
	<tr><th>部品</th><th>インタフェース</th><th>戻り値</th><th>formDataタイプ</th></tr>
	<tr><td>一覧画面</td><td>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td><td><a href="param.initConditionData.md">initConditionData</a></td></tr>
	<tr><td>入力画面</td><td>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td><td><a href="param.initFormData.md">initFormData</a></td></tr>
	<tr><td>入力ダイアログ</td><td>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td><td><a href="param.initFormData.md">initFormData</a></td></tr>
	<tr><td>検索ダイアログ</td><td>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td><td><a href="param.initConditionData.md">initConditionData</a></td></tr>
</table>
タイトルの文字列にhtmlタグを取り込んで、さらに鮮やかの表現ができる。※１
</td></tr>
<tr><td>タイプ</td><td>
<table>
	<tr><th>項目種類</th><th>説明</th><th>最大値</th><th>最小値</th><th>最大文字数</th><th>ソース</th>
	<th>タイトル幅</th><th>入力枠幅</th><th>入力枠高さ</th><th>値</th><th>編集不可</th>
	<th>タイトル操作</th><th>入力枠操作</th></tr>
	<tr><td>text</td><td>単一行テキストの入力欄</td>					<td>-</td><td>-</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>password</td><td>入力値を隠す単一行テキストの入力欄</td>	<td>-</td><td>-</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>textarea</td><td>テキストエリア</td>						<td>-</td><td>-</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>hidden</td><td>表示されないコントロール</td>				<td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>-</td><td>-</td><td>-</td></tr>
	<tr><td>date</td><td>日付の入力欄</td>								<td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>datetime</td><td>日付時刻の入力欄</td>						<td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>month</td><td>年月の入力欄</td>								<td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>week</td><td>週の入力欄</td>								<td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>time</td><td>時刻の入力欄</td>								<td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>color</td><td>カラーのコントロール</td>						<td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>range</td><td>範囲のコントロール</td>						<td>〇</td><td>〇</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>number</td><td>増減数値の入力欄</td>						<td>〇</td><td>〇</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>money0</td><td>小数点以降0桁金額の入力欄</td>				<td>〇</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>money1</td><td>小数点以降1桁金額の入力欄</td>				<td>〇</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>money2</td><td>小数点以降2桁金額の入力欄</td>				<td>〇</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>money3</td><td>小数点以降3桁金額の入力欄</td>				<td>〇</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>checkbox</td><td>チェックボックス</td>						<td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>radio</td><td>ラジオボタン</td>								<td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>combox</td><td>コンボックス</td>							<td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	<tr><td>button</td><td>ボタン</td>									<td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>-</td><td>〇</td></tr>
	<tr><td>img</td><td>画像</td>										<td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td><td>-</td><td>-</td><td>-</td></tr>
	<tr><td>span</td><td>ラベル</td>									<td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td><td>〇</td><td>-</td><td>-</td><td>-</td></tr>
</table>
</td></tr>
<tr><td>最大値</td><td>rangeとnumberタイプの最大値。</td></tr>
<tr><td>最小値</td><td>rangeとnumberタイプの最小値。</td></tr>
<tr><td>最大文字数</td><td>テキスト項目のmaxlength。</td></tr>
<tr><td>ソース</td><td>comboxとradioの選択肢。配列 ※２ または初期化処理を登録可能。
初期化処理関数のインタフェースは以下。
<table>
	<tr><th>部品</th><th>インタフェース</th><th>戻り値</th><th>formDataタイプ</th></tr>
	<tr><td>一覧画面</td><td>function( formData, initData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>Array</td><td><a href="param.initConditionData.md">initConditionData</a></td></tr>
	<tr><td>入力画面</td><td>function( formData, initData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>Array</td><td><a href="param.initFormData.md">initFormData</a></td></tr>
	<tr><td>入力ダイアログ</td><td>function( formData, dbData, initData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>Array</td><td><a href="param.initFormData.md">initFormData</a></td></tr>
	<tr><td>検索ダイアログ</td><td>function( formData, dbData, initData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>Array</td><td><a href="param.initConditionData.md">initConditionData</a></td></tr>
</table>
</td></tr>
<tr><td>タイトル幅</td><td>ラベルの幅。</td></tr>
<tr><td>入力枠幅</td><td>入力枠の幅。</td></tr>
<tr><td>入力枠高さ</td><td>テキストエリアの高さ。</td></tr>
<tr><td>値</td><td>入力枠に（初期）表示する内容。
<h3>一覧画面と選択ダイアログ</h3>
文字列または初期化処理を登録可能。初期化処理関数のインタフェースは以下。
<table>
	<tr><th>インタフェース</th><th>戻り値</th></tr>
	<tr><td>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td></tr>
</table>
formData：<a href="param.initConditionData.md">initConditionData</a>をご参照。
<h3>入力画面と入力ダイアログ</h3>
モード属性のオブジェクトで設定する。※２　
モード属性の値は、文字列または初期化処理を登録可能。初期化処理関数のインタフェースは以下。
<table>
	<tr><th>インタフェース</th><th>戻り値</th></tr>
	<tr><td>function( formData, dbData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td></tr>
</table>
formData：<a href="param.initFormData.md">initFormData</a>をご参照。
</td></tr>
<tr><td>編集不可</td><td>非活性する場合設定する。</td></tr>
<tr><td>タイトル操作</td><td>タイトル押下時のサーバ処理。</td></tr>
<tr><td>入力枠操作</td><td>入力枠押下時のサーバ処理。</td></tr>
</table>
※１：以下の例は入力枠の右枠に虫眼鏡アイコンと消しゴムアイコンを追加する書き方。

```html
<span style="display: inline-block;width:200px">承認者1</span><i class="bi-search" style="position:relative;left:200px;"></i><i class="bi-eraser" style="position:relative;left:210px;"></i>
```

※２：Sourceの登録値または処理関数の戻り値は以下のように、valueとoptionを持つオブジェクトの配列。

```
[{value:"0",option:"A"},{value:"1",option:"B"}]
```

以下のJquery式で特定可能。

入力枠
```
#{defId} #{itemId}
#{defId}_inputDialog #{itemId}
#{defId}_selectDialog #{itemId}
```
ラベル
```
#{defId} #lbl_{itemId}
#{defId}_inputDialog #lbl_{itemId}
#{defId}_selectDialog #lbl_{itemId}
```

