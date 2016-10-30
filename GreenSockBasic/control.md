# 动画控制

GreenSock提供了play()，pause()，resume()，reverse()，seek()，restart()， progress()，timeScale()等方法来控制动画。下面来看看这些方法都具体起到了什么作用。

play()方法是开始播放动画；

pause()是暂停动画；

resume()是重新开始播放动画，是从暂停处开始播放；

reverse()是从相反的方向来执行动画；

seek()是跳转到整个动画时间的某一个时间点的时地状态，比如整个动画时间是3秒，如果调用**seek(1)**就表示跳转到动画在1秒这个时间点的状态；

progress()是指执行整个动画到某一个时间段，只接收0到1之间的数字。比如给到参数0，表示在动画开始的时候；给到参数0.5表示动画直接跳转到整个动画执行来50%的状态；1就表示动画执行完的状态；

restart()表示重新开始播放动画。

说了这么多，还是直接看实例来理解更快些，点击对应的按钮：

<p data-height="300" data-theme-id="17491" data-slug-hash="edwvGR" data-default-tab="result" data-user="janily" data-embed-version="2" data-pen-title="edwvGR" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/edwvGR/">edwvGR</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

GreenSock基本的知识就介绍到这了，利用这些方法基本上可以对付开发中一些常见的动画开发，剩下的就要看你的想象力了。

当然GreenSock提供能力远不止于此，这一部分会在后面的GreenSock进阶部分讲到，敬请期待。






