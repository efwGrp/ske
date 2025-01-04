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
	<DIV class="MAIN-FORM"><DIV class="FORM">
	<!-- コンテンツ開始 -->
<NOBR STYLE="width:300px"><LABEL for="txtテスト項目" id="lblテスト項目"
STYLE="width:100px;">テスト項目</LABEL><INPUT id="txtテスト項目" TYPE="text"
MAXLENGTH="10"  STYLE="width:200px"></NOBR>
	<!-- コンテンツ終わり -->
	</DIV></DIV>
	<div class="FOOTER" style="text-align:right">
		<button onclick="myDialog.open('param1','param1')" id="btnSave"><i class="bi bi-save"> </i>マイダイアログ</button>
	</div>
</ske:page>
<SCRIPT>
//メインテーブルのサイズを自動調整する
$(function(){
	//存在しない場合0にする関数。
	function nvl(num){if (num==null){return 0;}else{return num;}}
	//メインテーブルの高さを調整するための関数
	function bodyResize(){
		//以下の各種類の高さは存在しない場合0にする。
		//bodyの高さ
		var bodyHeight=nvl($("body").height());
		//header部の高さ
		var headerHeight=nvl($("#myPage .HEADER").height());
		//header-menu部の高さ
		var headerMenuHeight=nvl($("#myPage .HEADER-MENU").height());
		//footer部の高さ
		var footerHeight=nvl($("#myPage .FOOTER").height());
		//メインテーブルの高さを計算する。
		var mainTableHeight=bodyHeight-headerHeight-headerMenuHeight-footerHeight-31;
		$(".MAIN-FORM").height(mainTableHeight+"px");
	}
	//resizeイベントを追加する。※複数設定可能
	$(window).resize(bodyResize);
	//resizeイベントを実行する。
	bodyResize();
	
	//初期化イベントを実行する
	//Efw("defId_inputPage_init");
});
</SCRIPT>
<efw:part path="myDialog.jsp"></efw:part>

```

## ここだよ

[イメージ](https://efwgrp.github.io/ske/img/myPage.png)