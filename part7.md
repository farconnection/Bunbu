#パート７

####タイピングをできるようになろう！
* ローマ字表
	* <a href="http://happylilac.net/roman-hyo3.pdf" target="_blank">http://happylilac.net/roman-hyo3.pdf</a>
* ホームポジション
	* <a href="http://typing.twi1.me/training/basic" target="_blank">http://typing.twi1.me/training/basic</a>
* タイピング
	* <a href="http://kids.nifty.com/cs/game/detail/91125000012/1.htm" target="_blank">http://kids.nifty.com/cs/game/detail/91125000012/1.htm</a>

####おさらい
*「margin」プロパティは何をするプロパティだったっけ？
*「padding」プロパティは何をするプロパティだったっけ？

*「width」プロパティは何をするプロパティだったっけ？
*「height」プロパティは何をするプロパティだったっけ？

*「font-size」プロパティは何をするプロパティだったっけ？
*「font-family」プロパティは何をするプロパティだったっけ？
*「font-weight」プロパティは何をするプロパティだったっけ？
*「text-shadow」プロパティは何をするプロパティだったっけ？



###テーブルを作ろう

```
<!DOCTYPE html>　
<html>

	<!-- ページの情報を入力する場所 -->
	<head>
		<title>ページのタイトル情報</title>
	</head>

	<!-- ここからが本文 -->
	<body>

		<table class="menuTable" border="#000" cellspacing="0">
			<tr>
				<th>メニュー</th>
				<th>説明</th>
				<th>豆知識</th>
			</tr>
			<tr>
				<td>カルボナーラ</td>
				<td>玉子とベーコンとクリームソースのパスタ</td>
				<td>カルボナーラとは炭焼き職人という意味</td>
			</tr>
			<tr>
				<td>ペスカトーレ</td>
				<td>エビとあさりの漁師風パスタ</td>
				<td>ペスカトーレは漁師風という意味</td>
			</tr>
		</table>

	</body>

	<style>
		.menuTable {
			width: 500px;
		}
		.menuTable tr th,
		.menuTable tr td, {
			padding: 10px;
		}
		.menuTable tr th {
			font-weight: bold;
			color: #ffffff;
			background: #EE0000;
		}
		.menuTable tr td {
		}
	</style>

</html>
```

<br>
---
<br>


####横並び（みっちり寄せたい場合）

* float（フロート）
	* 指定された要素を左または右に寄せて配置
		* left - 左寄せ
		* right - 左寄せ
* 参照：<a href="http://www.htmq.com/style/float.shtml">http://www.htmq.com/style/float.shtml</a>


```
<!DOCTYPE html>　
<html>

	<!-- ここからが本文 -->
	<body>

		<div class="box1">box1</div>
		<div class="box2">box2</div>
		<div class="box3">box3</div>

	</body>

	<style>
		.box1,
		.box2,
		.box3 {
			float: left;
			text-align: center;
			color: #fff;
		}
		.box1 {
			background: red;
		}
		.box2 {
			background: blue;
		}
		.box3 {
			background: black;
		}
	</style>

</html>
```