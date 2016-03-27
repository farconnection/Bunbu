
####HTMLに画像を表示しよう
	* img - イメージタグ
		* 画像を表示できる

```html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<h1>ページのタイトルが入る</h1> // 「h1要素」もしくは「h1タグ」
		<p>ここにはテキストが入る</p>　// 「p要素」もしくは「pタグ」

		<img src="（画像のファイル名）" alt="（画像の説明）">
		・src : 画像のファイル名
		・alt : 画像の説明（必ず入れる必要はない）

		実際の例
		・りんごの画像を「apple.jpg」というファイル名でダウンロードした場合
		<img src="apple.jpg" alt="りんご">


	</body>

</html>
```

#####ダウンロードの仕方
* 使いたい画像があったら右クリック
	* Windowsの人
		* 「名前を付けて保存」をクリック
	* Macの人
		* 「画像を保存」をクリック
	* ファイル名を付けて、index.htmlと同じ階層（場所）に保存


####背景色を付けよう
* background - バックグラウンド
	* url
		* %
		* contain
		* cover

```html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="bg_black">ここにはテキストが入る</p>　// 「p要素」もしくは「pタグ」

		<style>

		.bg_black {
			background: red;
		}

		</style>


	</body>

</html>
```

####隙間を作ろう
* margin - マージン
	* 要素の外側の余白
* padding - パディング
	* 要素の内側の余白

```html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="bg_black">ここにはテキストが入る</p>　// 「p要素」もしくは「pタグ」
		<p class="bg_blue">ここにはテキストが入る</p>　// 「p要素」もしくは「pタグ」

		<style>

		.bg_black {
			background: red;
			margin: 10px;
			padding: 10px;
		}
		.bg_black {
			background: blue;
			padding: 10px;
		}

		</style>


	</body>

</html>
```



####横幅と高さを指定しよう
* width - ウィズ
	* 横幅を変える
* height - ヘイト
	* 高さを変える


```html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="bg_black">ここにはテキストが入る</p>　// 「p要素」もしくは「pタグ」
		<p class="bg_blue">ここにはテキストが入る</p>　// 「p要素」もしくは「pタグ」

		<style>

		.bg_black {
			background: red;
			width: 100px;
		}
		.bg_black {
			background: blue;
			height: 100px;
		}

		</style>


	</body>

</html>
```
