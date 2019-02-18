# viewport
移动端适配
利用meta标签对viewport进行控制
```
<meta id="viewport" name="viewport" content="width=device-width; initial-scale=1.0; maximum-scale=1; user-scalable=no;">
```
使用viewport来实现等比适配  倘若设计图是640*1136，为了在设计图上量到多少样式中就能写多少，我们有如下代码
```
var clientWidth = document.documentElement.clientWidth,
    viewport = document.querySelector('meta[name="viewport"]');
    viewportScale = clientWidth / 640;
    viewportWidth = 640;
    viewport.setAttribute('content', 'width=' + viewportWidth + ', initial-scale=' + viewportScale + ', maximum-scale=' + viewportScale + ', user-scalable=0');
    }
```
