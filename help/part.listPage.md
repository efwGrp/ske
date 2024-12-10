## 一覧画面

一覧画面は標準部品の一つ。
標準利用は、リポジトリ定義の一覧画面タブで要素を定義して、
メニュー定義でその一覧画面をメニューとリンクする。
さらにロール定義でその一覧画面はどのロールでみえるか設定する。

各種アドオンから一覧画面の標準関数を実行したい場合、以下のAPIをご参考ください。

<table>
<tr><th>メソッド名</th><th>インタフェース</th><th>戻り値</th><th>説明</th></tr>
<tr><th>呼び出し</th></tr>
<tr><td>URL</td><td colspan=2>http://.../myApp/listPage.jsp?defId={defId}</td><td>{defId}_listPage_initイベントを実行する。</td></tr>
<tr><th>ヘッダー</th></tr>
<tr><td>サイドバーを開く</td><td>{defId}.openSideBar( )</td><td>void</td><td>※１</td></tr>
<tr><td>サイドバーを閉じる</td><td>{defId}.closeSideBar( )</td><td>void</td><td>※１</td><</tr>
<tr><td>ログアウト</td><td>{defId}.logout( )</td><td>void</td><td>※１、head_logoutイベントを実行する。</td></tr>
<tr><td>メインメニューへ遷移</td><td>{defId}.gotoMenu( )</td><td>void</td><td>※１、LG02.jspへ遷移する。</td>></tr>
<tr><td>プロファイル画面を開く</td><td>{defId}.showProfile( )</td><td>void</td><td>※１、<a href="part.inputPage.md">inputPage.jsp</a>へ遷移する。</td></tr>
<tr><td>検索</td><td>{defId}.search( newSrchFlg )</td><td>void</td><td>{defId}_listPage_searchイベントを実行する。</td></tr>
<tr><td>クリア</td><td>{defId}.clear( )</td><td>void</td><td>※１、{defId}_listPage_clearイベントを実行する。</td></tr>
<tr><td>追加ボタンをクリック</td><td>{defId}.{btnId}_onClick( )</td><td>void</td><td>※１、{defId}_listPage_touchイベントを実行する。</td></tr>
<tr><th>検索結果</th></tr>
<tr><td>最初のページへ遷移</td><td>{defId}.gotoFirstPage ( )</td><td>void</td><td>{defId}_listPage_searchイベントを実行する。</td></tr>
<tr><td>最後のページへ遷移</td><td>{defId}.gotoLastPage ( )</td><td>void</td><td>{defId}_listPage_searchイベントを実行する。</td></tr>
<tr><td>前のページへ遷移</td><td>{defId}.gotoPrePage ( )</td><td>void</td><td>{defId}_listPage_searchイベントを実行する。</td></tr>
<tr><td>次のページへ遷移</td><td>{defId}.gotoNextPage ( )</td><td>void</td><td>{defId}_listPage_searchイベントを実行する。</td></tr>
<tr><td>行をクリック</td><td>{defId}.clickRow ( row )</td><td>void</td><td>操作行の背景色を設定し、主キー情報を記録する。</td></tr>
<tr><td>行をダブルクリック</td><td>{defId}.dblClickRow ( row )</td><td>void</td><td>選択結果の１行を下記「ダブルクリック実行関数を選定」により操作する。</td></tr>
<tr><td>選択状態を維持</td><td>{defId}.keepSelection ( row )</td><td>void</td><td>上記「行をクリック」に記録された主キー情報により行の背景色を設定する。</td></tr>
<tr><td>全選択or全解除</td><td>{defId}.selectAll ( )</td><td>void</td><td>選択結果を全部チェックするまたは解除する。</td></tr>
<tr><td>チェック行のID配列を取得</td><td>{defId}.getSelectIds ( )</td><td>Array</td><td>チェックされた複数行の主キーを取得して配列を作る。</td></tr>
<tr><td>選択行のIDを取得</td><td>{defId}.getSelectId ( )</td><td>String</td><td>選択された１行の主キーを取得する。</td></tr>
<tr><td>選択行のObjを取得</td><td>{defId}.getSelectObj ( )</td><td>Object</td><td>選択された１行のデータのJSONオブジェクトを取得する。</td></tr>
<tr><td>検索結果エリアを初期化</td><td>{defId}.clearMainTable ( )</td><td>void</td><td>検索結果エリアのソート順と改ページ情報を初期化する。</td></tr>
<tr><th>フッター</th></tr>
<tr><td>新規</td><td>{defId}.add ( )</td><td>void</td><td>※１、addモードで、<a href="part.inputPage.md">inputPage.jsp</a>へ遷移する。または、<a href="part.inputDialog.md">{defId}_inputDialog</a>.addを呼び出す。</td></tr>
<tr><td>コピー新規</td><td>{defId}.copyAdd ( )</td><td>void</td><td>※１、copyAddモードで、<a href="part.inputPage.md">inputPage.jsp</a>へ遷移する。または、<a href="part.inputDialog.md">{defId}_inputDialog</a>.copyAddを呼び出す。</td></tr>
<tr><td>編集</td><td>{defId}.edit ( )</td><td>void</td><td>※１、editモードで、<a href="part.inputPage.md">inputPage.jsp</a>へ遷移する。または、<a href="part.inputDialog.md">{defId}_inputDialog</a>.editを呼び出す。</td></tr>
<tr><td>参照</td><td>{defId}.ref ( )</td><td>void</td><td>※１、refモードで、<a href="part.inputPage.md">inputPage.jsp</a>へ遷移する。または、<a href="part.inputDialog.md">{defId}_inputDialog</a>.refを呼び出す。</td></tr>
<tr><td>削除</td><td>{defId}.delete ( )</td><td>void</td><td>※１、{defId}_listPage_deleteイベントを実行する。</td></tr>
<tr><td>ダウンロード</td><td>{defId}.download ( )</td><td>void</td><td>※１、<a href="part.downloadDialog.md">downloadDialog</a>を呼び出す。</td></tr>
<tr><td>アップロード</td><td>{defId}.upload ( )</td><td>void</td><td>※１、<a href="part.uploadDialog.md">uploadDialog</a>を呼び出す。</td></tr>
<tr><td>添付</td><td>{defId}.attachEdit ( )</td><td>void</td><td>※１、editモードで<a href="part.attachDialog.md">attachDialog</a>を呼び出す。</td></tr>
<tr><td>添付参照</td><td>{defId}.attachRef ( )</td><td>void</td><td>※１、refモードで<a href="part.attachDialog.md">attachDialog</a>を呼び出す。</td></tr>
<tr><td>ダブルクリック実行関数を選定</td><td>{defId}.doDefault ( )</td><td>void</td><td>編集・参照・添付・添付参照の順で、利用不可機能を除き処理関数を決めて実行する。</td></tr>
<tr><td>追加ボタンをクリック</td><td>{defId}.{btnId}_onClick ( )</td><td>void</td><td>※１、{defId}_listPage_touchイベントを実行する。</td></tr>
<tr><th>ページ</th></tr>
<tr><td>ログインユーザのロールIDを取得</td><td>page.getRoleId ( )</td><td>String</td><td></td></tr>
<tr><td>ログインユーザのユーザIDを取得</td><td>page.getUserId ( )</td><td>String</td><td></td></tr>
<tr><td>ロール別の画面項目制限を実行</td><td>{defId}.doRoleConfig ( )</td><td>void</td><td>ロール定義の<a href="role.field.md">画面項目非活性非表示の設定</a>を実行する。</td></tr>
</table>

※１、該当メソッドは、リポジトリ定義により追加または削除される。

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>newSrchFlg</td><td>Boolean</td><td>true：新しい検索、false：改ページ検索orソース切替検索</td></tr>
<tr><td>row</td><td>Htmlタグ</td><td>選択された行。</td></tr>
</table>

## ここだよ

[イメージ](https://efwgrp.github.io/ske_image/img/listPage.png)
