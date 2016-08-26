# learning-log
MyLearninglog

###Augeset 26,2016
**学习方法这个必须几下！！！**   
1. 不要再想将来要学什么，沉浸现在！    
2. 通过把技术当做玩具来使得练习更加有趣！    
3. 写代码前告诉自己只写几分钟代码，这样就不知不觉会有很多时间来写（浏览facebook技巧）！    
4. 慢慢来，小步向前，将会学的更快    

###Augest 25,2016  
1. span标签宽度无效，原来是所有默认display为inline的元素都会宽度无效话。  
解决办法？  
据说不太完美解决办法 修改span为block类型并设置float
设置display:inline—block   
2. word-spacing不起作用！  
解决办法？  

>word-spacing这个属性对中文没用，不过在中文之间加个空格就生效了。可能老外觉得两词之间没空格就是一个词：helloworld，你好。试验了下letter-spacing，生效，说明浏览器把没空格的中文当成字母了。word-spacing用于修改字间距离。这里的“字”，简单的说，可以是任何非空白字符组成的串，并由某种空白符包围。所以象形文字是无法指定字间隔的。除非字之间有空格


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

###Augest 23,2016
1. input type=“type”的提示语可以用css中的vule实现不过用户输入的时候需要把提示语删除；  
2. 我们如果用html5中的placehoder属性实现<input placehoder=""> 用html5中的placehoder属性就能实现获取焦点时候自动去掉提示。  
