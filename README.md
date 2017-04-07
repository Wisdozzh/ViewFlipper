#ViewFlipper

手机京东app首页的京东快报有一个无限轮播的公告栏，先看效果：
![][viewflipper]
公告内容大概每3s从中间向上滑出，同时下一条内容从底部向上滑动进入。整个过程还伴随有内容的渐变消失。
开始想这样的效果可以通过自绘控件来实现，后面再想想采用ViewFlipper来实现更为简单。
看看ViewFlipper类官方注释：

```
Simple {@link ViewAnimator} that will animate between two or more views that have been added to it. Only one child is shown at a time. If requested, can automatically flip between each child at a regular interval.
```
大概意思就是ViewFlipper是一个容器，能够将添加在里面的两个或更多子View动画的切换，在一个时间点只有一个child展示出来。并且可以自动的在每隔一个时间段切换到一个child。
要实现京东快报的切换效果，我们只需要将需要根据轮播的公告内容设置到TextView并添加到ViewFlipper，同时设置他们之间的切换动画就可以了。

为了方便在项目中直接使用，我们将其自定义为一个继承自ViewFlipper的控件NoticeView。

--------------------------------
[csdn]:http://blog.csdn.net/zzh_receive/ "我的博客"
[viewflipper]:https://github.com/Wisdozzh/ViewFlipper/raw/master/img/viewflipper.gif

