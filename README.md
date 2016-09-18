# learning-log
My Learning Log

-------------------------------------  

###September 17,2016  
1. 学到了调用函数传递事件：  

        >fn1('click');  
        fn1('moseover');  
        function fn1(oEvent){  
        div1.on(oEvent,function(){  
        ...........  
        })  
        }
2. jquery的淡入淡出方法用在了焦点图切换：  
	
	>dow.fadeOut().css('zIndex',1)  

###September 16,2016  
接下去的空余时间看看：
1. 了解天猫形式首页上如何写入html，css。  
2. 个人简历写出网页形式，github.io也可以做出简历。  
3. 了解seo优化；了解安全性问题；了解http原理；了解基础的ecmascript，DOW，BOW；ajax；了解如何封装类；了解打包和压缩文件  

###September 15,2016  
1. jquery中dow.hide().eq(0).show();是元素都隐藏除了第0个显示。
2. attr()适合用于修改某个属性所有的值，removeClass()适合修改有多个class的元素。
3. 调用函数的时候传参数的时候同样可以传递对象栗子：    
	>fnTab($('.tabNav1'), $('.tabCon1'));  
4.一个函数里同样可以新定义变量。栗子：  
	>function fnTab( oNav, aCon){  
		var oLi=oNav.children();  
	};
5. addClass的时候如果已经存在这个class将不会发生变化.浏览器并没有出现我担心的报错.  

###September 13,2016  
1. jquery提供的hover方法.hover(function,function);
2. 清除timer用clearIterval(timer); 

###September 10,2016  
今天巩固了下jquery的使用，了解了focus()获取光标的事件和blur()失去光标的事件；利用console.log()来在控制面板里输出console的信息。

###September 7,2016  
今天遇到一个有趣的bug：  
在ie678下background:url()no-repter;中间的no-repter前面要是没有空格的话这个背景图就不会被识别了。规范还是挺重要的。

###September 5,2016  
####go on update   
今天又遇到了低等错误.active li a{ color：red；}来重写li a{ color：yellow；}但是就是不行，改来改去突然发现我的.active是加在li上的，被自己蠢哭！

###September 4,2016  
####命名的时候一直都挺注意用关键词的，今天练习的时候有个360°shop的练习我在其中用的了一个class="360shop"图省事没有加上°结果被他就狠狠的坑了一把。360shop这个玩意居然是不让用，结果下面所以的样式都不起作用我调试了半天肠子都绿了，等到换了一个class才知道原来360也不是什么好人啊！！！

### September 3,2016  
#### 今天在练习的时候发现li上用了overflow：hidden居然达到了去浮动的效果。  
那么overflow属性为什么能达到去浮动的效果？  
是因为overflow除了(visible)会重新给他里面的元素建立块级格式化(block formatting context)floats, position absolute, inline-block, table-cell和table-caption都不是块级样式，所以才会用到clear来控制浮动overflow也可以清除浮动是因为当在父级元素设置overflow时候，除了visible，就是只有auto, hidden或者scroll时候，也会建立新的块级格式给他的子元素, 从而起到清楚浮动效果

###September 1,2016  
####前两天组织了家人一次去金山沙滩的一次自驾游，耽误了几天  
ie6下当浮动元素与非浮动元素相邻时，这个3像素的Bug就会出现，它会偏移3像素解决办法    
1.给浮动的父盒子添加vertical-align:middle    
2.只要触发IE的hasLayout，非浮动元素就会拥有布局。所以，利用   
IE6特有的hack规则，为它单独写样式就可修复此问题：
_zoom:1;
margin-left: value;
_margin-left: value-3px;
zoom 是IE触发Layout条件之一，因为它是IE特有的CSS规则，所以
采用zoom。
margin-left: value-3px 是修复IE6 中3px 的bug。
此前采用非浮动元素也浮动的方法修复bug，现在我们可以试试这个
新的方法了！
注：前面的下划线是专门写给IE7以下版本的hack  

###Augeset 27,2016  
今天终于再次用git上传了一次练习项目，还要继续加油。faighting!!!

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
  谷歌浏览器是不支持12px以下小字体的，可能是考虑到用户体验吧。
  网上也有一些文章介绍，说可以使用：
  复制代码代码如下:
  -webkit-text-size-adjust:none;
  但是，自chrome 27之后，就取消了对这个属性的支持。
  我们还有其它办法解决这个问题吗?
  谷歌浏览器支持CSS缩放，于是，我们可以在这方面做文章：
  复制代码代码如下:
  -webkit-transform: scale(0.5);
  既然最小支持到12px，那么就以12px为基点进行缩放，
  同时可以使用-webkit-transform-origin-x: 0; 来解决缩放后margin-left的位移问题：
  复制代码代码如下:
  .test_tag{
  font-size:12px;
  -webkit-transform-origin-x: 0;
  -webkit-transform: scale(0.5833333333333334);
  }
  scale值的计算方法为： 7 / 12 = 0.5833333333333334      
2. 在父盒子有高度的时候不用清浮动！  

###Augest 23,2016
1. input type=“type”的提示语可以用css中的vule实现不过用户输入的时候需要把提示语删除；  
2. 我们如果用html5中的placehoder属性实现<input placehoder=""> 用html5中的placehoder属性就能实现获取焦点时候自动去掉提示。  
