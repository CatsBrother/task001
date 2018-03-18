# task001
百度前端技术学院任务001

花了好几天才写完这几个页面，是2015年百度前端技术学院任务0001，费了好大工夫上传到了github，刚刚入门，请各位大牛斧正。

下面总结一下这几个页面学到的东西


1.关于背景透明
颜色透明：rgba（255,255,255,0.5）；
前三个参数分别为颜色的rgb值，最后一个为透明度，在0到1之间；
图片透明 opacity：透明度；


2.关于背景的渐变
采用了W3C标准的方法
background：linear-gradient（to bottom，rgba（255,255,255,0.7） 0%，rgba（255,255,255,0.5） 75%，rgba（255,255,255,0）100%）

适用于不同浏览器的方法还有： 详情：http://www.runoob.com/css3/css3-gradients.html
  background: -webkit-linear-gradient(red, blue); /* Safari 5.1 - 6.0 */
  background: -o-linear-gradient(red, blue); /* Opera 11.1 - 12.0 */
  background: -moz-linear-gradient(red, blue); /* Firefox 3.6 - 15 */
  background: linear-gradient(red, blue); /* 标准的语法 */
  
  
3.设置几个并列模块的高度一致，且自适应于文字
  1.给所有模块设置一个父元素包裹，并让父元素 overflow：hidden；
  2.给子元素设置一个较大的padding-bottom；
  3.设置margin-bottom为padding-bottom的相反数，抵消内边距；
  
  
4.解决高度塌陷问题：
  1.overflow：hidden；
  2.zoom=1；


5导航栏水平居中
  1.设置li为行内块元素--display：inline-block；
  2.设置ul居中  text-align；
  
  
6单行文本溢出显示省略号
  1.white-space：nowrap  禁止换行
  2.overflow：hidden  溢出隐藏
  3.text-overflow：ellipsis  省略号
  
  
7瀑布流实现
  1.一列中的模块宽度一样，确定宽度，每一列为一组，组左浮动
  2.每一列内的数据块依次排列
  
  
8CSS的外边距合并问题
    当两个垂直外边距相遇时，他们将合成一个外边距，合并之后的外边距高度等于两个发生合并的外边距中较大的那个。
  解决：主要思想使两个外边距不相遇
     1.为父元素设置padding-top=1px；
     2.父元素overflow：hidden；
     3.父元素或子元素浮动；
     4.为父元素或子元素添加border；
     5.为父元素或子元素开启绝对定位；
