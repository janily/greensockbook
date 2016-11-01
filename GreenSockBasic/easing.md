# 缓动曲线

TweenMax提供了下面这些运动曲线：

1、Back 2、SlowMo 3、StppedEase 4、RoughEase 5、Bounce 6、Circ 7、Elastic 8、Expo 9、Sine

具体曲线运动效果，可以去[这个地址](http://greensock.com/ease-visualizer)看看：

![](http://ww4.sinaimg.cn/large/0060lm7Tgw1f997n29r9vg30nj0l6n5p.gif)

下面我们添加一个bounce曲线，看看实际效果(点击右下角的return按钮查看效果)：

```
TweenLite.fromTo($box, 2, {x: '-=200px'}, {x: 150, ease: Bounce.easeOut});
```

<p data-height="300" data-theme-id="17491" data-slug-hash="JRQoNv" data-default-tab="js,result" data-user="janily" data-embed-version="2" data-pen-title="JRQoNv" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/JRQoNv/">JRQoNv</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

可以看到，加了曲线之后，动画有了弹动的效果。

在实际开发中，开发动画效果都会在动画过程中做一些其它的操作，这个时候就要用到回调函数了。TweenMax提供了在动画各个阶段的回调方法，使用起来非常方便。

请看下一章节。


