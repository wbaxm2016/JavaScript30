# canvas & 鼠标按下绘制粗细颜色渐变的线条

<canvas> width | height属性与css 指定width height不同

- css width height 使画布缩放
- html attribute width height 画布宽高，推荐使用.

## 基础

- 画笔的属性都是全局的，故需使用beginPath()来开始每一次路径绘制，使画笔属性只影响该次路径绘制。
- 绘制路径都是不可见的，需要fill或stroke才能看到效果。
- 填充需要路径是闭合的，非0填充规则。

## MouseEvent坐标

- (clientX, clientY)基于**视区**，无视滚动。
  - (x, y)为该属性的别名
- (screenX, screenY)基于**屏幕**，无视滚动。
- (pageX, pageY)基于**文档**，滚动变化。
- (offsetX, offsetY)基于**事件触发对象 content-box**，滚动变化。
  - (layerX, layerY)基于定位元素，**非标准**，不使用。
- (movementX, movementY)仅mousemove事件，当前与上一个事件坐标差值。

总结：除了(movementX, movementY)都是基于**不同起点**的绝对坐标。考虑是否需要**滚动坐标变化**特性选用。(movementX,movementY)仅对mousemove可用，反映了两次移动之间的相对位置。

## 实现

1. 鼠标按下获取基于视区的坐标信息，设置



 