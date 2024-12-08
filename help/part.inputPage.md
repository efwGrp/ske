## 入力画面

入力画面は標準部品の一つ。
標準利用は、リポジトリ定義の入力画面タブで要素を定義して、
メニュー定義でその入力画面をメニューとリンクする。
または、リポジトリ定義・一覧画面タブの「連携する入力部品」で入力画面を選択する。
さらにロール定義でその入力画面はどのロールでみえるか設定する。

各種アドオンから入力画面の標準関数を実行したい場合、以下のAPIをご参考ください。

<table>
<tr><th>メソッド名</th><th>インタフェース</th><th>戻り値</th><th>備考</th></tr>
<tr><th>呼び出し</th></tr>
<tr><td>URL</td><td colspan=3>http://.../myApp/inputPage.jsp?defId={defId}&mode={mode}&selectId={selectId}</td></tr>
<tr><th>ページ</th></tr>
<tr><td>ログインユーザのロールIDを取得</td><td>page.getRoleId ( )</td><td>String</td><td></td></tr>
<tr><td>ログインユーザのユーザIDを取得</td><td>page.getUserId ( )</td><td>String</td><td></td></tr>
<tr><td>ロール別の画面項目制限を実行</td><td>{defId}.doRoleConfig ( mode )</td><td>void</td><td></td></tr>
<tr><th>ヘッダー</th></tr>
<tr><td>サイドバーを開く</td><td>{defId}.openSideBar( )</td><td>void</td><td>※１</td></tr>
<tr><td>サイドバーを閉じる</td><td>{defId}.closeSideBar( )</td><td>void</td><td>※１</td></tr>
<tr><td>ログアウト</td><td>{defId}.logout( )</td><td>void</td><td>※１</td></tr>
<tr><td>メインメニューへ遷移</td><td>{defId}.gotoMenu( )</td><td>void</td><td>※１</td></tr>
<tr><td>プロファイル画面を開く</td><td>{defId}.showProfile( )</td><td>void</td><td>※１</td></tr>
<tr><th>フッター</th></tr>
<tr><td>保存</td><td>{defId}.save( )</td><td>void</td><td>※１</td></tr>
<tr><td>閉じる</td><td>{defId}.close( )</td><td>void</td><td>※１</td></tr>
<tr><td>追加ボタンをクリック</td><td>{defId}.{btnId}_onClick( )</td><td>void</td><td>※１</td></tr>
</table>

※１、該当メソッドは、リポジトリ定義により追加または削除される。

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>defId</td><td>String</td><td>リポジトリ定義ID</td></tr>
<tr><td>mode</td><td>String</td><td>add | copyAdd | edit | ref</td></tr>
<tr><td>selectId</td><td>String</td><td>選択行の主キー配列のJSON文字列。

```
//主キー配列のJSON文字列
"[\"PK1_1\",\"PK1_2\"]"
//URLに利用する場合URLエンコード必要。
%5B%22PK1_1%22%2C%22PK1_2%22%5D
```
</td></tr>
</table>
