## 入力ダイアログ

入力ダイアログは標準部品の一つ。
標準利用は、リポジトリ定義の入力ダイアログタブで入要素を定義して、
リポジトリ定義・一覧画面タブのまたは入力画面タブの[インポートダイアログ](base.imports.md)に「{defId}_inputDialog」を登録する。

各種アドオンから入力ダイアログの標準関数を実行したい場合、以下のAPIをご参考ください。

<table>
<tr><th>メソッド名</th><th>インタフェース</th><th>戻り値</th><th>説明</th></tr>
<tr><th>呼び出し</th></tr>
<tr><td>新規モードで開く</td><td>{defId}_inputDialog.add ( closeCallback )</td><td>void</td><td>addモードで、{defId}_inputDialog_initイベントを実行する。</td></tr>
<tr><td>コピー新規モードで開く</td><td>{defId}_inputDialog.copyAdd ( selectId, closeCallback )</td><td>void</td><td>copyAddモードで、{defId}_inputDialog_initイベントを実行する。</td></tr>
<tr><td>編集モードで開く</td><td>{defId}_inputDialog.edit ( selectId, closeCallback )</td><td>void</td><td>editモードで、{defId}_inputDialog_initイベントを実行する。</td></tr>
<tr><td>参照モードで開く</td><td>{defId}_inputDialog.ref ( selectId )</td><td>void</td><td>refモードで、{defId}_inputDialog_initイベントを実行する。</td></tr>
<tr><th>フッター</th></tr>
<tr><td>追加ボタンをクリック</td><td>{defId}_inputDialog.{btnId}_onClick ( )</td><td>void</td><td>※１、{defId}_inputDialog_touchイベントを実行する。</td></tr>
<tr><td>保存</td><td>{defId}_inputDialog.save ( )</td><td>void</td><td>※１、{defId}_inputDialog_saveイベントを実行する。</td></tr>
<tr><td>閉じる</td><td>{defId}_inputDialog.close ( )</td><td>void</td><td></td></tr>
<tr><th>ダイアログ</th></tr>
<tr><td>ロール別の画面項目制限を実行</td><td>{defId}.doRoleConfig ( mode )</td><td>void</td><td></td></tr>
</table>

※１、該当メソッドは、リポジトリ定義により追加または削除される。

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>mode</td><td>String</td><td>add | copyAdd | edit | ref</td></tr>
<tr><td>closeCallback</td><td>function ( )</td><td>閉じるコールバック。</td></tr>
<tr><td>selectId</td><td>String</td><td>
選択行の主キー配列のJSON文字列。

```
//主キー配列のJSON文字列
"[\"PK1_1\",\"PK1_2\"]"
```
</td></tr>
</table>

## ここだよ

[イメージ](https://efwgrp.github.io/ske_image/img/inputDialog.png)
