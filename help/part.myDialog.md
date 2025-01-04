## 自作ダイアログ

自作ダイアログの場合、Jquery UIダイアログに従って作成する。以下のテンプレートをご利用ください。

```jsp
<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>
<%@ taglib prefix="efw" uri="efw"%>
<%@ taglib prefix="ske" uri="ske"%>
<%
String dialogId="myDialog";
%>
<ske:dialog dialogId="<%=dialogId%>" title="マイダイアログ" height="300" width="500">
	<DIV class="FORM">
	<!-- コンテンツ開始 -->
<NOBR STYLE="width:300px"><LABEL for="txtテスト項目" id="lblテスト項目"
STYLE="width:100px;">テスト項目</LABEL><INPUT id="txtテスト項目" TYPE="text"
MAXLENGTH="10"  STYLE="width:200px"></NOBR>
	<!-- コンテンツ終わり -->
	</DIV>
	<ske:section for="btn">
	<DIV CLASS="FOOTER" style="text-align:right">
		<BUTTON ID="btnUpload" ONCLICK="<%=dialogId%>.doit()"><i class="bi bi-cloud-download"> </i>マイ処理
		</BUTTON><BUTTON ID="btnClose" ONCLICK="<%=dialogId%>.close()"><i class="bi bi-door-closed"> </i>閉じる</BUTTON>
	</DIV>
	</ske:section>
</ske:dialog>
<SCRIPT>
//この段落はdialogのScriptタグの後ろに置く必要。
//開くメソッド
<%=dialogId%>.open=function(param1,param2){
	//defIdをhiddenに格納する
	<%=dialogId%>.param1=param1;
	<%=dialogId%>.param2=param2;
	
	//ダイアログを開く
	this.dlg.dialog("open");
	//初期化イベントを実行する
	//Efw("myDialog_init",{param1:<%=dialogId%>.param1,param2:<%=dialogId%>.param2});
};
//実行メソッド
<%=dialogId%>.doit=function(){
	//アクションイベントを実行する
	//Efw("myDialog_do",{param1:<%=dialogId%>.param1,param2:<%=dialogId%>.param2});
};
</SCRIPT>
```

## ここだよ

[イメージ](https://efwgrp.github.io/ske/img/myDialog.png)