###ボックスで遊ぼう！

####ボックスからはみ出しちゃったらどうなるの？

* overflow（オーバーフロー）
	* ボックスの範囲内（はんいない）に入りきらない場合に、はみ出た部分の表示の仕方を指定する。
		* visible - ボックスからはみ出して表示される。これが初期値です。尚、Internet Explorerでは、内容がはみ出すのではなく、ボックスの方が内容に合わせて広がります。
		* scroll - 入りきらない内容はスクロールして見られるようになります。
		* hidden - はみ出た部分は表示されません。
		* auto - ブラウザに依存（いぞん）します（一般的にはスクロールして見られるようになります）。

* 参照：<a href="http://www.htmq.com/style/overflow.shtml</a>

```
<!DOCTYPE html>　
<html>

	<!-- ここからが本文 -->
	<body>

		<div class="box1">
			<p>visiblevisiblevisible</p>
		</div>
		<div class="box2">
			<p>scrollscrollscrollscroll</p>
		</div>
		<div class="box3">
			<p>hiddenhiddenhiddenhidden</p>
		</div>
		<div class="box4">
			<p>autoautoautoautoautoauto</p>
		</div>

	</body>

	<style>
		.box1,
		.box2,
		.box3,
		.box4 {
			width: 100px;
			height: 100px;
			margin: 10px;
		}
		.box1 {
			overflow: visible;
			background: red;
		}
		.box2 {
			overflow: scroll;
			background: blue;
		}
		.box3 {
			overflow: hidden;
			background: greeen;
		}
		.box4 {
			overflow: auto;
			background: orange;
		}
	</style>

</html>
```

<br>
---
<br>


####ボックスの位置を変更してみよう

* position（ポジション）
	* ボックスの配置方法（基準位置）が、相対位置か絶対位置かを指定する際に使用する。
	* 相対位置って？絶対位置って？
	* positionプロパティで指定するのは、配置方法（基準位置）のみなので実際の表示位置の指定には、top、bottom、left、rightを併用して、基準位置からの距離を設定する。
		* static - 特に配置方法を指定しない。この値のときには、top、bottom、left、rightは適用されない。これが初期値になる。
		* relative - 相対位置への配置となる。positionプロパティでstaticを指定した場合に表示される位置が基準位置となる。
		* position - 絶対位置への配置となる。親ボックスにpositionプロパティのstatic以外の値が指定されている場合には、親ボックスの左上が基準位置となる。親ボックスにpositionプロパティのstatic以外の値が指定されていない場合には、ウィンドウ全体の左上が基準位置となる。
		* fixed - 絶対位置への配置となるのはabsoluteと同じだが、スクロールしても位置が固定されたままとなる。

* 参照：<a href="http://www.htmq.com/style/position.shtml</a>

```
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<div class="box1"></div>
		<div class="box2"></div>
		<div class="box3">
			<div class="box3-1"></div>
		</div>
		<div class="box4"></div>

	</body>

	<style>
		.box1,
		.box2,
		.box3,
		.box3-1,
		.box4 {
			width: 300px;
			height: 100px;
		}

		.box1 {
			background: red;
			position: static;
			margin: 100px
		}
		.box2 {
			background: blue;
			position: relative;
			margin: 100px;
		}
		.box3 {
			background: green;
			position: relative;
			margin: 100px
		}
		.box3-1 {
			background: pink;
			position: absolute;
			top: 30px;
			left: 30px;
		}
		.box4 {
			background: skyblue;
			position: fixed;
			top: 0;
			right: 0;
		}
	</style>

</html>
```

<br>
---
<br>

####ボックスを3Dにしてみよう

* box-shadow（ボックスシャドウ）
	* ボックスに影をつける。

* 参照：<a href="http://www.htmq.com/css3/box-shadow.shtml</a>

```
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<div class="box1">box-shadow: 10px 10px</div>
		<div class="box2">box-shadow: 10px 10px 10px</div>
		<div class="box3">box-shadow: 10px 10px 10px 10px</div>
		<div class="box4">box-shadow: 10px 10px 10px 10px inset</div>

	</body>

	<style>
		.box1,
		.box2,
		.box3,
		.box4 {
			width: 400px;
			height: 100px;

		}
		.box1 {
			background: red;
			box-shadow: 10px 10px;
		}
		.box2 {
			background: blue;
			box-shadow: 10px 10px 10px;
		}
		.box3 {
			background: pink;
			box-shadow: 10px 10px 10px 10px;
		}
		.box4 {
			background: skyblue;
			box-shadow: 10px 10px 10px 10px inset;
		}
	</style>

</html>
```


