## ���i�̕�

�ꗗ��ʂ̏ꍇ�A����100%�Œ�Őݒ肪�K�v�Ȃ��B
���͉�ʂ̏ꍇ�A���̐ݒ�͓��̓G���A�̃T�C�Y�����ɓ]�p�����B
���̓_�C�A���O�ƑI���_�C�A���O�̏ꍇ�AJquery-UI�̃_�C�A���O�̕��ɂ�����B

���i�̕����v���O�����œ��I�ɒl��ݒ肷�邱�Ƃ𐄏����Ȃ����A�ȉ��̃N���C�A���g
javaScript����ʏ������̃A�h�I����eval�Ŏ��s������悤�ɂ���ΑΉ��\�ɂȂ�B

```js
//���͉�ʂ̏ꍇ�A����div�ɑ΂��Đݒ肷��
var width=$("#USER_form>div>div").css("width");
$("#USER_form>div>div").css("width","500px");
//���̓_�C�A���O�̏ꍇ�A�_�C�A���OID��{defId}_inputDialog�ɂȂ�
var width=USER_inputDialog.dlg.dialog("option","width");
USER_inputDialog.dlg.dialog("option","width","500px");
//�ƑI���_�C�A���O�̏ꍇ�A�_�C�A���OID��{defId}_selectDialog�ɂȂ�
var title=USER_selectDialog.dlg.dialog("option","width");
USER_selectDialog.dlg.dialog("option","width","500px");
```
��ʏ������̃A�h�I���͈ȉ��̂悤�Ƀ��X�g����B

- �ꗗ��ʁ������G���A��[��������](condition.conds.md)
- ���͉�ʁ����̓G���A��[���͍���](input.fds.md)
- ���̓_�C�A���O�����̓G���A��[���͍���](input.fds.md)
- �I���_�C�A���O�������G���A��[��������](condition.conds.md)

### ��������
���͉�ʁF[��`�ꏊ](https://efwgrp.github.io/ske_image/svg/base.width.inputPage.def.svg)�A[�C���[�W](https://efwgrp.github.io/ske_image/svg/base.width.inputPage.svg)

���̓_�C�A���O�F[��`�ꏊ](https://efwgrp.github.io/ske_image/svg/base.width.inputDialog.def.svg)�A[�C���[�W](https://efwgrp.github.io/ske_image/svg/base.width.inputDialog.svg)

�I���_�C�A���O�F[��`�ꏊ](https://efwgrp.github.io/ske_image/svg/base.width.selectDialog.def.svg)�A[�C���[�W](https://efwgrp.github.io/ske_image/svg/base.width.selectDialog.svg)

