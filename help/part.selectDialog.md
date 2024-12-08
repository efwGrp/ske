## 選択ダイアログ

選択ダイアログは標準部品の一つ。
標準利用は、リポジトリ定義の選択ダイアログタブで要素を定義して、
リポジトリ定義・一覧画面タブのまたは入力画面タブの[インポートダイアログ](base.imports.md)に「{defId}_selectDialog」を登録する。

各種アドオンから入力ダイアログの標準関数を実行したい場合、以下のAPIをご参考ください。

<table>
<tr><th>メソッド名</th><th>インタフェース</th><th>戻り値</th><th>備考</th></tr>
<tr><th>呼び出し</th></tr>
<tr><td>開く</td><td>{defId}_selectDialog.open ( selectCallback )</td><td>void</td><td></td></tr>
<tr><th>ダイアログ</th></tr>
<tr><td>閉じる</td><td>{defId}_selectDialog.close ( )</td><td>void</td><td></td></tr>
<tr><td>ロール別の画面項目制限を実行</td><td>{defId}_selectDialog.doRoleConfig ( )</td><td>void</td><td></td></tr>
<tr><th>ヘッダー</th></tr>
<tr><td>検索</td><td>{defId}_selectDialog.search( newSrchFlg )</td><td>void</td><td></td></tr>
<tr><td>クリア</td><td>{defId}_selectDialog.clear( )</td><td>void</td><td>※１</td></tr>
<tr><th>検索結果</th></tr>
<tr><td>最初のページへ遷移</td><td>{defId}_selectDialog.gotoFirstPage ( )</td><td>void</td><td></td></tr>
<tr><td>最後のページへ遷移</td><td>{defId}_selectDialog.gotoLastPage ( )</td><td>void</td><td></td></tr>
<tr><td>前のページへ遷移</td><td>{defId}_selectDialog.gotoPrePage ( )</td><td>void</td><td></td></tr>
<tr><td>次のページへ遷移</td><td>{defId}_selectDialog.gotoNextPage ( )</td><td>void</td><td></td></tr>
<tr><td>行をクリック</td><td>{defId}_selectDialog.clickRow ( row )</td><td>void</td><td></td></tr>
<tr><td>行をダブルクリック</td><td>{defId}_selectDialog.dblClickRow ( row )</td><td>void</td><td></td></tr>
<tr><td>選択状態を維持</td><td>{defId}_selectDialog.keepSelection ( row )</td><td>void</td><td></td></tr>
<tr><td>選択行のIDを取得</td><td>{defId}_selectDialog.getSelectId ( )</td><td>String</td><td></td></tr>
<tr><td>選択行のObjを取得</td><td>{defId}_selectDialog.getSelectObj ( )</td><td>Object</td><td></td></tr>
<tr><td>検索結果エリアを初期化</td><td>{defId}_selectDialog.clearMainTable ( )</td><td>void</td><td></td></tr>
<tr><th>フッター</th></tr>
<tr><td>選択</td><td>{defId}_selectDialog.select ( )</td><td>void</td><td>※１</td></tr>
<tr><td>新規</td><td>{defId}_selectDialog.add ( )</td><td>void</td><td>※１</td></tr>
<tr><td>コピー新規</td><td>{defId}_selectDialog.copyAdd ( )</td><td>void</td><td>※１</td></tr>
<tr><td>編集</td><td>{defId}_selectDialog.edit ( )</td><td>void</td><td>※１</td></tr>
<tr><td>参照</td><td>{defId}_selectDialog.ref ( )</td><td>void</td><td>※１</td></tr>
<tr><td>削除</td><td>{defId}_selectDialog.delete ( )</td><td>void</td><td>※１</td></tr>
<tr><td>ダブルクリック実行関数を選定</td><td>{defId}_selectDialog.doDefault ( )</td><td>void</td><td></td></tr>
<tr><td>追加ボタンをクリック</td><td>{defId}_selectDialog.{btnId}_onClick ( )</td><td>void</td><td>※１</td></tr>
</table>

※１、該当メソッドは、リポジトリ定義により追加または削除される。

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>selectCallback</td><td>Object</td><td>

```js
//selectCallbackはマップと関数で構成する
USER_selectDialog.open({
  runat: "#K005_inputDialog",
  map: {
    "#fd承認社員番号":"ユーザid",
    "#fd社員名":"ユーザ名",
  },
  callback: function(id, obj){},
});
```
</td></tr>
<tr><td>newSrchFlg</td><td>Boolean</td><td>true：新しい検索、false：改ページ検索orソース切替検索</td></tr>
<tr><td>row</td><td>Htmlタグ</td><td>選択された行。</td></tr>
</table>
