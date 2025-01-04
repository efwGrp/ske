## テーブル＆クエリの設定

リポジトリは基本的に一つテーブル対するCRUD処理を定義する。
そのテーブルは、メインテーブルと称する。

テーブルの格納されるDBは、[context.xml](https://github.com/efwGrp/efw4.X/blob/master/help/resources.context.md)に定義し、その定義IDを
「JDBCリソース名」に登録する。ただし、デフォルトのJDBCリソースjdbc/efwは登録不要。
システム初期化便利のため、テーブルと初期値を「DDL」に定義できる。

- 画面の主要機能はテーブルCRUD処理ではない場合、カスタマイズ画面で対応してください。
- 画面は複数テーブルCRUDに関わる場合、メインのテーブルは「テーブル名」に登録してください。
- ほかのテーブルのCRUDはダイアログ画面で対応してください。
- 操作性のため画面分割不可の場合、カスタマイズ画面で対応してください。


各定義項目は以下のようにリストする。

|項目			|説明|
|-|-|
|テーブル名		|リポジトリに格納するメインテーブルの名称。※１|
|クエリ			|ほかのエンティティの項目が必要の場合、テーブルJOINのクエリを作る。|
|DDL			|リポジトリ定義に関わるテーブルを自動作成したい場合、テーブルDDLを登録する。|
|JDBCリソース名	|デフォルトはjdbc/efw。ほかのリソースを利用する場合登録する。|

※１：名称に特殊文字を含む場合、各DBのSQL規則に従ってコーテーションをつけてください。
```sql
--postgreSqlの場合、特殊文字を含むエンティティ名はダブルクォーテーションで囲む
"ユーザマスタA"
```

DDL登録のサンプル。毎回システム起動時、実行されるので、重複実行を防ぐ工夫が必要。
```sql
CREATE TABLE IF NOT EXISTS "ユーザマスタ"
(
  "ユーザID" character varying(10) PRIMARY KEY, -- ユーザID
  "所属部署コード" character varying(6), --所属部署コード
  "ユーザ名" character varying(20) -- ユーザ名
);
insert into "ユーザマスタ"
select 'admin',null
where not exists (
	select "ユーザID","所属部署コード","ユーザ名" 
	from "ユーザマスタ" where "ユーザID"='admin'
);
```

### ここだよ

[定義場所](https://efwgrp.github.io/ske/svg/comm.tableQuery.svg)