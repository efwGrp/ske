## �e�[�u�����N�G���̐ݒ�

���|�W�g���͊�{�I�Ɉ�e�[�u���΂���CRUD�������`����B
���̃e�[�u���́A���C���e�[�u���Ə̂���B

�e�[�u���̊i�[�����DB�́A[context.xml](https://github.com/efwGrp/efw4.X/blob/master/help/resources.context.md)�ɒ�`���A���̒�`ID��
�uJDBC���\�[�X���v�ɓo�^����B�������A�f�t�H���g��JDBC���\�[�Xjdbc/efw�͓o�^�s�v�B
�V�X�e���������֗��̂��߁A�e�[�u���Ə����l���uDDL�v�ɒ�`�ł���B

- ��ʂ̎�v�@�\�̓e�[�u��CRUD�����ł͂Ȃ��ꍇ�A�J�X�^�}�C�Y��ʂőΉ����Ă��������B
- ��ʂ͕����e�[�u��CRUD�Ɋւ��ꍇ�A���C���̃e�[�u���́u�e�[�u�����v�ɓo�^���Ă��������B
- �ق��̃e�[�u����CRUD�̓_�C�A���O��ʂőΉ����Ă��������B
- ���쐫�̂��߉�ʕ����s�̏ꍇ�A�J�X�^�}�C�Y��ʂőΉ����Ă��������B


�e��`���ڂ͈ȉ��̂悤�Ƀ��X�g����B

|����			|����|
|-|-|
|�e�[�u����		|���|�W�g���Ɋi�[���郁�C���e�[�u���̖��́B|
|�N�G��			|�ق��̃G���e�B�e�B�̍��ڂ��K�v�̏ꍇ�A�e�[�u��JOIN�̃N�G�������B|
|DDL			|���|�W�g����`�Ɋւ��e�[�u���������쐬�������ꍇ�A�e�[�u��DDL��o�^����B|
|JDBC���\�[�X��	|�f�t�H���g��jdbc/efw�B�ق��̃��\�[�X�𗘗p����ꍇ�o�^����B|

DDL�o�^�̃T���v��
```sql
CREATE TABLE IF NOT EXISTS "���[�U�}�X�^"
(
  "���[�UID" character varying(10) PRIMARY KEY, -- ���[�UID
  "���������R�[�h" character varying(6), --���������R�[�h
  "���[�U��" character varying(20) -- ���[�U��
);
insert into "���[�U�}�X�^"
select 'admin',null
where not exists (
	select "���[�UID","���������R�[�h","���[�U��" 
	from "���[�U�}�X�^" where "���[�UID"='admin'
);
```

### ��������

[��`�ꏊ](https://efwgrp.github.io/ske_image/svg/comm.tableQuery.svg)