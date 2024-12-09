## 入力項目の共通定義

検索エリアの検索条件と入力エリアの入力項目は、
ほとんどの設定内容が同じだから、まとめて説明する。

- ID

項目ID、部品内ユニークな識別子。

- タイトル

表示ラベル。文字列または初期化処理を登録可能。
初期化処理関数のインタフェースは以下。
<table>
	<tr><th>部品</th><th>インタフェース</th><th>戻り値</th><th>formDataタイプ</th></tr>
	<tr><td>一覧画面</td>
		<td rowspan=2>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td>
		<td rowspan=2>String</td>
		<td rowspan=2><a href="param.initConditionData.md">initConditionData</a></td></tr>
	<tr><td>検索ダイアログ</td></tr>
	<tr><td>入力画面</td>
		<td rowspan=2>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td>
		<td rowspan=2>String</td>
		<td rowspan=2><a href="param.initFormData.md">initFormData</a></td></tr>
	<tr><td>入力ダイアログ</td></tr>
</table>
タイトルの文字列にhtmlタグを取り込んで、さらに鮮やかの表現ができる。以下の例は入力枠の右枠に虫眼鏡アイコンと消しゴムアイコンを追加する書き方。

```html
<span style="display: inline-block;width:200px">承認者1</span><i class="bi-search" style="position:relative;left:200px;"></i><i class="bi-eraser" style="position:relative;left:210px;"></i>
```


- タイプ
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

- 最大値

rangeとnumberタイプの最大値。

- 最小値

rangeとnumberタイプの最小値。

- 最大文字数

テキスト項目のmaxlength。

- ソース

comboxとradioの選択肢。配列または初期化処理を登録可能。
初期化処理関数のインタフェースは以下。
<table>
	<tr><th>部品</th><th>インタフェース</th><th>戻り値</th><th>formDataタイプ</th></tr>
	<tr><td>一覧画面</td><td>function( formData, initData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>Array</td><td><a href="param.initConditionData.md">initConditionData</a></td></tr>
	<tr><td>入力画面</td><td>function( formData, initData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>Array</td><td><a href="param.initFormData.md">initFormData</a></td></tr>
	<tr><td>入力ダイアログ</td><td>function( formData, dbData, initData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>Array</td><td><a href="param.initFormData.md">initFormData</a></td></tr>
	<tr><td>検索ダイアログ</td><td>function( formData, dbData, initData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>Array</td><td><a href="param.initConditionData.md">initConditionData</a></td></tr>
</table>

上記言及の配列は以下のように、valueとoptionを持つオブジェクトの配列。

```
[{value:"0",option:"A"},{value:"1",option:"B"}]
```

- タイトル幅

ラベルの幅。単位はpix。

- 入力枠幅

入力枠の幅。単位はpix

- 入力枠高さ

テキストエリアの高さ。単位はpix

- 値

入力枠に（初期）表示する内容。
<table>
	<tr><th>部品</th><th>インタフェース</th><th>戻り値</th></tr>
	<tr><td>一覧画面</td><td>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td></tr>
	<tr><td>選択ダイアログ</td><td>function( formData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td></tr>
	<tr><td>入力画面</td><td>function( formData, dbData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td></tr>
	<tr><td>入力ダイアログ</td><td>function( formData, dbData, <a href="https://github.com/efwGrp/efw4.X/blob/master/README.md#Result">result</a> ){ }</td><td>String</td></tr>
</table>

formData：<a href="param.initConditionData.md">initConditionData</a>をご参照。

<h3>一覧画面と選択ダイアログ</h3>
文字列または初期化処理を登録可能。初期化処理関数のインタフェースは以下。

<h3>入力画面と入力ダイアログ</h3>
モード属性のオブジェクトで設定する。※２　
モード属性の値は、文字列または初期化処理を登録可能。初期化処理関数のインタフェースは以下。

formData：<a href="param.initFormData.md">initFormData</a>をご参照。
</td></tr>
<tr><td>編集不可</td><td>非活性する場合設定する。</td></tr>
<tr><td>タイトル操作</td><td>タイトル押下時のサーバ処理。</td></tr>
<tr><td>入力枠操作</td><td>入力枠押下時のサーバ処理。</td></tr>
</table>


## 入力項目の特定

以下のJquery式で特定可能。


```
//ラベル
#{defId} #lbl_{itemId}
#{defId}_inputDialog #lbl_{itemId}
#{defId}_selectDialog #lbl_{itemId}
//入力枠
#{defId} #{itemId}
#{defId}_inputDialog #{itemId}
#{defId}_selectDialog #{itemId}
```

