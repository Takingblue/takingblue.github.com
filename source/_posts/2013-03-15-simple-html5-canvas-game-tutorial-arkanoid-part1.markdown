---
layout: post
title: "Simple HTML5 Canvas Game Tutorial: Arkanoid Part1"
date: 2013-03-15 21:57
comments: true
categories: [HTML5, Javascript]
---
This is a pretty simple game based on HTML5 Canvas and basic javascript. It is easy to learn and just enjoy building it. I think almost everyone know Arkanoid, a little game which goal is to make all bricks disappear by using your little ball to hit them.

Now, we are going to make it by ourselves.
<!--more-->
If you want to take a look the demo. Please refer to [HERE](http://people.cs.nctu.edu.tw/~chenkuo/HTML5/Arkanoid/index.html).
And, [source code of the whole project](https://github.com/Takingblue/Arkanoid-CanvasGame).

Now, build the index.html at first.
``` html index.html
<!DOCTYPE HTML>
<html>
	<head>
		<link rel="stylesheet" href="css/main.css">
		<script src="js/main.js"></script>
	</head>
	<body>
		<canvas id="paintGround">
	    </canvas>
	</body>
</html>
```
It just do the following two things:

1. Create a canvas element with id equals "paintGround" for us to draw on it.
2. Link the simple css file, main.css and our core design javascript file, main.js to our index.html.

Then take a look at main.css.
``` css main.css
body{
    margin:0px;
    padding:0px;
}
#paintGround{
    display:block;
    margin: 50px auto 0 auto;
    border:5px solid;
}
```

Easy and simple, set display:block, adjust position of canvas element to the middle of whole page and add a 5px border for it.

Let's start to write the basic setup for canvas in main.js.
We are going to define the width and height of canvas element. 
``` javascript main.js
window.onload = function()
{
    var canvas = document.getElementById("paintGround");
    var W = 799;
    var H = 600;
    canvas.width = W;
    canvas.height = H;
}
```
Due to the border, you can see the width and height of canvas are already being set up.   
Nice! Start to draw on it!


