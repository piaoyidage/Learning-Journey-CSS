# align-items 在 IE 浏览器上的 width 超出父元素

**DOM 结构见 index.html**

当 .wrap 设置 align-items，同时 .options 没有设置 width，此时 .options 的宽度会超出 .wrap

![](https://ws1.sinaimg.cn/large/006tNc79ly1g26veexe3jj310404mq31.jpg)

如果要正确显示，需要给 .options 设置 width 或者 max-width

![](https://ws2.sinaimg.cn/large/006tNc79ly1g26vf1x008j30je0aiweq.jpg)
