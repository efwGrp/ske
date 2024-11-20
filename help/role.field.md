## 画面項目非活性非表示の設定

部品の項目は数が多いからデフォルトとして活性・表示にしている。
ロールにより非活性あるいは非表示にしたい場合、設定が必要。
<table>
<tr><th>項目</th><th>説明</th></tr>
<tr><td>リポジトリ定義</td><td>
	すべてのリポジトリ定義を表示する。
	定義済みの場合「*」が付ける。
	</td></tr>
<tr><td>部品種別</td><td>
	選択されたリポジトリの４種類部品をリストする。
	<table>
	<tr><td>listPage</td></tr>
	<tr><td>inputPage</td></tr>
	<tr><td>selectDialog</td></tr>
	<tr><td>inputDialog</td></tr>
	</table>
	定義済みの場合「*」が付ける。
</td></tr>
<tr><td>全項目</td><td>
	選択された種別の部品のすべての項目をリストする。
	<table>
	<tr><th>項目種別</th><th>listPage</th><th>inputPage</th><th>selectDialog</th><th>inputDialog</th></tr>
	<tr><td>header icon: [項目ID][項目名]</td>		<td>〇</td><td>〇</td><td></td><td></td></tr>
	<tr><td>header link: [項目ID][項目名]</td>		<td>〇</td><td>〇</td><td></td><td></td></tr>
	<tr><td>condition field: [項目ID][項目名]</td>	<td>〇</td><td></td><td>〇</td><td></td></tr>
	<tr><td>condition button: [項目ID][項目名]</td>	<td>〇</td><td></td><td>〇</td><td></td></tr>
	<tr><td>table column: [項目ID][項目名]</td>		<td>〇</td><td></td><td>〇</td><td></td></tr>
	<tr><td>input field: [項目ID][項目名]</td>		<td></td><td>〇</td><td></td><td>〇</td></tr>
	<tr><td>footer button: [項目ID][項目名]</td>	<td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
	</table>
	同じ部品に項目IDの重複が存在する場合、想定外の動きになってしまう。
</td></tr>
<tr><td>非活性項目</td><td>
	選択された非活性項目をリストする。
</td></tr>
<tr><td>非表示項目</td><td>
	選択された非表示項目をリストする。
</td></tr>
</table>

### ここだよ
[定義場所](https://efwgrp.github.io/ske_image/svg/role.field.svg)