## ���̓_�C�A���O

���̓_�C�A���O�͕W�����i�̈�B
�W�����p�́A���|�W�g����`�̓��̓_�C�A���O�^�u�œ��̓_�C�A���O�̗v�f���`���āA
���|�W�g����`�E�ꗗ��ʃ^�u�̂܂��͓��͉�ʃ^�u��[�C���|�[�g�_�C�A���O](base.imports.md)�Ɂu{defId}_inputDialog�v��o�^����B

�e��A�h�I��������̓_�C�A���O�̕W���֐������s�������ꍇ�A�ȉ���API�����Q�l���������B

<table>
<tr><th>���\�b�h��</th><th>�C���^�t�F�[�X</th><th>�߂�l</th><th>���l</th></tr>
<tr><th>�Ăяo��</th></tr>
<tr><td>�V�K���[�h�ŊJ��</td><td>{defId}_inputDialog.add ( closeCallback )</td><td>void</td><td></td></tr>
<tr><td>�R�s�[�V�K���[�h�ŊJ��</td><td>{defId}_inputDialog.copyAdd ( selectId, closeCallback )</td><td>void</td><td></td></tr>
<tr><td>�ҏW���[�h�ŊJ��</td><td>{defId}_inputDialog.edit ( selectId, closeCallback )</td><td>void</td><td></td></tr>
<tr><td>�Q�ƃ��[�h�ŊJ��</td><td>{defId}_inputDialog.ref ( selectId )</td><td>void</td><td></td></tr>
<tr><th>�_�C�A���O</th></tr>
<tr><td>�J��</td><td>{defId}_inputDialog.open ( )</td><td>void</td><td></td></tr>
<tr><td>����</td><td>{defId}_inputDialog.close ( )</td><td>void</td><td></td></tr>
<tr><td>���[���ʂ̉�ʍ��ڐ��������s</td><td>{defId}.doRoleConfig ( mode )</td><td>void</td><td></td></tr>
<tr><th>�t�b�^�[</th></tr>
<tr><td>�ۑ�</td><td>{defId}_inputDialog.save ( )</td><td>void</td><td>���P</td></tr>
<tr><td>�ǉ��{�^�����N���b�N</td><td>{defId}_inputDialog.{btnId}_onClick ( )</td><td>void</td><td>���P</td></tr>
</table>

���P�A�Y�����\�b�h�́A���|�W�g����`�ɂ��ǉ��܂��͍폜�����B

<table>
<tr><th>����</th><th>���</th><th>����</th></tr>
<tr><td>mode</td><td>String</td><td>add | copyAdd | edit | ref</td></tr>
<tr><td>closeCallback</td><td>function ( )</td><td>����R�[���o�b�N�B</td></tr>
<tr><td>selectId</td><td>String</td><td>
�I���s�̎�L�[�z���JSON������B

```
//��L�[�z���JSON������
"[\"admin\"]"
```
</td></tr>
</table>
