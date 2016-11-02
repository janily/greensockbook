# 3D效果

在平时的动效开发中，为了是动效具有立体的效果，一般会用到CSS3中的3D transform这一属性。在GreenSock中也提供了3D transform功能，支持CSS3D的全部属性，使用起来比CSS3更加方便。

下面来看看它的使用方法。

开始之前首先要理解greensock中的perspective和transformPerspective两个属性。它们是greensock中运行的基础，使用它们才能使元素具有一个3D空间透视的表现能力。

下面是分别使用transformPerspective和没用transformPerspective的实例：

<p data-height="300" data-theme-id="17491" data-slug-hash="NxyvPb" data-default-tab="result" data-user="janily" data-embed-version="2" data-pen-title="NxyvPb" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/NxyvPb/">NxyvPb</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

可以明显看到，第三个元素由于没有使用perspective属性，只是一个平面的旋转效果。

transformPerspective是针对单个元素使用的，而perspective则是使用在父级元素上，使用它会使改父级元素下的子元素具有3D空间透视的一个展现形式，实例如下所示：

<p data-height="300" data-theme-id="17491" data-slug-hash="EPQvPd" data-default-tab="result" data-user="janily" data-embed-version="2" data-pen-title="EPQvPd" class="codepen">See the Pen <a href="http://codepen.io/janily/pen/EPQvPd/">EPQvPd</a> by janily (<a href="http://codepen.io/janily">@janily</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

可以看到，只需要在父级使用perspective的方法，可以同时使它的子元素都具有3D的展现。

### transformOrigin

transformOrigin是用来设置元素在做transform位移变换时的原点的。默认值是元素的中心点即("50%,50%")。transformOrigin有三个值(x,y,z)，z值是一个可选项。

可以使用"top", "left", "right",或者是"bottom"值亦或是百分值(比如bottom right可以设置为 "100% 100%)。

