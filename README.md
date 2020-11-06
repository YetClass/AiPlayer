仿TikTok

![抖音，记录别人的美好生活](https://upload-images.jianshu.io/upload_images/8669504-3293ef3c6d1d27d3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/800)

抖音，可以说目前最火的短视频APP！作为一名 Android 开发，是时候研究一下功能是如何实现的了！目前，也有一些其他的小伙伴实现都有播放的效果，只要是用 ViewPager 来实现的上下滑动。 今天，我们换个思路用我们最常用的控件，RecyclerView 来实现，下面先看看需要实现的功能。

大概实现的效果如下
![](https://user-gold-cdn.xitu.io/2019/10/22/16df14a6cf3296fc?imageslim)

大致有以下几个功能。
1. 上下滑动播放详情页
2. 播放之后自动播放
3. 双击点赞效果，并且点赞
4. 单击暂停，再单击播放

仿抖音App做的技术点及特点：
- 全屏切换播放效果用的是Recycler加PagerSnapHelper控制。
![](https://upload-images.jianshu.io/upload_images/8669504-e0830fc715f87cb2.gif?imageMogr2/auto-orient/strip)


- 使用lottie库加载json动画，json动画由VUE制作
![](https://upload-images.jianshu.io/upload_images/8669504-dd45e579a049a9c3.gif?imageMogr2/auto-orient/strip)


- 点赞心形动画
![](https://upload-images.jianshu.io/upload_images/8669504-fccfa86f71641144.gif?imageMogr2/auto-orient/strip)


- 分享评论弹框用的是BottomSheetDialogFragment
![](https://upload-images.jianshu.io/upload_images/8669504-edd6777f1ba8733a.gif?imageMogr2/auto-orient/strip)


- 个人主页用的是CoordinatorLayout+AppBarLayout折叠布局。
![](https://upload-images.jianshu.io/upload_images/8669504-ca63d12612869f5d.gif?imageMogr2/auto-orient/strip)


- 头像大图页面
![](https://upload-images.jianshu.io/upload_images/8669504-94434ff349aec811.gif?imageMogr2/auto-orient/strip)


- 同城视频
![](https://upload-images.jianshu.io/upload_images/8669504-fb5e3e9ad10cd1c5.gif?imageMogr2/auto-orient/strip)

- 话题# @用户控件，可标颜色可点击
![](https://upload-images.jianshu.io/upload_images/8669504-475553d2484c356a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/400)


由于没有接口获取数据，使用的方式是将图片视频资源下载放入项目中，自己构造的视频列表数据。