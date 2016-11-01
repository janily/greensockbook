# 回调方法

首先以.fromTo()方法来说明回调的使用用法。

比如，我们想要在动画开始的时候来触发回调函数。首先来创建一个start的函数：


```
function start(){
  console.log('start');
}
```

触发回调函数，只需要添加这句代码就可以了onStart:start就可以了，非常简单吧。


```
TweenLite.fromTo($box, 2, {y: '-=200px'}, {y: 100, ease: Bounce.easeOut,onStart:start});
```

打开开发者工具，就可以看到输出的相关信息。

你也可以添加onUpdate和onComplete来触发对应的回调函数：

```
function start(){
  console.log('start');
}
function update(){
  console.log('animating');
}
function complete(){
  console.log('end');
}
```

<p data-height="300" data-theme-id="17491" data-slug-hash="wzLBPa" data-default-tab="js,result" data-user="janily" data-embed-version="2" data-pen-title="wzLBPa" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/wzLBPa/">wzLBPa</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

如下图所示，可以看到在每一个阶段都执行了指定的回调方法。

![](http://ww2.sinaimg.cn/large/0060lm7Tgw1f998q07951j308q025glh.jpg)

OK，到目前为止，我们开发的动画都是针对单个元素的运动。在实际开发中有时候需要多个元素一起运动，只是运动的属性的值不同而已，比如像下面这样的动画：

![](http://ww1.sinaimg.cn/large/0060lm7Tgw1f99982ulhug30hq0crt9w.gif)

这就是下一章节要讲的。





