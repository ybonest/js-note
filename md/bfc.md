
### BFC理解
   BFC（Block Formatting Context）块级格式上下文。
   
   BFC其实就是一种布局方式，在这种布局方式下，盒子所在的containing block顶部一个接一个垂直排列，水平方向上撑满整个宽度
- 布局规则
 - 内部的Box会在垂直方向一个接一个地放置
 - Box垂直方向距离由margin决定，属于同一个BFC的两个相邻Box的margin会发生重叠
 - 每个元素的margin box的左边，与包含块border box的左边相接触
 - BFC的区域不会与float box重叠
 - BFC就是页面上的一个隔离的独立容器，容器里面的元素不会影响到外面的元素
 - 计算BFC的高度时，浮动元素也参与计算

- 能够生成BFC的元素
 - 根元素
 - float属性不为none
 - position为absolute或fixed
 - display为inline-block、table-cell，table-caption、flex、inline-flex
 - overflow不为visible