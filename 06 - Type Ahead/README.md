# 城市查询

## 布局抖动

windows下滚动条会占据视口尺寸。当滚动条出现和消失时，视区尺寸变化，依赖与视区尺寸的布局会产生抖动。通过设置html或body width:100vw避免布局抖动。因为vw为视区宽度，无论滚动条是否出现视区尺寸都不会发生变化。

## 实现

- Web API fetch(url)获取数据
- findMatches(word, list)过滤数据
  - word生成正则表达式
  - filter过滤生成新数组并返回
- displayMatches()展示数据
  - map对每一项生产新的html标签
  - join、innerHTML渲染