## プロパティの設定

[myapp]/WEB-INF/classes/efw.propertiesファイルに対してプロパティ設定を行う。

該当ファイルのベース説明は[efw.properties](https://github.com/efwGrp/efw4.X/blob/master/help/properties.web.md)をご参照ください。

ske専用のプロパティは以下のようにリストする。

<table>
  <tr><th>項目</th><th>初期値</th></tr>
  <tr><td>efw.login.key</td><td>USER_ID</td></tr>
  <tr><td colspan=2>ログインユーザIDのセッションキー。
  </td></tr>
  <tr><td>efw.auth.key</td><td>EFW_AUTH</td></tr>
  <tr><td colspan=2>ログインユーザのロールIDのセッションキー。<a href="https://efwgrp.github.io/ske/svg/properties.auth.key.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.license</td><td>SKEライセンスキー</td></tr>
  <tr><td colspan=2>ライセンスキーには利用ユーザ数、システム名とコピーライトを含んでいる。トライアル申込は<a href="https://escco-demo.escco.co.jp/lic4ske/index.jsp" target="_blank">こちらへ</a>。
  <a href="https://efwgrp.github.io/ske/svg/properties.license.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.username.key</td><td>USER_NM</td></tr>
  <tr><td colspan=2>ログインユーザ名のセッションキー。<a href="https://efwgrp.github.io/ske/svg/properties.username.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.theme.key</td><td>LOGIN_THEME</td></tr>
  <tr><td colspan=2>ログイン時選択されたテーマのセッションキー。</td></tr>
  <tr><td>efw.skeleton.theme.default</td><td>start</td></tr>
  <tr><td colspan=2>初回システム利用時のテーマを設定する。ログイン時選択されたテーマはクッキーに保存して、次回システム利用時はクッキーからテーマを特定する。</td></tr>
  <tr><td>efw.skeleton.themes</td><td>base, black-tie, blitzer, cupertino, dark-hive, dot-luv, eggplant, excite-bike, flick, hot-sneaks, humanity, le-frog, mint-choc, overcast, pepper-grinder, redmond, smoothness, south-street, start, sunny, swanky-purse, trontastic, ui-darkness, ui-lightness, vader</td></tr>
  <tr><td colspan=2>ログイン時選択候補のテーマ名リスト、カンマ区切り。
  各テーマの詳細はEfwの<a href="https://github.com/efwGrp/efw4.X/blob/master/help/tag.client.md">Client</a>タグの説明をご参考ください。
  <a href="https://efwgrp.github.io/ske/svg/properties.themes.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.csv.charset</td><td>MS932</td></tr>
  <tr><td colspan=2>ダウンロードするCSVファイルの文字コード。<a href="https://efwgrp.github.io/ske/svg/properties.csv.charset.svg">利用場所</a></td></tr>
</table>

カスタマイズプログラムに上記情報を取得する際、以下のサンプルをご参考ください。

```js
var userId=session.get(properties.get("efw.login.key","USER_ID"));
var roleId=session.get(properties.get("efw.auth.key","EFW_AUTH"));
var userNm=session.get(properties.get("efw.skeleton.username.key","USER_NM"));
var themeId=session.get(properties.get("efw.skeleton.theme.key","LOGIN_THEME"));
```
```jsp
String userId=(String)session.getAttribute(PropertiesManager.getProperty("efw.login.key", "USER_ID"));
String roleId=(String)session.getAttribute(PropertiesManager.getProperty("efw.auth.key", "EFW_AUTH"));
String userNm=(String)session.getAttribute(PropertiesManager.getProperty("efw.skeleton.username.key", "USER_NM"));
String themeId=(String)session.getAttribute(PropertiesManager.getProperty("efw.skeleton.theme.key", "LOGIN_THEME"));

```
