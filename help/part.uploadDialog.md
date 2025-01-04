## アップロードダイアログ

アップロードダイアログは標準部品の一つ。
標準利用は、一覧画面のアップロードボタンで呼び出して、テーブル項目のCSVを選んでアップロードする。

ダウンロードボタンではない箇所から利用したい場合、以下のAPIをご参考ください。

<table>
<tr><th>メソッド名</th><th>インタフェース</th><th>戻り値</th><th>説明</th></tr>
<tr><th>呼び出し</th></tr>
<tr><td>開く</td><td>uploadDialog.open ( defId, closeCallback )</td><td>void</td><td></td></tr>
<tr><th>フッター</th></tr>
<tr><td>ダウンロード</td><td>uploadDialog.download ( )</td><td>void</td><td>{defId}_listPage_uploadイベントを実行する。</td></tr>
<tr><td>閉じる</td><td>uploadDialog.close ( )</td><td>void</td><td></td></tr>
</table>

<table>
<tr><th>引数</th><th>種類</th><th>説明</th></tr>
<tr><td>defId</td><td>String</td><td>リポジトリ定義ID。</td></tr>
<tr><td>closeCallback</td><td>function ( )</td><td>閉じるコールバック。</td></tr>
</table>

## ここだよ

[イメージ](https://efwgrp.github.io/ske/img/uploadDialog.png)
