## 言語の設定

skeエンジンは日本語・英語・中国語の3種類言語を搭載しており、ログイン時切り替えできる。

他の言語を導入したい場合、以下のように設定を行う。
- まずWEB-INF/efw/i18nフォルダに既存言語XMLをコピーして他の言語に翻訳する。

- 作成した言語XMLファイルを略称名つけて以下の指定パスに格納する。

```
[myapp]/WEB-INF/efw/i18n/
	cn.xml
	en.xml
	jp.xml
	mylang.xml
```


### ここだよ
[利用場所](https://efwgrp.github.io/ske/svg/design.languages.svg)
