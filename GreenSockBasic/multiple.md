# 多个元素运动

### staggered()方法

在实际开发中我们需要使用它来同时运行多个元素执行同一个动画效果的时候，有什么方法呢？

也许可以使用**TimelineLite.to()方法**一个一个的来执行。这样虽然可以达到目的，但是不够优雅。greensock给我们提供了staggered()这一方法来实现，先来看看staggerFrom这个方法的语法：


```
TweenMax.staggerFrom( targets:Array, duration:Number, vars:Object, stagger:Number, onCompleteAll:Function, onCompleteAllParams:Array, onCompleteAllScope:* ) :
```
TweenMax.staggerFrom(targets:目标元素为一个数组,duration:动画执行时间,vars:动画的属性，比如位移、放大缩小以及延迟等,stagger:表示目标数组中的每一个对象动画延迟执行的时间,onCompleteAll:所有的序列动画完成后的回调方法,onCompleteAllParams:传参数给onCompleteAll方法)。

当然这个staggerFrom方法需要使用TweenMax来调用。我们来看GreenSock官方网站的一个实例：

<p data-height="300" data-theme-id="17491" data-slug-hash="vXqEPo" data-default-tab="js,result" data-user="janily" data-embed-version="2" data-pen-title="vXqEPo" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/vXqEPo/">vXqEPo</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

从代码可以看到，使用stagger()方法可以同时操作多个元素来产生动画效果，仅仅只需要一句代码方便好使。

### staggerFrom()方法使用高级技巧cycle

像上面的例子，我们只能一次赋予一个属性一个值，如x:100, rotation:90。如果我们想一次性让元素的属性能随机的随指定的值来运动，就可以使用到taggerFrom()方法中的cycle来达到目的，如下实例所示：

<p data-height="395" data-theme-id="17491" data-slug-hash="bEarQM" data-default-tab="result" data-user="janily" data-embed-version="2" data-pen-title="bEarQM" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/bEarQM/">bEarQM</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

在上面的代码中，使用了**cycle**这个属性来达到这一目的。

```
 cycle:{
    x:[-100,100], 
    ｝
```

我们在**cycle**中定义了一个数组赋予给X(即transform中的translateX),在实际代码运行中，stagger()会依次从数组中取值赋予给元素，不断的循环。这在执行多个对象的动画的时候非常方便。

下一章节将来介绍GreenSock中很强大的链式动画。




