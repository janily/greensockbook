# 选择元素

### 代码约定

为了方便演示代码，统一使用**codepen**这个在线的代码编辑平台来进行demo演示。

本教程主要以TweenMax这个全功能的js文件为基础，它包括了GreenSock动画平台的所有核心的功能。还需要引入jquery来选择和操作DOM。

### 开始

先准备基本的html和css骨架，如下所示：

<p data-height="300" data-theme-id="17491" data-slug-hash="xwbpGw" data-default-tab="result" data-user="janily" data-embed-version="2" data-pen-title="xwbpGw" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/xwbpGw/">xwbpGw</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

OK，准备工作已做好，下面来让它动起来！

这里操作的对象是这个ID为box的盒子。首先把它用一个变量存起来，方便后面来操作。在codepen里的js区域编写下面的代码：

```
var $box = $('#box');
```

上面可以看到我们使用了**jquery**来选择需要操作的DOM。当然你也可以使用javascript原生提供的DOM操作方法来选择DOM节点。

接下来就可以是使用GreenSock中提供的各种API方来使它动起来，请看下一章节。




