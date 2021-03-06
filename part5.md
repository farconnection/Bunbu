#パート５

####タイピングをできるようになろう！
* ローマ字表
	* <a href="http://happylilac.net/roman-hyo3.pdf" target="_blank">http://happylilac.net/roman-hyo3.pdf</a>
* ホームポジション
	* <a href="http://typing.twi1.me/training/basic" target="_blank">http://typing.twi1.me/training/basic</a>
* タイピング
	* <a href="http://kids.nifty.com/cs/game/detail/91125000012/1.htm" target="_blank">http://kids.nifty.com/cs/game/detail/91125000012/1.htm</a>


####おさらい
* 「<」と「>」で囲まれたものをなんと呼ぶ？
* CSSは何タグの中で書く？
* なんて読む？
	* 「:」→「◯◯◯」
	* 「;」→「◯◯◯◯◯」
* 「color」プロパティは何をするプロパティだったっけ？
* 「background-color」プロパティは何をするプロパティだったっけ？

##### 選択した要素が全部変わってしまう
```
html
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

#####それぞれのHTML要素に名前を付けてあげる

* HTMLの要素ごとに名前を付けてあげることで名前ごとでCSSを指定出来る
	* id - アイディー
		* 「#」 - cssではシャープで表現
		* 1つのHTML内で1つしか付けれない名前
	* class - クラス
		* 「.」 - cssではドットで表現
		* 1つのHTML内で複数使える名前

```

##使い方
<h1 id="title">見出し（タイトル）にIDをつけました</h1>
<p class="red">この文字を赤色にしたい</p>
<p class="blue">この文字を青色にしたい</p>


<style>
	#title {
		color: orange;
	}
	.red {
		color: red;
	}
	.blue {
		color: blue;
	}
</style>
```

##今までとの違い
```
p {
	color: red;
}
↓
.red {
	color: red;
}
```
*「要素」が「class」(「id」)に変わっただけ


実際の例
```
html
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<h1 id="title">タイトルにIDをつけました</h1>
		<p class="red">この文字を赤色にしたい</p>
		<p class="blue">この文字を青色にしたい</p>

	</body>

	<style>
		#title {
			color: orange;
		}
		.red {
			color: red;
		}
		.blue {
			color: blue;
		}
	</style>

</html>
```

##### border - 枠を付けよう
【読み方】 
「border」 → 「ボーダー」

【意味】
・枠線

* px - ピクセル単位
	* 1px(イチピクセル)
	* 太さを示す

* 線の形状
	* solid（ソリッド）- 1本線で表示されます。
	* double（ダブル）- 2本線で表示されます。
	* dashed（ダッシュ）- 破線で表示されます。
	* dotted（ドット）- 点線で表示されます。

* 参考：<a href="http://www.htmq.com/style/border.shtml" target="_blank">http://www.htmq.com/style/border.shtml></a>

```
プロパティ名（特性・特質）: 変化させたい値;
border: 1px solid blue;
↓
枠線: 1ピクセルの1本線を青色にする;

border: 5px dotted red;
↓
枠線: 5ピクセルの点線を赤色にする;
```

```
html
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="solid">3ピクセルの赤い1本の枠線</p>
		<p class="double">3ピクセルの青い2本の枠線</p>
		<p class="dashed">3ピクセルの黒い破線の枠線</p>
		<p class="dotted">3ピクセルのオレンジ色の点線の枠線</p>

	</body>

	<style>
		.solid {
			border: 3px solid red;
		}
		.double {
			border: 3px double blue;
		}
		.dashed {
			border: 3px dashed black;
		}
		.dotted {
			border: 3px dotted orange;
		}
	</style>

</html>
```

##### text-align - 文字を寄せよう

【読み方】 
「text-align」 → 「テキストアライン」

【意味】
・文字の寄せ方

* 値の種類
	* left - 左に寄せる
	* right - 右に寄せる
	* center - 中央に寄せる

* 参考：<a href="http://www.htmq.com/style/text-align.shtml" target="_blank">http://www.htmq.com/style/text-align.shtml</a>

```
プロパティ名（特性・特質）: 変化させたい値;
text-align: center;
↓
文字の寄せ方を: 中央に寄せる;

text-align: right;
↓
文字の寄せ方を: 右に寄せる;
```

```
html
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<p class="left">左寄せの文字</p>
		<p class="center">真ん中の文字</p>
		<p class="right">右寄せの文字</p>

	</body>

	<style>
		.left {
			text-align: left;
		}
		.center {
			text-align: center;
		}
		.right {
			text-align: right;
		}
	</style>

</html>
```