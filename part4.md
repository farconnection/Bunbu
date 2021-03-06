#パート４

##マイタイピング練習
* 初級編 - http://typing.twi1.me/game/46472
* 中級編 - http://typing.twi1.me/game/47838

##実際に作ってみよう

####必要な知識
* HTMLファイル
	* これがホームページ等になり公開される
	* WEBサイトの基盤となる枠組みのようなもの
	* 「<」「>」で囲まれる部分を「要素」もしくは、「タグ」と呼ぶ
	* HTMLは要素（タグ）で作っていく
	* 基本的に要素（タグ）は小文字で書く
	* 基本的に開始タグ「<>」と閉じタグ「</>」を書く

* CSS
	* HTMLに色をつけたり、文字を大きくしたり小さくしたり装飾できるもの

###作ってみよう

####index.html作成 - サイトの入り口となるファイルを作成
#####html要素

```html
<!DOCTYPE html>　
<html lang="ja">
	<head>
		<meta charset="utf-8">
		<title></title>
	</head>
	<body>
		<h1></h1>
		<p></p>
	</body>
</html>
```

```html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
		<meta charset="utf-8"> // 文字化けをしないように
	</head>

	<!-- ここからが本文 -->
	<body>

		<h1>ページの見出し（タイトル）が入る</h1> // 「h1要素」もしくは「h1タグ」
		<p>ここにはテキストが入る</p>　// 「p要素」もしくは「pタグ」
		
		// 1行のコメントアウト
		<!-- 
		複数行のコメントアウト	
		-->
	</body>

</html>
```

* HTML構造
	* DOCTYPE
		* このファイルの宣言をする
	* `<html lang="ja">` - 日本語で書きますという宣言をする
		* lang - language（言語）の略
		* ja - japan（日本）の略
	* `<meta charset="utf-8">` - 文字化けをしないように文字コードを設定する
		* utf-8 - ユーティーエフエイトと読む
	* `<head>` - 頭（ヘッド）のことでこのページの情報などを入れる
		* 画面には表示はされない（目に見えない）
	* `<body>` - 体（ボディ）のことで実際に表示したい（見せたい）ものを書く
		* 画面に表示される（目に見える）
	* コメントアウト - 意図的に表示しないようにする
		* // 1行のコメントアウト
		* <!-- 複数行のコメントアウト -->

* テキスト
	* `<title>` - ページのタイトル情報を書く
		* 画面（ウィンドウ）の一番上に表示される
	* `<h1>` - 見出し（タイトル）
		* `<h1> ~ <h6>` まである
		* 数字が小さいほど文字が大きくなる
		* `<h1>`が一番大きくて`<h6>`が一番小さい
	* `<p>` - 見出しまでにはいかないテキスト


####CSSを書いて装飾してみよう

* `<style></style>`タグで囲まれた部分にCSSを書く

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

		<h1>ページの見出し（タイトル）が入る</h1>
		<p>ここには赤文字のテキストが入る</p>

	</body>

	<!-- ここにCSS(装飾するコード)を書いていく -->
	<style>
		p {
			color: red;
		}
	</style>

</html>
```

プロパティ名（特性・特質）: 変化させたい値;
color: blue;

【読み方】 
「:」 → 「コロン」
「;」 → 「セミコロン」

#実際の使われ方

```
HTMLの要素名 {
	プロパティ名: 変化させたい値;
}
↓
p {
	color: blue;
}
// p要素が青文字になる
```

##### color - 文字の色を変える
【読み方】 
「color」 → 「カラー」

【意味】 
* 文字の色

* 参考：<a href="http://www.htmq.com/style/color.shtml" target="_blank">http://www.htmq.com/style/color.shtml</a>

プロパティ名（特性・特質）: 変化させたい値;

```
文字の色: 青にする;
↓
color: blue;
```

* カラーコード
	* プログラムで色を宣言するためのコード（それぞれの色にそれぞれのコードがついている）
		* 黒 - black もしくは #000000
		* 白 - white もしくは #FFFFFF
		* 赤 - red もしくは #FF0000
		* 緑 - green もしくは #00FF00
		* 青 - blue もしくは #0000FF
		* 色んな色を指定できる
			* 参考：<a href="http://hogehoge.tk/webdev/color/" target="_blank">http://hogehoge.tk/webdev/color/</a>

##### background-color - 背景色を変えよう

【読み方】 
「background-color」 → 「バックグラウンドカラー」

【意味】 
* 背景色

* 参考：<a href="http://www.htmq.com/style/background-color.shtml" target="_blank">http://www.htmq.com/style/background-color.shtml</a>


プロパティ名（特性・特質）: 変化させたい値;

```
#実際の使われ方
background-color: blue;
↓
背景色: 青にする;
p {
	background-color: blue;
}
```

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

		<p>赤い背景色</p>

	</body>

	<!-- ここにCSS(装飾するコード)を書いていく -->
	<style>
		p {
			background-color: red;
		}
	</style>

</html>
```

#####複数のプロパティを使う

#「color」プロパティと「background-color」プロパティを一緒に使ってみよう


```
p {
	color: red;
	background-color: blue;
}
```

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

		<p>赤い文字色と青い背景色</p>

	</body>

	<!-- ここにCSS(装飾するコード)を書いていく -->
	<style>
		p {
			color: red;
			background-color: blue;
		}
	</style>

</html>
```

##### 選択した要素が全部変わってしまう

```html
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p>この文字を赤色にしたい</p>
		<p>この文字を青色にしたい</p>

	</body>

	<style>
		p {
			color: red;
		}
		p {
			color: blue;
		}
	</style>

</html>
```
↑どちらも同じ色になってしまう

##これをどうやって解決しよう？

