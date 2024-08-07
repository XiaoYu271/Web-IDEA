## 009-Float

`标准文档流`
--
`1、标准文档流: Web页面的制作是个 "流" 必须从上到下而设计软件想往哪画都可以`

`2、标准文档流的特性`

- `1. 空白折叠现象：无论多少个空格、换行、tab，都会折叠为一个空格`

  `2. 高矮不齐，底边对齐`

  `3. 自动换行，一行写不满，换行写`

`3、脱离标准文档流`

- `1. 浮动`

  `2. 绝对定位`

  `3. 固定定位`

`行内元素 块级元素`
--
`1、行内元素和块级元素区别`

- `1. 行内元素：与其他行内元素并排 不能设置宽、高 默认的宽度，就是文字的宽度`

  `2. 块级元素：霸占一行 不能与其他任何元素并列 能接受宽、高 如果不设置宽度，那么宽度将默认变为父亲的100%`

`2、行内元素和块级元素的分类`

- `1. 行内元素：span、a、b、i、u、em`

  `2. 块级元素：p、div、h系列、li、dt、dd`

`3、display="规定元素应该生成的框的类型"`

- `1. none="不占位隐藏 此元素不会被显示"`

  `2. block="此元素将显示为块级元素 此元素前后会带有换行符"`

  `3. inline="此元素会被显示为内联元素 元素前后没有换行符 默认"`

  `4. inline-block="行内块元素"`

`浮动`
--
`1、浮动的性质`

- `1. 浮动的元素脱标`

  `2. 浮动的元素互相贴靠`

  `3. 浮动的元素有"字围"效果`

  `4. 收缩：一个浮动的元素 如果没有设置 width 那么将自动收缩为内容的宽度这点非常像行内元素`

`2、float="规定框是否应该浮动"`

- `1. left="元素向左浮动"`

  `2. right="元素向右浮动"`

  `3. none="默认值 元素不浮动 并会显示在其在文本中出现的位置"`

`9、浮动的清除`
- `1. 给浮动元素的祖先元素加高度` `有高度的盒子，才能关住浮动`

  `两个 div 均没有高度导致不能给自己浮动的孩子撑起一个容器 如果 div 自己的高度小于孩子的高度也会出现不正常的现象`

  `2. clear:both 不允许左侧和右侧有浮动对象`

  `致命问题: 标签 margin 属性失效 本质原因是：两个 div 高度为零`

  `3. 隔墙法`

  `防止第二个 div 贴靠到第一个 div 可以在这两个 div 中间用一个新的 div 隔开 这个新的 div 设置 clear: both 属性 这个新的 div 无法设置 margin 属性 我们可以给它设置 height 以达到 margin 的效果`

  `4. 内墙法`

  `父亲是不能被浮动的儿子撑出高度 内墙法可以给它所在的家撑出高度`

  `5. overflow:hidden`

  `本意是清除溢出到盒子外面的文字 这一招，实际上生成了 BFC 生成了封闭空间`

  `6. 伪元素清除浮动`