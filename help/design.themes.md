## シーマの設定

skeエンジンはJquery-UIの25種類シーマを搭載しており、ログイン時切り替えできる。

専用シーマを導入したい場合、以下のように設定を行う。
- まずJquery-UIにてシーマを作成する。https://jqueryui.com/themeroller/

- 作成したシーマを以下のように指定パスに格納する。

```
[myapp]/jquery-ui/themes/[mytheme]
	images			//imagesフォルダ内のファイルはリネームしない
		ui-bg_diagonals-thick_75_f3d8d8_40x40.png
		ui-bg_dots-small_65_a6a6a6_2x2.png
		ui-bg_glass_55_fbf8ee_1x400.png
		ui-bg_highlight-hard_100_eeeeee_1x100.png
		ui-bg_highlight-hard_100_f6f6f6_1x100.png
		ui-bg_highlight-soft_15_000080_1x100.png
		ui-icons_000080_256x240.png
		ui-icons_004276_256x240.png
		ui-icons_ffffff_256x240.png
	theme.css		//シーマのcssファイルをリネームする
```
- プロパティファイルに自作シーマを登録する。[プロパティの設定へ](properties.md)


### ここだよ
[イメージ](https://efwgrp.github.io/ske_image/svg/design.themes.svg)
