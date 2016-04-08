#4月22日（金曜日）

##実際に作ってみよう

####必要な知識
* htmlファイル
	* これがホームページ等になり公開される
	* WEBサイトの基盤となる枠組みのようなもの
* css
	* htmlに色をつけたり、文字を大きくしたり小さくしたり装飾できるもの

###作ってみよう

####index.html作成 - サイトの入り口となるファイルを作成
#####html要素
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

	</body>

</html>
```

* HTML構造
	* DOCTYPE
		* このファイルの宣言をする
* テキスト
	* h - タイトル
		* h1 ~ h6 まである
		* 一般的には最高h4ぐらいまでしか使われない
	* p - タイトルまでにはいかないテキスト


####CSSを書いて装飾してみよう

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

		<h1>ページのタイトルが入る</h1>
		<p>ここには赤文字のテキストが入る</p>

	</body>

	<!-- ここにcss(装飾するコード)を書いていく -->
	<style>
		p {
			color: red;
		}
	</style>

</html>
```

```
プロパティ名: 変化させたい値;
color: blue;

【読み方】 
: →「コロン」
; →「セミコロン」

#実際の使われ方
HTMLの要素名 {
	プロパティ名: 変化させたい値;
}
↓
p {
	color: blue;
}
// HTML内のp要素が青文字になる
```

##### color - 文字の色を変える
```
プロパティ名（特性・特質）: 変化させたい値;
color: blue;
↓
文字の色: 青にする;
```

* カラーコード
	* プログラムで色を宣言するためのコード（それぞれの色にそれぞれのコードがついている）
		* 黒 - black もしくは #000000
		* 赤 - red もしくは #FF0000
		* 青 - blue もしくは #0000FF
		* オレンジ - orange もしくは #FFA500
		* 白 - white もしくは #fff
		* 色んな色を指定できる
			* <a href="http://hogehoge.tk/webdev/color/" target="_blank">http://hogehoge.tk/webdev/color/</a>


##### background - 背景色を変えよう
```
プロパティ名（特性・特質）: 変化させたい値;
background: blue;
↓
背景色: 青にする;

#実際の使われ方
p {
	background: blue;
}
```

#####複数のプロパティを使う
```
p {
	color: red;
	background: blue;
}
```


##### border - 枠を付けよう
```
プロパティ名（特性・特質）: 変化させたい値;
border: 1px solid blue;
↓
枠線: 1ピクセルの1本線を青色にする;

border: 5px dotted red;
↓
枠線: 5ピクセルの点線を赤色にする;
```

* px - ピクセル単位
	* 1px(イチピクセル)
	* 太さを示す

* 線の形状
	* solid（ソリッド） - 1本線で表示されます。
	* double（ダブル） - 2本線で表示されます。
	* dashed（ダッシュ）- 破線で表示されます。
	* dotted（ドット） - 点線で表示されます。

* 参考：<a href="http://www.htmq.com/style/border.shtml" target="_blank">http://www.htmq.com/style/border.shtml</a>

##### text-align - 文字を寄せよう
```
プロパティ名（特性・特質）: 変化させたい値;
text-align: center;
↓
文字の寄せ方を: 中央に寄せる;

text-align: right;
↓
文字の寄せ方を: 右に寄せる;
```

* 値の種類
	* left - 左に寄せる
	* right - 右に寄せる
	* center - 中央に寄せる


##### 選択した要素が全部変わってしまう
```
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
		* 「#」 - CSSではシャープで表現
		* 1つのHTML内で1つしか付けれない名前
	* class - クラス
		* 「.」 - CSSではドットで表現
		* 1つのHTML内で複数使える名前

```html
使い方
<h1 id="title">タイトルにIDをつけました</h1>
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


実際の例
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