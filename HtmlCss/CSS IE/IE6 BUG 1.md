IE6下与float元素相邻的position:absolute元素消失BUG
==================================================
解决方法：只要别让绝对定位元素紧邻浮动元素就可以了。比如可以在绝对定位元素后面加个空元素。

```html
    <!DOCTYPE>
    <html>
    <head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title>IE6下与float元素相邻的position:absolute元素消失BUG</title>
    <style type="text/css">
        *{ margin:0; padding:0}
        .wrap{ width:800px; height:200px; margin:0 auto; position:relative}
        .left{ width:300px; height:200px; background-color:#F00; float:left}
        .right{ width:500px; height:200px; background-color:#00F; float:left}
        .pos{ width:600px; height:30px; background-color:#000; color:#fff; position:absolute; left:0; top:0;}
        .pos2{ top:60px;}
    </style>
    </head>

    <body>
    <div class="wrap"> 
        <div class="pos">如果不加下面的div,在IE6下是看不见我的</div>
        <!--[if IE 6]><div></div><![endif]-->
        <div class="left"></div>
        <div class="right"></div>
         <!--[if IE 6]><div></div><![endif]-->
        <div class="pos pos2">如果不加上面的div,在IE6下是看不见我的，总之是要与浮动之间加个空的DIV</div>  
    </div>
    </body>
    </html>
```    