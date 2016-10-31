# 动画

### TweenLite.to()方法

下面就是让它动起来，可以使用TweenLite.to()方法来使元素动起来。比如，让元素移动到浏览器左边的边缘，我们就可以使用TweenLite.to()方法。

![](http://ww1.sinaimg.cn/large/0060lm7Tgw1f9952txmfcj30hc04zwer.jpg)

在codepen中加入下面的代码：


```
TweenLite.to($box, 0.7, {left: 0});
```
上面的代码会在0.7秒之内把$box元素从CSS中定义的位置移动到body的边缘。如下所示(**点击右下角的return按钮，可以重新运行代码观看效果**)：

<p data-height="300" data-theme-id="17491" data-slug-hash="meypPB" data-default-tab="css,result" data-user="janily" data-embed-version="2" data-pen-title="meypPB" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/meypPB/">meypPB</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

如果没看到效果，可以把鼠标移动到右下角会出现一个return按钮，点击以下就可以重新运行代码，就可以看到效果了。

不过，你应该发现了一个奇怪的小问题。那就是$box元素只有一半露出来了，应该是全部显示的，这是为什么呢？

这是因为我们在CSS中定义了**transform: translate(–50%, –50%)**，这个时候就可以来定义元素的X的值。

> 在GreenSock中，一些CSS属性对应到GreenSock中还是有些不同的。比如transform中translate在GreenSock中使用**x,y**就对应着translate(x,y)。任何的CSS属性需要从有－的写法变为驼峰式的写法。比如background-color修改为backgroundColor等。以及CSS中的transform:rotate()变为rotation。

这个时候我们可以使用TweenLite来定义translate中的x值，如下所示：


```
TweenLite.to($box, 0.7, {left: 0, x: 0});
```

### TweenLite.from方法

**TweenLite.from**顾名思义，就是使元素从指定的属性的值运动到元素的初始值。还是以上一个demo为例子，修改代码如下：


```
TweenLite.from($box, 2, {x: '-=200px', autoAlpha: 0});
```

上面的代码是用来使元素从定义在.from()方法里的位置运动到在CSS中定义的位置。

运行这个例子，我们会看到元素从元素左边200px的位置运动到元素在CSS中定义的位置。

autoAlpha方法是GSAP中一个特别的属性，它把opacity和visibility两个属性合二为一了。

![](http://ww3.sinaimg.cn/large/0060lm7Tgw1f995fy9pdfj30hc090jrw.jpg)

在代码中autoAlpha: 0表示它会把元素初始化为opacity:0;visibility:hidden。当执行动画效果的时候它会把visibility的值设置为inherit以及opacity值设置为1。从而产生一个渐现的效果。

运行下面的demo就可以看到效果：

<p data-height="300" data-theme-id="17491" data-slug-hash="LRKYoe" data-default-tab="js,result" data-user="janily" data-embed-version="2" data-pen-title="LRKYoe" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/LRKYoe/">LRKYoe</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

### TweenLite.set()

有时候，我们只是想设置元素的一些CSS属性并不需要动画效果，比如，重设元素的位置。

这个时候就可以使用GreenSock提供的.set()方法。

去掉我们前面编写的代码除了定义好的$box变量，编写下面的代码：

```
TweenLite.set($box, {x: '-=200px', scale: 0.3});
TweenLite.set($box, {x: '+=100px', scale: 0.6, delay: 1});
TweenLite.set($box, {x: '-50%', scale: 1, delay: 2});
```
运行上面的代码，可以看到元素只是单纯的在改变属性并没有动画效果。

<p data-height="300" data-theme-id="17491" data-slug-hash="ZbYvJE" data-default-tab="js,result" data-user="janily" data-embed-version="2" data-pen-title="ZbYvJE" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/ZbYvJE/">ZbYvJE</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

在上面的代码中，前面两个动画序列我们定义了x属性相对的补间值。

第一个序列把$box元素从CSS中的位置移动到元素左边的200px的位置，然后在第二序列中把元素的位置移动到100px的位置，最后移动到-50%的绝对的补间值。跟默认在CSS中定义的位置一样。

### TweenLite.fromTo()方法

最后来说一说TweenLite.fromTo这个方法。

顾名思义，这个方法我们可以定义元素的起始位置：


```
TweenLite.fromTo($box, 2, {x: '-=200px'}, {x: 150});
```

把上面的代码放入到codepen中，就可以看到运行的动画效果。

<p data-height="300" data-theme-id="17491" data-slug-hash="bwPGXP" data-default-tab="js,result" data-user="janily" data-embed-version="2" data-pen-title="bwPGXP" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/bwPGXP/">bwPGXP</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

我们定义了元素从左边200px的位置开始运动到指定的位置。

x:150会覆盖在CSS中定义的transform: translate(–50%, –50%)的样式，用新的transform: matrix(1, 0, 0, 1, 150, -50);样式来代替。

接下来，可以给元素加一些缓动曲线，使之更符合真实的物体运动效果。GreenSock也提供了各种的运动曲线，来使动画效果更加自然。

请看下一节。







