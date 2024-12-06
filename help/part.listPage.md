## 一覧画面

一覧画面は標準部品の一つ。
標準利用は、リポジトリ定義の一覧画面タブで一覧画面の要素を定義して、
メニュー定義でその一覧画面をメニューとリンクする。
さらにロール定義でその一覧画面はどのロールでみえるか設定する。

各種アドオンから一覧画面の標準関数を実行したい場合、以下のAPIをご参考ください。

<table>
<tr><th>属性＆メソッド名</th><th>インタフェース</th><th>戻り値</th><th>備考</th></tr>
<tr><td colspan=4>＜ページ＞</td></tr>
<tr><td>ログインユーザのロールIDを取得</td><td>page.getRoleId ( )</td><td>String</td><td></td></tr>
<tr><td>ログインユーザのユーザIDを取得</td><td>page.getUserId ( )</td><td>String</td><td></td></tr>
<tr><td>画面項目制限定義を取得</td><td>{defId}.roleConfig</td><td>void</td><td></td></tr>
<tr><td>画面項目制限関数を実行</td><td>{defId}.doRoleConfig( )</td><td>void</td><td></td></tr>
<tr><td colspan=4>＜ヘッダーエリア＞</td></tr>
<tr><td>検索</td><td>{defId}.search( newSrchFlg )</td><td>void</td><td></td></tr>
<tr><td>クリア</td><td>{defId}.clear( )</td><td>void</td><td>※１</td></tr>
<tr><td>追加ボタンをクリック</td><td>{defId}.{btnId}_onClick( )</td><td>void</td><td>※１</td></tr>
<tr><td colspan=4>＜検索結果エリア＞</td></tr>
<tr><td>最初のページへを遷移</td><td>{defId}.gotoFirstPage ( )</td><td>void</td><td></td></tr>
<tr><td>最後のページへを遷移</td><td>{defId}.gotoLastPage ( )</td><td>void</td><td></td></tr>
<tr><td>前のページへを遷移</td><td>{defId}.gotoPrePage ( )</td><td>void</td><td></td></tr>
<tr><td>次のページへを遷移</td><td>{defId}.gotoNextPage ( )</td><td>void</td><td></td></tr>
<tr><td>行をクリック</td><td>{defId}.clickRow ( row )</td><td>void</td><td></td></tr>
<tr><td>行をダブルクリック</td><td>{defId}.dblClickRow ( row )</td><td>void</td><td></td></tr>
<tr><td>選択状態を維持</td><td>{defId}.keepSelection ( row )</td><td>void</td><td></td></tr>
<tr><td>全選択or全解除</td><td>{defId}.selectAll ( )</td><td>void</td><td></td></tr>
<tr><td>チェック行のID配列を取得</td><td>{defId}.getSelectIds ( )</td><td>Array</td><td></td></tr>
<tr><td>選択行のIDを取得</td><td>{defId}.getSelectId ( )</td><td>String</td><td></td></tr>
<tr><td>選択行のObjを取得</td><td>{defId}.getSelectObj ( )</td><td>Object</td><td></td></tr>
<tr><td>検索結果エリアを初期化</td><td>{defId}.clearMainTable( )</td><td>void</td><td></td></tr>
<tr><td colspan=4>＜フッターエリア＞</td></tr>
<tr><td>新規</td><td>{defId}.add( )</td><td>void</td><td>※１</td></tr>
<tr><td>コピー新規</td><td>{defId}.copyAdd( )</td><td>void</td><td>※１</td></tr>
<tr><td>編集</td><td>{defId}.edit( )</td><td>void</td><td>※１</td></tr>
<tr><td>参照</td><td>{defId}.ref( )</td><td>void</td><td>※１</td></tr>
<tr><td>削除</td><td>{defId}.delete( )</td><td>void</td><td>※１</td></tr>
<tr><td>ダウンロード</td><td>{defId}.download( )</td><td>void</td><td>※１</td></tr>
<tr><td>アップロード</td><td>{defId}.upload( )</td><td>void</td><td>※１</td></tr>
<tr><td>添付</td><td>{defId}.attachEdit( )</td><td>void</td><td>※１</td></tr>
<tr><td>添付参照</td><td>{defId}.attachRef( )</td><td>void</td><td>※１</td></tr>
<tr><td>ダブルクリック実行関数を選定</td><td>{defId}.doDefault( )</td><td>void</td><td></td></tr>
<tr><td>追加ボタンをクリック</td><td>{defId}.{btnId}_onClick( )</td><td>void</td><td>※１</td></tr>
</table>

※１、該当メソッドは、リポジトリ定義により追加または削除される。

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>newSrchFlg</td><td>Boolean</td><td>true：新しい検索、false：改ページ検索orソース切替検索</td></tr>
<tr><td>row</td><td>Htmlタグ</td><td>選択された行。</td></tr>
</table>
