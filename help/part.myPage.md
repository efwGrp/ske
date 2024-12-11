## 自作画面

自作画面の場合、自由に作成できる。もし、標準デザインを流用したい場合、以下のテンプレートをご利用ください。

```jsp
<%@ page language="java" contentType="text/html; charset=UTF-8"
	pageEncoding="UTF-8"%>
<%@ taglib prefix="efw" uri="efw"%>
<%@ taglib prefix="ske" uri="ske"%>
<ske:page defId="myPage" title="マイページ" lang="jp">
	<ske:header title="マイページ">
	<ske:section for="ico">
		<i class="bi bi-github" title="テストアイコン" onclick="alert('hello world!')"></i>
	</ske:section>
	<ske:section for="lnk">
		<a href="https://github.com/efwGrp">テストリンク</a>
	</ske:section>
	</ske:header>
	<DIV class="MAIN" style="text-align:left;">
	<!-- コンテンツ開始 -->
	<p>あいうえお</p>
	<p>あいうえお</p>
	<p>あいうえお</p>
	<p>あいうえお</p>
	<p>あいうえお</p>
	<!-- コンテンツ終わり -->
	</DIV>
	<ske:footer for="copyRight"></ske:footer>
</ske:page>

```

## ここだよ

[イメージ](https://efwgrp.github.io/ske_image/img/myPage.png)