1、尚硅谷，关于动画部分的学习
什么是动画? 
动画有下面两种情况
同一个图形通过视图在界面上进行透明度,缩放,旋转,平移的变化(View动画)
在界面的同一个位置上不断切换显示不同的图片(Drawable动画)
2.1 使用View Animation
动画的分类
View Animation
Drawable Animation

Android中提供了两种实现动画的方式
纯编码的方式
Xml配置的方式

动画在应用中是非常常见的界面效果, 也是提高用户体验的一种好手段


View动画的分类
单一动画(Animation)
缩放动画(ScaleAnimation)
透明度动画(AlphaAnimation)
旋转动画(RotateAnimation)
平移动画(TranslateAnimation)

复合动画(AnimationSet)
由多个单一动画组合在一起的动画


Animation的公用功能
setDuration(long durationMillis) : 设置持续时间(单位ms)
setStartOffset(long startOffset) : 设置开始的延迟的时间(单位ms)
setFillBefore(boolean fillBefore) : 设置最终是否固定在起始状态
setFillAfter(boolean fillAfter) : 设置最终是否固定在最后的状态
setAnimationListener(AnimationListener listener) : 设置动画监听

坐标类型:
Animation.ABSOLUTE    绝对位置
Animation.RELATIVE_TO_SELF     相对于自己
Animation.RELATIVE_TO_PARENT   相对于父位置

启动动画 : view.startAnimation(animation);
结束动画: view.clearAnimation()

动画监听器 : AnimationListener
onAnimationStart(Animation animation) : 动画开始的回调
onAnimationEnd(Animation animation) : 动画结束的回调
onAnimationRepeat(Animation animation) : 动画重复执行


缩放动画(Code ScaleAnimation)
fromX : 开始时X轴上的缩放比例   
toX : 结束时X轴上的缩放比例   
fromY :开始时Y轴上的缩放比例
toY :结束时Y轴上的缩放比例
pivotXType : X轴坐标的类型(计算x轴上的偏移量的方式)
pivotXVlaue : 中心点在X轴相对视图左顶点在x轴上的偏移量
pivotYType :  Y轴坐标的类型(计算x轴上的偏移量的方式)
pivotYValue : 中心点相对视图左顶点在y轴上的偏移量
缩放动画(Xml ScaleAnimation)
<scale xmlns:android="http://schemas.android.com/apk/res/android"
    android:duration="2000"
    android:fromXScale="0.0"
    android:fromYScale="0.0"
    android:pivotX=“1"
    android:pivotY=“0.5“           
    android:toXScale="1.0"
    android:toYScale="1.0"
    android:fillAfter="true"/>
    
   Animation.ABSOLUTE : 
	数值(默认以px为单位)   100
Animation.RELATIVE_TO_SELF : 
	百分数,如:50% (以当前视图的宽度或高度其为基数来计算)   
Animation.RELATIVE_TO_PARENT : 
	百分数+p,如:50%p (以父视图的宽度或高度其为基数来计算)
    
    
