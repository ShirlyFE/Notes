ie6/7 input margin双倍解决方法
==============================

####问题描述

input标签(不包含type="checkbox"类型标签)的父元素有加水平方向的margin,则水平方向的margin会成双倍显示。

####问题代码

        <div style="width:300px; height:35px; border:1px red solid;margin-left:15px;"><input type="text"/></div>

####解决方法

#####1.  给input标签的直属父标签加*display:inline;属性  (推荐)

        <div style="width:300px; height:35px; border:1px red solid;margin-left:15px;float:left;*display:inline;"><input type="text"/></div>

        (上面代码加float:left;只为保证div成块状显示，非必须！)
 
#####2.  把父元素的水平margin改成padding，直接避开ie6、7这个margin双倍bug (推荐)

        <div style="width:300px; height:35px; border:1px red solid;padding-left:15px;"><input type="text"/></div>