##aタグの使い方(つかいかた)

####リンクを指定(してい)する！
- 記述例(きじゅつれい)<br>
`<a href="http://bunbu.co.jp">Bunbu学院</a>`
	- aタグはアンカーの略(りゃく)です。
	- `href=""`でリンク先を指定します。
	- 他(ほか)のタグと同じでid名やclass名を指定することもできます。

- 画像(がぞう)をリンクにしたい時<br>
`<a href="http://bunbu.co.jp"><img src="bunbu.png"></a>`
	- リンクにしたい画像をaタグでくくります。

- リンク先を別ウィンドウで開きたい時<br>
`<a href="http://bunbu.co.jp" target="_blank">Bunbu学院</a>`
	- target属性(ぞくせい)に`_blank`を指定する。

- 文章中(ぶんしょうちゅう)の文字からリンクさせたい時<br>
`<p>Bunbu学院のサイトは<a href="http://bunbu.co.jp">こちら</a></p>`
	- aタグを文章中で使うことができます。

- リンクする文字の色を変える時
	- aタグは何もCSSを指定していないと文字の色が青、一度リンクしたことがある時は紫(むらさき)になっています。
	- また、下線(下の線)があります。
	- 他のタグと同じくCSSでスタイル(見た目)を変えることができます。
	- 下線を消す場合には`text-decoration`プロパティで`none`と指定します。
	- コードの例
	
	```
	<!DOCTYPE html>
	<html>
	  <head>
	    <meta charset="utf-8">
	    <title>リンクの練習</title>
	  </head>
	  <style>
	    .link {
	      color: red;
	      text-decoration: none;
	    }
	  </style>
	  <body>
	    <a href="http://bunbu.co.jp" class="link">Bunbu学院</a>
	  </body>
	</html>
	```



####ページ内リンクを指定する！
- ページ内リンクとは？
	- 同じページ内を移動(いどう)させること。 
	- 1ページの内容(ないよう)が増えてくるとスクロールして目的の内容を探(さが)すのが大変になる。
	- ページの下から一番上に戻(もど)りたい時によく使う。(例：[http://porte-web.com](http://porte-web.com))
- ページ内リンクの作り方
	- アンカー(めじるし)を作る
		- `<div id="hoge">内容</div>` 
		- リンク先の要素にid名を指定する。

	- アンカーへのリンクを作る
		- `<a href="#hoge">hogeへリンクする</a>`
		- href属性に作ったid名を入れる(idなのでid名の前に#を入れる)

- コードの例
	
	```
	<!DOCTYPE html>
	<html>
	  <head>
	    <meta charset="utf-8">
	    <title>ページ内リンクの練習</title>
	  </head>
	  <style>
	    #top {
	      height: 1000px;
	    }
	  </style>
	  <body>
	    <div id="top">
	      ページのトップ
	    </div>
		
	    <a href="#top">トップへ</a>
	  </body>
	</html>
	```
		



