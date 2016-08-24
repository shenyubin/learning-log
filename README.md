# learning-log
MyLearninglog

###Augest 23,2016
1. input type=“type”的提示语可以用css中的vule实现不过用户输入的时候需要把提示语删除；我们如果用html5中的placehoder属性实现<input placehoder=""> 用html5中的placehoder属性就能实现获取焦点时候自动去掉提示。  

###Augest 24,2016
1. chrome默认字体最小为12，再小还是显示12  
《解决办法？》  
  
>谷歌浏览器是不支持12px以下小字体的，可能是考虑到用户体验吧。
>网上也有一些文章介绍，说可以使用：
>复制代码代码如下:
>-webkit-text-size-adjust:none;
>但是，自chrome 27之后，就取消了对这个属性的支持。
>我们还有其它办法解决这个问题吗?
>谷歌浏览器支持CSS缩放，于是，我们可以在这方面做文章：
>复制代码代码如下:
>-webkit-transform: scale(0.5);
>既然最小支持到12px，那么就以12px为基点进行缩放，
>同时可以使用-webkit-transform-origin-x: 0; 来解决缩放后margin-left的位移问题：
>复制代码代码如下:
>.test_tag{
>font-size:12px;
>-webkit-transform-origin-x: 0;
>-webkit-transform: scale(0.5833333333333334);
>}
>scale值的计算方法为： 7 / 12 = 0.5833333333333334
2. 在父盒子有高度的时候不用清浮动！
