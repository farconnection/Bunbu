##オシャレな今どきボタンを作ろう！
今回はaタグの応用としてCSSで今どきなボタンデザインをCSSで作っていきます。<br>
[参考サイト](http://www.nxworld.net/tips/css-only-button-design-and-hover-effects.html)<br>
自分のサイトの一番下に「トップへ戻る」ボタンを作ります。

###まずはHTMLを書く
自分のサイトの一番下に以下のようなHTMLを書きます。

```
<div class="button_area">
	<a href="#top">トップへ戻る</a>
</div>

```

###CSSを書く
次にCSSを指定します。<br>
さきほど書いたHTMLにスタイルを指定します。

```
.button_area {
  margin: 20px 0;
  text-align: center;
}

.button_area a {
  background: blue;
  //transparentは色を透明にする
  //透明な1pxのボーダー
  border: 1px transparent solid;
  color: white;
  text-decoration: none;
  display: inline-block;
  padding: 10px 15px;
}

```
上のコードでは`button_area`の余白を指定し、aタグの背景色、ボーダー、文字色、paddingを指定しています。

####なぜaタグを`display: inline-block;`してるの？
aタグは最初の状態だとinlineです。<br>
しかし、inlineのままだとmarginやpaddingが正しく適用されません。<br>
これらの理由から`display: inline-block;`でinline-block扱いにしています。

###マウスをかざした時のCSSを書く
次にマウスをかざした時のCSSを書きます。<br>
かざした時などの特定の状態のCSSを指定するために`擬似クラス`を使用します。
####擬似(ぎじ)クラスとは？
擬似クラスは、要素が特定の状態の場合にスタイルを指定するものです。<br>
よく使われる例として、hover(マウスをかざした時)、visited(一度アクセスしたことがある場合)などがあります。<br>
今回は、マウスをかざした時に文字の色と背景色を入れ替えます。<br>
基本的に擬似クラスには今の状態から変えたいプロパティのみを指定します。<br><br>

下のCSSを追加します。

```
//.button_area aにマウスをかざした時
.button_area a:hover {
  background: white;
  border: 1px blue solid;
  color: blue;
}
```

##問題
###「トップへ戻る」ボタンの下に新しい「Bunbuのサイトへ」ボタンを作ろう!!!!

####ホバー前
	・背景の色(はいけいしょく)が赤色
	・文字の色が白色
	・ボーダーの色が黒色(black)で線の太さが1pxの実線(じっせん)

####ホバー時
	・背景の色が白色
	・文字の色が赤色
	・ボーダーの色が赤色で線の太さが1pxの実線

クリックをしたらBunbu学院のサイト(http://bunbu.co.jp)に別ウィンドウでリンクするボタンを作る！(クリックしやすさも考える)

###問題の答え
####HTMLの例
```
<div class="button2">
	<a href="http://bunbu.co.jp" target="_blank">Bunbuのサイトへ</a>
</div>
```


####CSSの例
```
.button2 {
  text-align: center;
  margin: 20px;
}

.button2 a {
  background: red;
  color: white;
  border: 1px black solid;
  text-decoration: none;
  padding: 10px 15px;
  display: inline-block;
}

.button2 a:hover{
  background: white;
  color: red;
  border: 1px red solid;
}
```


##トップへ戻るボタンをページの下に固定する
トップへ戻るボタンがずっとページの下に固定されるようにするために、`position`プロパティを使って指定します。

###positionプロパティとは
positionプロパティとは、要素の配置方法を指定するためのプロパティです。何も指定しないと特に配置方法を指定しない`static`が指定されています。<br>

今回はページの下に常に固定したいので、絶対位置への配置になりスクロールをしても固定されたままになる`fixed`を指定します。<br>

他にも`relative`と`absolute`があり、`relative`は相対位置への配置となり`static`を指定した時の位置が基準値になります。
`absolute`は`fixed`と同じく絶対位置への配置となり、親ボックスに`static`以外が指定されている場合は、その親ボックスの左上が基準となります。<br>

絶対配置をする`absolute`と`fixed`を指定した場合は、表示する位置を`top` `bottom` `left` `right`プロパティで指定します。

###実際に試してみよう！
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Positionの例</title>
  </head>

  <style>
    body {
      height: 2000px;
    }

    .oya {
      position: relative;
      width: 500px;
      height: 100px;
      background: salmon;
    }

    span {
      color: slateblue;
    }

    .sample1 {
      position: static;
    }

    .sample2 {
      position: relative;
      top: 10px;
      left: 10px;
    }

    .sample3 {
      position: absolute;
      top: 10px;
      left: 10px;
    }

    .sample4 {
      position: fixed;
      top: 10px;
      left: 10px;
    }
  </style>

  <body>
    <p class="oya">
      position:staticの場合<span class="sample1">staticの場合</span>
    </p>

    <p class="oya">
      position:relativeの場合<span class="sample2">relativeの場合</span>
    </p>

    <p class="oya">
      position:absoluteの場合<span class="sample3">absoluteの場合</span>
    </p>

    <p class="oya">
      position:fixedの場合<span class="sample4">fixedの場合</span>
    </p>
  </body>
</html>
```

###実際にトップへ戻るボタンを固定する
トップへ戻るボタンをページの右下に固定します。<br>
下のCSSを追加します。

```
.button {
	position: fixed;
	bottom: 10px;
	right: 10px;
}
```

