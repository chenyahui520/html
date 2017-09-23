### 什么 是video

作用：播放视频

格式

```
<video src="">
</video>
```

**video 标签的属性**

* src：用于高速video标签需要播放的视频地址

* autoplay：用于高速video标签是否需要自动播放视频

* controls:用高速浏览器是否显示控制条

* poster：用于告诉video标签没有播放之前显示的展位图片

* loop:一般用于广告视频，用于告诉video标签视频播放完毕是否需要循环

* preload:预加载视频，但是需要注意preload和autoplay相冲突，如果设置了autoplay属性，那么preload属性会失效

* muted:静音

* width:

* height:

#### video的第二种格式

```
<video>
<source src="视频路劲" type="video/mp4"></source>
</video>
```

由于视频数据非常非常的重要，所以五大浏览器厂商都不愿意支持别人的视频格式，所以导致了没有一种视频格式是所有浏览器都支持的，这个时候w3c为了解决这个问题，所以推出了第二个video标签的格式

