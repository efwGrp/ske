## �t�b�^�[�G���A�̑I���{�^��

�I���_�C�A���O�̃t�b�^�[�G���A�ɑI���{�^����݂��Ă���B
�I���{�^���ɂ�茟�����ʂ̑I���s��O��ʂɓn���B
��`�ݒ�ɂ��{�^�����\�������邱�Ƃ͉\�B

�ȉ���Jquery���œ���\�B
```
#{defId}_selectDialog_footer #btnSelect
```

�I�����ʂ̎󂯎��́A�u�^�C�g������v�Ɓu�{�^�������v�Ȃǂ̃A�h�I���֐��ɃN���C�A���gjavaScript�őΉ�����B
�ȉ��̗�����Q�l���������B
```js
function(formData){
	//�߂�l��Result�͉�ʕ\���Ɠ���ɂȂ�A�K�v�ɉ����Đ݂��邱�Ƃ��\�B
	return (new Result()).eval(`
		USER_selectDialog.open({
			runat:"#K005_inputDialog",
			map:{
				"#fd���F�Ј��ԍ�":"���[�Uid",
				"#fd�Ј���":"���[�U��",
			}
		});
	`);
}
```

### ��������

[��`�ꏊ](https://efwgrp.github.io/ske_image/svg/footer.select.selectDialog.def.svg)�A[���p�ꏊ](https://efwgrp.github.io/ske_image/svg/footer.select.selectDialog.svg)
