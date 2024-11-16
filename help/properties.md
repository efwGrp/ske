## プロパティの設定

[myapp]/WEB-INF/classes/efw.propertiesファイルに対してプロパティ設定を行う。

該当ファイルのベース説明は[efw.properties](https://github.com/efwGrp/efw4.X/blob/master/help/properties.web.md)をご参照ください。

プロパティ設定値は日本語の場合<a href="https://tech-unlimited.com/escape-unicode.html">Unicodeエンコード</a>を行ってください。


ske専用のプロパティは以下のようにリストする。

<table>
  <tr><th>項目</th><th>初期値</th></tr>
  <tr><td>efw.login.key</td><td>USER_ID</td></tr>
  <tr><td colspan=2>ログインユーザIDのセッションキー。
  </td></tr>
  <tr><td>efw.auth.key</td><td>EFW_AUTH</td></tr>
  <tr><td colspan=2>ログインユーザのロールIDのセッションキー。<a href="https://efwgrp.github.io/ske_image/svg/properties.auth.key.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.username.key</td><td>USER_NM</td></tr>
  <tr><td colspan=2>ログインユーザ名のセッションキー。<a href="https://efwgrp.github.io/ske_image/svg/properties.username.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.theme.key</td><td>LOGIN_THEME</td></tr>
  <tr><td colspan=2>ログイン時選択されたシーマのセッションキー。</td></tr>
  <tr><td>efw.skeleton.theme.default</td><td>start</td></tr>
  <tr><td colspan=2>初回システム利用時のシーマを設定する。ログイン時選択されたシーマはクッキーに保存して、次回システム利用時はクッキーからシーマを特定する。</td></tr>
  <tr><td>efw.skeleton.themes</td><td>base, black-tie, blitzer, cupertino, dark-hive, dot-luv, eggplant, excite-bike, flick, hot-sneaks, humanity, le-frog, mint-choc, overcast, pepper-grinder, redmond, smoothness, south-street, start, sunny, swanky-purse, trontastic, ui-darkness, ui-lightness, vader</td></tr>
  <tr><td colspan=2>ログイン時選択候補のシーマ名リスト、カンマ区切り。
  各シーマの詳細はEfwの<a href="https://github.com/efwGrp/efw4.X/blob/master/help/tag.client.md">Client</a>タグの説明をご参考ください。
  <a href="https://efwgrp.github.io/ske_image/svg/properties.themes.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.title</td><td>Efw Skeleton Engine</td></tr>
  <tr><td colspan=2>システムのタイトル。<a href="https://efwgrp.github.io/ske_image/svg/properties.title.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.copyright</td><td>© 2024 Escco Japan Co., Ltd.</td></tr>
  <tr><td colspan=2>システムの著作権。<a href="https://efwgrp.github.io/ske_image/svg/properties.copyright.svg">利用場所</a></td></tr>
  <tr><td>efw.skeleton.csv.charset</td><td>MS932</td></tr>
  <tr><td colspan=2>ダウンロードするCSVファイルの文字コード。<a href="https://efwgrp.github.io/ske_image/svg/properties.csv.charset.svg">利用場所</a></td></tr>
</table>

カスタマイズプログラムに上記情報を取得する際、以下のサンプルをご参考ください。

```js
var userId=session.get(properties.get("efw.login.key","USER_ID"));
var roleId=session.get(properties.get("efw.auth.key","EFW_AUTH"));
var userNm=session.get(properties.get("efw.skeleton.username.key","USER_NM"));
var themeId=session.get(properties.get("efw.skeleton.theme.key","LOGIN_THEME"));
var title=properties.get("efw.skeleton.title","Efw Skeleton Engine");
var copyright=properties.get("efw.skeleton.copyright","© 2024 Escco Japan Co., Ltd.");
```
```jsp
String userId=(String)session.getAttribute(PropertiesManager.getProperty("efw.login.key", "USER_ID"));
String roleId=(String)session.getAttribute(PropertiesManager.getProperty("efw.auth.key", "EFW_AUTH"));
String userNm=(String)session.getAttribute(PropertiesManager.getProperty("efw.skeleton.username.key", "USER_NM"));
String themeId=(String)session.getAttribute(PropertiesManager.getProperty("efw.skeleton.theme.key", "LOGIN_THEME"));
String title=PropertiesManager.getProperty("efw.skeleton.title","Efw Skeleton Engine");
String copyright=PropertiesManager.getProperty("efw.skeleton.copyright","© 2024 Escco Japan Co., Ltd.");

```
