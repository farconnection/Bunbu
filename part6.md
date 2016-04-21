#パート６

####タイピングをできるようになろう！
* ローマ字表
	* <a href="http://happylilac.net/roman-hyo3.pdf" target="_blank">http://happylilac.net/roman-hyo3.pdf</a>
* ホームポジション
	* <a href="http://typing.twi1.me/training/basic" target="_blank">http://typing.twi1.me/training/basic</a>
* タイピング
	* <a href="http://kids.nifty.com/cs/game/detail/91125000012/1.htm" target="_blank">http://kids.nifty.com/cs/game/detail/91125000012/1.htm</a>

####おさらい
* 「border」プロパティは何をするプロパティだったっけ？
* 「px」ってなんだっけ？
* 「text-align」プロパティは何をするプロパティだったっけ？
* 「id」は1つのHTML内でいくつ使える？
* 「class」は1つのHTML内でいくつ使える？


####HTMLに画像を表示しよう
	* img - イメージ要素（タグ）
		* 画像を表示できる
		* src : 画像のファイル名
		* alt : 画像の説明（必ず入れる必要はない）
		* 閉じタグがない

```
html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<img src="（画像のファイル名）" alt="（画像の説明）">

	</body>

</html>
```

* 実際の例
	* りんごの画像を「apple.jpg」というファイル名でダウンロードした場合
	<img src="apple.jpg" alt="りんご">


#####ダウンロードの仕方
* 使いたい画像があったら右クリック
	* Windowsの人
		*「名前を付けて保存」をクリック
	* Macの人
		*「画像を保存」をクリック
	* ファイル名を付けて、index.htmlと同じ階層（場所）に保存


#### margin,padding - 隙間を作ろう

【読み方】 
「margin」 → 「マージン」
「padding」 → 「パディング」

【意味】 
「margin」→ 要素の外側の余白
「padding」→ 要素の内側の余白

* 参考：<a href="http://www.htmq.com/style/margin.shtml" target="_blank">http://www.htmq.com/style/margin.shtml</a>
* 参考：<a href="http://www.htmq.com/style/padding.shtml" target="_blank">http://www.htmq.com/style/padding.shtml</a>


```
html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="bg_black">黒いボックス</p>
		<p class="bg_blue">青いボックス</p>
		<p class="bg_red">赤いボックス</p>

	</body>

	<style>
		.bg_black {
			background-color: black;
			margin: 10px;
		}
		.bg_blue {
			background-color: blue;
			padding: 10px;
		}
		.bg_red {
			background-color: red;
			padding: 10px;
			margin: 10px;
		}
	</style>

</html>
```


<br>
---
<br>


#### width,height - 横幅と高さを指定しよう

【読み方】 
「width」 → 「ウィズ」
「height」 → 「ハイト」

【意味】 
「width」→ 横幅
「height」→ 高さ

* 参考：<a href="http://www.htmq.com/style/width.shtml" target="_blank">http://www.htmq.com/style/width.shtml</a>
* 参考：<a href="http://www.htmq.com/style/height.shtml" target="_blank">http://www.htmq.com/style/height.shtml</a>

```
html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="bg_black">黒いボックス</p>
		<p class="bg_blue">青いボックス</p>
		<p class="bg_red">赤いボックス</p>

	</body>

	<style>

		.bg_black {
			background: block;
			width: 100px;
		}
		.bg_blue {
			background: blue;
			height: 100px;
		}
		.bg_red {
			background: red;
			width: 100px;
			height: 100px;
		}

	</style>

</html>
```


####HTMLとCSSを分けよう
* フォルダ分け（style.css, images）
	* HTMLのコード量が多くなるため、HTMLとCSSとでそれぞれファイルを分ける
	* <link href="（cssファイル名）" rel="stylesheet" type="text/css">
		* cssがstyle.cssの場合
		* <link href="style.css" rel="stylesheet" type="text/css">

```
html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
		<link href="style.css" rel="stylesheet" type="text/css">
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="bg_black">ここにはテキストが入る</p>
		<p class="bg_blue">ここにはテキストが入る</p>

	</body>

</html>
```

```
css
style.css

.bg_black {
	background: red;
	width: 100px;
}
.bg_black {
	background: blue;
	height: 100px;
}

```

## <style></style>タグがいらない

<br>
---
<br>

####フォントをより装飾しよう
* font-size（フォントサイズ）
	* フォントの大きさを指定する
	* 単位はpx
* font-family（フォントファミリー）
	* フォントの種類 
		* sans-serif（サンセリフ） - ゴシック系のフォント
		* serif（セリフ） - 明朝系（みんちょうけい）のフォント
		* cursive（カーシブ） - 筆記体（ひっきたい）・草書体のフォント
		* fantasy（ファンタジー） - 装飾的（そうしょくてき）なフォント
		* monospace（モノスペース） - 等幅フォント
