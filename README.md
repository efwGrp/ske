# Efw Skeleton Engine
## 紹介
[![SKE Runtime](./img/ske_runtime.png)](./img/ske_runtime_org.png)
[![SKE Editor](./img/ske_editor.png)](./img/ske_editor_org.png)
- [SKEとは](https://qiita.com/changkejun/items/da8e3d944879bd60a7a9)
## 手順＆説明
- [環境構築の手順](https://qiita.com/changkejun/items/52a786eaed1a1c6ac98b)、 [トライアルライセンス]（https://escco-demo.escco.co.jp/lic4ske/index.jsp）
- [プロトタイプ作成の手順](https://qiita.com/changkejun/items/2f25030223b7d3f0091f)
- [標準部品の鮮やかな表現力](https://qiita.com/changkejun/items/6918a886d76132d98496)
- [標準部品アドオン開発の紹介](https://qiita.com/changkejun/items/51e0d436b6c917269b51)<br>
　[自動採番のさまざま](https://qiita.com/changkejun/items/6ebe7d24fd54feac5be3)<br>
　[更新日時の排他処理](https://qiita.com/changkejun/items/532e5a177782937d2842)<br>
　[階層連動ドロップダウン](https://qiita.com/changkejun/items/c3837e00fa42f0381795)<br>
　[選択ダイアログの利用](https://qiita.com/changkejun/items/0cee4173eac17ce7cf98)<br>
　[検索結果の加工](https://qiita.com/changkejun/items/d36c8bbe3c74ceaaddb9)<br>
- 新しいロール追加の手順
- カスタマイズ部品追加の手順
- [多国語対応の手順](https://qiita.com/changkejun/items/a656091d345158e8871f)
- [多種類DB対応の手順](https://qiita.com/changkejun/items/e805eef2c8a2fe134d6f)
- インタネット公開の注意事項

# API
### デザイン
<table>
<tr><td><a href="help/design.logo.md">ロゴの設定</a></td></tr>
<tr><td><a href="help/design.themes.md">テーマの設定</a></td></tr>
<tr><td><a href="help/design.languages.md">言語の設定</a></td></tr>
</table>

### プロパティ
<table>
<tr><td><a href="help/properties.md">プロパティの設定</a></td></tr>
</table>

### 部品モデル

<table>
<tr><th>部品</th><th>区分</th></tr>
<tr><td><a href="help/part.listPage.md">一覧画面</a></td><td>標準部品・定義可能</td></tr>
<tr><td><a href="help/part.inputPage.md">入力画面</a></td><td>標準部品・定義可能</td></tr>
<tr><td><a href="help/part.inputDialog.md">入力ダイアログ</a></td><td>標準部品・定義可能</td></tr>
<tr><td><a href="help/part.selectDialog.md">選択ダイアログ</a></td><td>標準部品・定義可能</td></tr>
<tr><td><a href="help/part.attachDialog.md">添付ダイアログ</a></td><td>標準部品</td></tr>
<tr><td><a href="help/part.downloadDialog.md">ダウンロードダイアログ</a></td><td>標準部品</td></tr>
<tr><td><a href="help/part.uploadDialog.md">アップロードダイアログ</a></td><td>標準部品</td></tr>
<tr><td><a href="help/part.myPage.md">自作画面</a></td><td>自作部品</td></tr>
<tr><td><a href="help/part.myDialog.md">自作ダイアログ</a></td><td>自作部品</td></tr>
</table>

### ロール定義
<table>
<tr><td><a href="help/role.menu.md">メニュー閲覧可の設定</a></td></tr>
<tr><td><a href="help/role.page.md">メイン画面閲覧可の設定</a></td></tr>
<tr><td><a href="help/role.field.md">画面項目非活性非表示の設定</a></td></tr>
</table>

### メニュー定義
<table>
<tr><td><a href="help/menu.md">メニューの設定</a></td></tr>
</table>

### リポジトリ定義

<table>
<tr><th>共通設定</th></tr>
<tr><td><a href="help/comm.tableQuery.md">テーブル＆クエリの設定</a></td></tr>
<tr><td><a href="help/comm.beforeAfter.md">CRUD前後イベントの設定</a></td></tr>
<tr><td><a href="help/comm.fields.md">テーブル＆クエリ項目の設定</a></td></tr>
</table>

<table>
<tr><th>定義項目/部品</th>
	<th>一覧画面</th>
	<th>入力画面</th>
	<th>入力ダイアログ</th>
	<th>選択ダイアログ</th>
</tr>
<tr><th>基本情報</th></tr>
<tr><td><a href="help/base.title.md">タイトル</a></td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
<tr><td><a href="help/base.width.md">横幅</a></td><td></td><td>〇</td><td>〇</td><td>〇</td></tr>
<tr><td><a href="help/base.height.md">高さ</a></td><td></td><td>〇</td><td>〇</td><td>〇</td></tr>
<tr><td><a href="help/base.direction.md">並び方向</a></td><td></td><td>〇</td><td>〇</td><td></td></tr>
<tr><td>[<a href="help/base.imports.md">インポートダイアログ</a>]</td><td>〇</td><td>〇</td><td></td><td></td></tr>
<tr><th>ヘッダー</th></tr>
<tr><td><a href="help/header.title.md">タイトル</a></td><td>〇</td><td>〇</td><td></td><td></td></tr>
<tr><td><a href="help/header.profile.md">プロファイル</a></td><td>〇</td><td>〇</td><td></td><td></td></tr>
<tr><td><a href="help/header.logout.md">ログアウト</a></td><td>〇</td><td>〇</td><td></td><td></td></tr>
<tr><td><a href="help/header.menu.md">メニュー</a></td><td>〇</td><td>〇</td><td></td><td></td></tr>
<tr><td><a href="help/header.sidebar.md">サイドバー</a></td><td>〇</td><td>〇</td><td></td><td></td></tr>
<tr><td>[<a href="help/header.icos.md">追加アイコン</a>]</td><td>〇</td><td>〇</td><td></td><td></td></tr>
<tr><td>[<a href="help/header.lnks.md">追加リンク</a>]</td><td>〇</td><td>〇</td><td></td><td></td></tr>
<tr><th>検索エリア</th></tr>
<tr><td><a href="help/condition.search.md">検索ボタン</a></td><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><td><a href="help/condition.clear.md">クリアボタン</a></td><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><td>[<a href="help/condition.conds.md">検索条件</a>]</td><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><td>[<a href="help/condition.btns.md">追加ボタン</a>]</td><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><th>結果エリア</th></tr>
<tr><td>[<a href="help/ths.md">検索結果</a>]</td><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><th>入力エリア</th></tr>
<tr><td>[<a href="help/input.fds.md">入力項目</a>]</td><td></td><td>〇</td><td>〇</td><td></td></tr>
<tr><th>フッター</th></tr>
<tr><td><a href="help/footer.select.md">選択ボタン</a><td></td><td></td><td></td><td>〇</td></tr>
<tr><td><a href="help/footer.add.md">新規ボタン</a><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><td><a href="help/footer.copyAdd.md">コピー新規ボタン</a><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><td><a href="help/footer.edit.md">編集ボタン</a><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><td><a href="help/footer.ref.md">参照ボタン</a><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><td><a href="help/footer.delete.md">削除ボタン</a><td>〇</td><td></td><td></td><td>〇</td></tr>
<tr><td><a href="help/footer.download.md">ダウンロードボタン</a><td>〇</td><td></td><td></td><td></td></tr>
<tr><td><a href="help/footer.upload.md">アップロードボタン</a><td>〇</td><td></td><td></td><td></td></tr>
<tr><td><a href="help/footer.attachEdit.md">添付ボタン</a><td>〇</td><td></td><td></td><td></td></tr>
<tr><td><a href="help/footer.attachRef.md">添付参照ボタン</a><td>〇</td><td></td><td></td><td></td></tr>
<tr><td><a href="help/footer.save.md">保存ボタン</a><td></td><td>〇</td><td>〇</td><td></td></tr>
<tr><td><a href="help/footer.close.md">閉じるボタン</a><td></td><td>〇</td><td>〇</td><td>〇</td></tr>
<tr><td>[<a href="help/footer.btns.md">追加ボタン</a>]</td><td>〇</td><td>〇</td><td>〇</td><td>〇</td></tr>
</table>

