# 链式动画

使用过jquery都知道，jquery又一个很强大的特性即链式操作，比如：


```
$("#myphoto").css("border","solid 2px#FF0000").attr("alt"," good");
```

对一个jQuery对象先调用了css()函数修改样式，然后使用attr()函数修改属性，这种调用方式象链一样，所以称为"链式操作"。

链式操作能够让代码变得简洁，因为往往可以在一条语句中实现以往多条语句才能完成的任务。

同样在GreenSock中也支持类似jquery一样的链式动画操作，先来看实例：

<p data-height="300" data-theme-id="17491" data-slug-hash="jWwBaE" data-default-tab="result" data-user="janily" data-embed-version="2" data-pen-title="jWwBaE" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/jWwBaE/">jWwBaE</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

来看看代码：

```
tl.to(".green", 1, {x:750})
  .to(".blue", 1, {x:750})
  .to(".orange", 1, {x:750})
```

是不是跟jquery的链式操作很相似，所有的动画效果是一个接着一个运行的，即链式动画。

GreenSock不仅提供了像这种方便的链式动画操作，而且还提供了各种动画的控制方法，比如播放、暂停等方法可以更加灵活的来对动画进行控制。

下一章节将介绍动画的控制。