* font-weight（フォントウェイト）
	* フォントの太さを指定する
		* normal（ノーマル） - 標準の太さ
		* bold（ボールド）- 太字
		* lighter（ライター） - 相対的に一段階細くする。
		* bolder（ボールダー） - 相対的に一段階太くする。
* text-shadow（テキストシャドウ）
	* フォントに影をつける
	* text-shadow: 横軸 縦軸 ぼかし具合 ぼかす色;
	* text-shadow: 1px 1px 10px red;


```
html
<!-- DOCTYPE宣言 - 「このファイルはhtmlですよ」と宣言する -->
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
		<link href="style.css" rel="stylesheet" type="text/css">
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="bg_black">ここにはテキストが入る</p>
		<p class="bg_blue">ここにはテキストが入る</p>

	</body>

</html>
```

```css
style.css

.bg_black {
	font-family: serif;
	font-size: 20px;
	font-weight: bold;
	text-shadow: 1px 1px 10px red;
}

```

#### ul,ol,li - リストを使う
* ul、ol、li - 何かを並べたいときに使用する
	* ul、li - 箇条書きリスト
		* ul要素（タグ）の中にli要素（タグ）を書く
	* ol、li - 番号付きリスト
		* olタグの中にliタグを書く
		* ul要素（タグ）の中にli要素（タグ）を書く

###親要素と子要素
```
* HTMLは要素（タグ）の中に要素（タグ）があって、またその中に要素（タグ）があるというような階層構造（かいそうこうぞう）、になっている。

<タグ1><タグ2>要素の内容</タグ2></タグ1>

<タグ1>要素＝<タグ1>～</タグ1>（この場合は全体）
<タグ2>要素＝<タグ2>要素の内容</タグ2>

このとき、<タグ1>要素を、<タグ2>要素に対する親要素と言います。逆に<タグ2>要素を、<タグ1>要素に対する子要素と言います。
```

```
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<ul>
			<li>リスト１</li>
			<li>リスト２</li>
			<li>リスト３</li>
			<li>リスト４</li>
			<li>リスト５</li>
			<li>リスト６</li>
			<li>リスト７</li>
			<li>リスト８</li>
		</ul>

	</body>

	<style>
		ul {
			list-style-type: circle;
		}
	</style>

</html>
```


* 参照： <a href="http://www.htmq.com/style/list-style.shtml" target="_blank">http://www.htmq.com/style/list-style.shtml</a>
	* list-style-type
		* <a href="http://www.htmq.com/style/list-style-type.shtml" target="_blank">http://www.htmq.com/style/list-style-type.shtml</a>


<br>
---
<br>


####要素を横並びにしよう

#####その前にブロック要素とインライン要素の説明

* ブロック要素
	* 文書の骨組み
	* 要素の幅が100%
	* <div>, <h1>~<h6>, <p>
* インライン要素
	* 行の中の文字に意味を持たせることが出来る
	* 要素の幅が要素の中身分の幅
		* 横並びにすることが出来る性質を持っている
	* <img>, <span>


```
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="text1"><span class="red">赤字</span>にしたり、<span class="bold">太字</span>にしたり出来るよ</p>

		<span class="text2">インライン要素１</span>
		<span>インライン要素２</span>
		<span>インライン要素３</span>

	</body>

	<style>
		//text1内の要素
		.text1 {
			background: gray;
		}
		.red {
			color: red;
		}
		.bold {
			font-weight: bold;
		}

		//text2内の要素
		.text2 {
			color: white;
			background: blue;
		}
		.text2 {
			list-style-type: circle;
		}
	</style>

</html>
```

* 参照： <a href="http://www.htmq.com/htmlkihon/005.shtml" target="_blank">http://www.htmq.com/htmlkihon/005.shtml</a>


#####横並びにしてみよう

* display


```
<!DOCTYPE html>　
<html>

	<!-- ここからが本文 -->
	<body>

		<p class="text1"><span class="red">赤字</span>にしたり、<span class="bold">太字</span>にしたり出来るよ</p>
		<p class="text1"><span class="red">赤字</span>にしたり、<span class="bold">太字</span>にしたり出来るよ</p>
		<p class="text1"><span class="red">赤字</span>にしたり、<span class="bold">太字</span>にしたり出来るよ</p>

	</body>

	<style>
		//text1内の要素
		.text1 {
			display: inline-block; //横並びにしてみる
			background: gray;
		}
		.red {
			color: red;
		}
		.bold {
			font-weight: bold;
		}
	</style>

</html>
```

