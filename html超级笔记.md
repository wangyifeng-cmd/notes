# Html,css笔记

### 快捷键

```js
alt + shift + 上下键 //复制这一行到上下位置
```

### mate的用法

```html
<mate name="keyword" content="网页的关键字 用英文逗号隔开">
<mate name="description" content="对网站的描述 一般为一段话">
```

###  i和em（加粗）

###  strong和em （斜体）

###  有语法含/义

```html
王译锋<b>好帅</b>
王译锋<strong>好帅</strong>
王译锋<i>好帅</i>i标签因为很少用到，可以用来装小图标）
王译锋<em>好帅</em>
```

### rem布局

> em 相对于自己
> rem 相对于根元素html的字体

### img 中的 "alt" 和 "title"

```html
<img src="" alt="当图片显示不出来的时候显示的文字" title="当鼠标悬停在图片上面的文字">
```

### href 和 src 的区别

-  href：用于<a>,<link>,页面会并行加载后续内容

```css
a{
 text-decoration:none;
 color:black;
}
```

```html
<a href="http://www.baidu.com"></a>
```

```html
<link type="text/css" rel="stylesheet" href="common.css">
```

- src：用于<img>,<frame>,<iframe>,<script>,浏览器需要加载完毕src的内容才能继续往下走

```html
<img src="img/girl.jpg">
```

```html
<iframe src="top1.html">
<frame src="top.html">
<script src="show1.js">
```

### a标签的target

- "_self" 表示当前网页打开(默认)_
- "_blank" 表示新打开一个页面

```html
<a target="_blank" href="http://www.baidu.com">点击这里</a>
```

### del标签---表示删除线

```html
<del>小风同学</del>
```

###  href中的上一级和下一级

-  "./"表示当前文件夹
- "../"表示上一个文件夹

```html
<a href="./img/王译锋.ipg">王译锋<a>
<a href="../img/王译锋.ipg">王译锋<a>
```

### 空格，大于符号，小于符号，版权符号

- 空格：&nbsp
- 大于符号：&gt
- 小于符号：&lt
- 版权符号：&copy

### 有序列表 和 无序列表

- 有序列表：

```html
<ol>
 <li>第一个</li>
 <li>第二个</li>
<ol>
```

- 无序列表：

```html
<ul>
 <li>第一个</li>
 <li>第二个</li>
<ul>
```

### 自定义列表

```html
<dl>
 <dt>头</dt>
 <dd>内容</dd>
</dl>
```

### 颜色

rgba = rgb + 透明度
rgba红，绿，蓝，透明度)
rgbared,green,blue,alpha)
取值范围(0-255,0-255,0-255,0-1)

```css
color:rgb(34,54,56,0.5);
```

### 十六进制-颜色

红绿蓝范围00-ff

```css
color:#ff0000;
```

hsla = hsl + 透明度
hsla颜色
hsla(色环，饱和度，亮度，透明度)
hsla(0-360,0-100%,0-100%,0.5)

```css
color:hsl(0,50%,50%)
```

### em/rem 倍数

- em是相对于自己的倍数
- rem是相对于html根节点的倍数

```css
font-size:2em;
font-size:2rem;
```

### 样式优先级的关系，先后顺序

标签选择器 1
class选择器 10
id选择器 100
行内选择器 1000
！improtant 无限大

```css
p{
 color:blue !important;
}
```

### 后代选择器

- 作用：选择满足条件的所有后代

```css
.box>p{
}
```

### 子代选择器

- 作用：选择满足条件的子代元素

```css
.box p{
}
```

### 怪异盒模型

- 特点：盒子大小不会发生改变，添加border盒padding的时候会缩小内容区域保证盒子的大小不变，为了加padding时让盒子不撑大

```css
box-sizing:border-box;
```

### overflow

超出div部分用 hidden 隐藏

```css
.div{
 overflow:hidden;
}
```

### overflow---滚动条

- auto:当内容超出div长度用auto自动生成滚动条
- scroll:无论内容有没有超出div长度强行加滚动条

```css
.div{
 overflow:auto;
}
.div{
 overflow:scroll;
}
```

### 开启bfc容器 bfc:格式化上下文 相当于漂浮在海上的新的容器

- position
- float
- overflow

### div中文字对其-两端对齐

- 用于当文字换行右边有多出半个空格的时候对其左右两边空格

```css
text-align:justify;
```

### 段落缩进（文章前面两个空格，空两格）

```css
text-indent:2em;
```

### 字与字之间的间隙，字体间隙

```css
letter-spacing:1em
```

### 字体倾斜

```css
font-style:italic;
```

### 引用字体-下载 ttf 字体，文字样式

```css
@font-face{
 font-family:"憨憨";
 src:url("./字体/楷书.ttf");
}
p{
 font-family:"憨憨" , sans-serif;
}
```

```css
img{
 vertical-align:baseline;(默认)
 vertical-align:middle;(中线对齐)
 vertical-align:top;(行宽顶部)
}
```

### 文本装饰线

```css
下划线：text-decoration:underline;
上划线：text-decoration:overline;
删除线：text-decoration:line-through;
```

### style中全部都调整(通配符)

```css
*{
 margin:0;
 padding:0;
 list-style:none;
}
```

### 多余文字省略号代替

```css
white-space:nowrap;(文字超出不慌行)
overflow:hidden;(超出隐藏)
text-overflow:ellipsis;(文字超出部分显示状态)
```

### 不可复制文字

```css
user-selet:none;
```

### 定义为块元素

```css
display:none;(隐藏)
display:block;
display:inline;(行内元素，宽高失效)
display:inline-block(支持宽高的块元素)
```

### 代码中换行符导致行内块元素中间有空格，去除空格，可以加一下代码，空格解析（中间有间隙）

```css
父类{
 font-zise:0;
}
```

### 通过link引用css

```html
<link rel="stylesheet" href="./reset.css">
```

### 背景不重复

```css
background-repeat:no-repeat;
```

### 控制背景图片的x和y轴位置

```css
background-position:right top;
background-position:center;
```

### 改变背景图片的xy轴的原点

```css
background-origin:padding-box;(默认以内容左上角为原点)
background-origin:border-box;(以边框左上角为原点)
```

### 背景填充的两种方式

```css
background-size:cover;(等比例放大到填充整个容器，可能有一部分图片被遮住)
background-size:contain;(等比例放大到其中一条边碰到边界就停止，整张图片都在)
```

### 当背景填充用cover造成部分图片不在区域内可用backgound-clip裁剪掉，值和background-origin一样

```css
background-clip:content-box;
```

### 背景复合写法"background:color url repeat position位置/size大小;"，可写多个背 景，多个背景的前后关系和代码上下关联，复合背景。

```css
background:url("./img/wangyifeng.jpg") no-repeat left top/40px 40px,
url("./img/wangyifeng.jpg") no-repeat left top/cover;
url("./img/wangyifeng.jpg") no-repeat center/cover;
```

### 背景的附着定位，和overflow;auto(滚动条)一起用

```css
background-attachment:scroll;(默认值，固定在body上)
background-attachment:fixed;(随滚动条滚动)
background-attachment:local;(会固定在文字上)
```

### 主页背景的设置

```css
body,html{
 width:100%;
 height:100%;
 background:url("./img/feng.jpg") no-repeat center/cover;
 background-attachment:fixed;(背景附着定位)
}
```

### border和outline(轮廓)的区别，书写是一样的，但是outline不会占据其他元素的位置

```css
outline:10px solid black;
```

### 盒子阴影

````css
box-shadow:x y 模糊半径 原来的基础上增加的大小 颜色 扩散位置（outset向外扩散，inset巷内扩散）;
box-shadow:10px 10px 10px 10px black inset;
````

### 盒子渐变色,默认垂直变色,不属于背景颜色，属于图片，线性渐变

```css
background:linear-gradient(to right,blue 33%,white 33%,white 66%,red 66%);
background:linear-gradient(45deg,blue 33%,white 33%,white 66%,red 66%);（deg可以控制颜色的角度）
background:linear-gradient(1.3turn,blue 33%,white 33%,white 66%,red 66%);（turn也可以控制颜色角度）
```
```css
background: linear-gradient(90deg, #0081ff, #1cbbb4);
background: linear-gradient(90deg, #9EF5D2, #6DB7F4);
background: linear-gradient(90deg, #CA4CA8, #2C84F9);
```

### 背景径向渐变色

```css
background:radial-gradient(圆心水平半径 圆心垂直半径 at 圆心水平位置 圆心垂直位置 red 30,blue 80%,yellow);
background:radial-gradient(100px 100px at 100px 100px,red 30,blue 80%,yellow 99%,transparent) no-repeat 0 0 / 100px 100px;
```
### 背景重复线性渐变色

```css
background:repeating-linear-gradient(red 0px,red 40px,blue 40px,blue 100px);
```
### 背景重复径向渐变色

```css
background:repeating-radial-gradient(red 0px,red 40px,blue 40px,blue 100px);
```

### 背景滤镜

```css
filter: blur(10px);（模糊）
```
### 任何元素设置浮动后会强制转换为行内块元素，就可以设置宽高了

```css
span{
float:left;
}
```


### 消除两边浮动

```css
clear:both;
```
### 伪元素创建幽灵元素设置clear，使用浮动的时候在父级元素中添加为元素，清除浮动，目的是为了防止父级高度塌陷

```css
.clearfix::before{
 content:"";
 display:block;
 clear:both;
}
```
### font-weight的范围

normal：默认值。
bold：粗体字
bolder：更粗的字
lighter：更细的字
100
200
300
400（bold）
500
600
700（bold）
800
900
inherit：从父元素继承字体的粗细

### 层级，z-index的值越高，就在越上面

```css
z-index:1000;
```
![](C:\Users\nnf\Desktop\超叼的\img\10-2.png)

### 绝对定位，和float浮动的漂浮特性很像，谁在最后面谁的层级越高，参照物是离他最近的一个父级定位元素

```css
position:absolute;
```
### 相对定位，相对于自己的位移

```css
position:relative;
```
### 固定定位，是绝对定位absolute的一种，跟绝对定位的特性一摸一样，但是参照物永远是html

```css
position:fixed;
```
- fixed布局后div居中

```css
div{
position:fixed;
margin:auto;
left:0;
right:0;
top:0;
bottom:0;
width:200px;
height:150px;
}
```

### 黏滞定位，在默认情况下不脱离文档流，达到限制的区间以后会脱离文档流，实现固定定位

```css
position:sticky;
```
### a标签不想要下划线

```css
text-decoration:none;
color:black;
```
### a标签的属性

- href:跳转路径 （阻止默认跳转的方式：# 后者 JavaScript:;）
- target:跳转方式 （新页面打开：_blank）

> form表单容器
> 元素类型：块元素
> action："请求地址"
> method："请求方式"，常见值GET 和 POST
> name："表单名字"
> target："表单提交的位置，是当前位置还是新页面

```js
<form target="-blank" action action="https://www.baidu.com" method="POST" name="xixi">
```

> input表单，放在表单容器中
> 元素类型：行内块元素
> type：表单元素的类型
> name：表单的名字
> value：用户输入的内容，即提交到后端的数据
> placeholder：用户提示信息
> autocomplete：默认“on”，可以填“off”，需要对客户的资料进行保密，防止浏览器软件或者恶意插件获取到，可以用off来关闭记录

```css
css:input{/*去除边框线*/
 outline:none;
}
```

```css
<input type="text" name="user" value="" placeholder="请输入账号密码">/*文本输入框：*/
密码输入框：<input type="password" name="pwd" placeholder="请输入密码" value="">
```

### 给input的默认值加颜色（placeholder加颜色）

```css
input::-webkit-input-placeholder {
    /* WebKit browsers */
    color: #CDCBCE;
}

input:-moz-placeholder {
    /* Mozilla Firefox 4 to 18 */
    color: #CDCBCE;
}

input::-moz-placeholder {
    /* Mozilla Firefox 19+ */
    color: #CDCBCE;
}

input:-ms-input-placeholder {
    /* Internet Explorer 10+ */
    color: #CDCBCE;
}
```

### select多选栏，下拉选项，，默认选中用selected，如果是必须填的值，不选提交不了就加required

```html
<select required name="day">
  <option selected value="1">星期一</option>
  <option value="2">星期二</option>
  <option value="1">星期三</option>
</select>
```

### 下拉值可以用optgroup分类

```html
<select required name="day">
 <optgroup label="星期几">
  <option selected value="1">星期一</option>
  <option value="2">星期二</option>
  <option value="1">星期三</option>
 </optgroup>
 <optgroup label="吃啥">
  <option selected value="1">星期一</option>
  <option value="2">星期二</option>
  <option value="1">星期三</option>
 </optgroup>
</select>
```

### radio单选框，选择小圆圈，必须name值相同，默认选中用checked，男女

```html
性别：
<input checked type="radio" value="nan" name="sex">男
<input type="radio" value="nv" name="sex">女
```

### label 扩大选区范围，只能配合 radio 或者checkbox 使用，for绑定的是单选或者复选框的id值，鼠标按字也可以选择

```html
性别：
<input type="radio" value="nan" name="sex" id="man">
<label for="man">男</label>
<input type="radio" value="nv" name="sex" id="woman">
<label for="woman">女</label>
```

### checked 单选框被选择时的状态

```css
input[type="radio"]:checked{
}
```

### focus 表单元素聚焦时的状态，鼠标焦点在表单上

```css
input : focus{
}
```

### checkbox多选框

```html
兴趣爱好：
<input type="checkbox" name="like" value="music" id="">唱
<input type="checkbox" name="like" value="dance" id="">跳
<input type="checkbox" name="like" value="rap" id="">rap
<input type="checkbox" name="like" value="bas" id="">篮球
```

### textall文本框，cols控制宽，rows控制高

```html
<textarea name="textall" id="" cols="30" rows="10"></textarea>
```

### email,color,data的表单元素

```html
邮箱：<input type="email" name="e" id="">
颜色：<input type="color" name="color" id="">
日期：<input type="date" name="d" id="">
```

### 提交文件按钮

```html
<input type="flie" name="" id="">
```

### 提交按钮，禁止提交加disabled

```html
<input type="submit" value="提交">（标准）
<input type="button" value="提交">
<button></button>
```

### reset清空表单按钮

```html
<input type="reset" value="清空表单">
```

### 表单后端取到的值

```js
{
 user : "你好哈哈哈",
 pwd : 1234,
 day : 3,
 sex : ":nv"
 like : ["music","rap"]
 textall : "aasdjfkigdsgveij"
}
```

### 表格

```css
table{
 border-collapse:collapse;
}
table td{
 width:100px;
}
```

```css
<table>
    <tr>
        <td rowspan="2">1</td>
        <td colspan="2">2</td>
        <td>3</td>
    </tr>
    <tr>
        <td>4</td>
        <td>5</td>
        <td>6</td>
    </tr>
</table>
```

### 高级选择器

```css
后代选择器，选择后代所有：
div span{
}
并列选择器：
div,p{
}
子代选择器，选择下一代的：
div > span{
}
兄弟（相邻）选择器，选择所有p下一个“标签”是span的这个span：
p + span{
}
关联选择器，弟弟选择器，选择第一个p后面所有span：
p ~ span{
}
并且选择器，ul 下 li 元素并且class名为list
ul li.list{
}
属性选择器
^以什么开始
￥以什么结束
*包含什么
input[type^="f"]{
}
<input type="file" name="aa" id="">
多选选择器(even偶数 odd奇数)
div p:nth-child(n+1){
}（既要满足p又要满足n+1）
div p:nth-of-type(n+1){
}（p和n+1都要满足）
div p:first-child{
}（选择第一个）
div p:last-of-type{
}（选择最后又一个）
```

### 伪类选择器，鼠标悬停

- 链接：https://www.w3school.com.cn/css/css_pseudo_classes.asp

- :link 未被访问
- :hover 鼠标悬停
- :visited 访问过的
- :active 点击按下时
- :focus <input>获取焦点时

### 过渡动画

```
最简单
transition: .3;
有部分属性参与动画
transitiong-property: width ;(一部分)
transition-duration: 1s;(时间)
transition-timing-function:ease;(默认，先快后慢)
transition-timing-function:linear;(匀速)
transition-timing-function:cubic-bezier(0,0,1,1);(自己调)
transition-delay:2s;(延迟时间)
复合写法
transition: width 1s linear 1s,height 2s;
```

### 添加动画

```css
.div{
 animation-name:move;
 动画时间
 animation-duration:2s;
 动画加速度
 animation-timing-function:linear;
 动画播放次数 infinite:无限循环
 animation-iteration-count:3;
 动画播放方向 
 animation-direction:alternate;(播放结束后反向播放)
 animation-direction:reverse;(一开始就反向播放)
 动画延迟时间
 animation-delay:1s;
 动画结束后的位置
 animation-fill-mode:forwards;(回到终点)
 animation-fill-mode:backwards;(回到起点)
 动画播放控制停止还是播放，可以和hover一起用
 animation-play-state:runing;(动)
 animation-play-state:paused;(停止)
 动画的复合写法
 animation:move 4s linear infinite;
}
@keyframes move{
 0%{
  left: 0px;
  opacity:0;(可以设置渐渐变浅色)
 }
 100%{
 left:1000px;
 }
}
```

### 鼠标

```css
cursor:url(./img/..),default;
```

### 变形，原位置不会脱离文档流（旋转，变大放大缩小，xy轴移动）

```css
旋转
transform: rotate(1.2turn);
平移
transform: translate(100px,0);
缩放
transform: scale(2);
倾斜
transform: skew(35deg);
设置变化原点
transform-origin: left top;
transform-origin: 100% 0;
复合写法
transform: translatexX(100px) translateY(100px) scale(.5);
立体旋转
transform: rotateX(90deg);（从 右边 看顺时针旋转）
transform: rotateY(90deg);（从 上面 看顺时针旋转）
transform: rotateZ(90deg);（从 正面 看顺时针旋转）
设置景深，添加的位置是参与变化的父元素，想要看到3D效果就一定要加这个属性，为了模拟到z轴的距离
perspective: 800px;（800px~n）
如果又多个3D元素的话要加上
transfrom-style: preserve-3d;
```
### 一直旋转

```css
.turn {
     -webkit-transform: rotate(360deg);
     animation: rotation 25s linear infinite;
     -moz-animation: rotation 3s linear infinite;
     -webkit-animation: rotation 25s linear infinite;
     -o-animation: rotation 3s linear infinite;
}

@-webkit-keyframes rotation {
     from {
          -webkit-transform: rotate(0deg);
     }
     to {
          -webkit-transform: rotate(360deg);
     }
}
```

### 弹性盒模（弹性容器）

父级加display: flex; 子代会相似左浮动效果，但是当一列元素宽度超出父级宽度，子代会被像皮球一样均匀压缩而不会换行，而且子代中行内元素会强制转发为行内块元素
改变排布方向，主轴方向
flex-direction: row;(默认值，横向排布)
flex-direction: row-reverse;(反向横向排布)
flex-direction: column;(垂直排布)
换行
flex-wrap: wrap;
主轴方向和换行的复合写法（不常用）
flex-flow: column wrap;
缩小系数，在不换行的情况下缩小父级宽度，里面元素缩小的速度倍数，2在缩小的时候缩小的速度是1的两倍，值越大缩小越快，为0时就是变的几乎为0，就是不变
flex-shrink: 1;
成长系数，与缩小系数相反，系数越大是增长得更快
flex-grow: 1;
元素的基础大小，不会因为父级改变而发生伸缩!
flex-basis: 200px;
成长系数，缩小系数，基础大小复合写法
flex: 1 1 auto;
<img src="C:\Users\nnf\AppData\Roaming\Typora\typora-user-images\image-20210228160427552.png" alt="image-20210228160427552" style="zoom: 80%;" />
侧轴(横)排列方式，居中
align-tiems: flex-start;(默认值)
align-items: center;
align-items: flex-end
主轴(竖)排列方式
jutify-items: flex-start;
给元素单独设置排列方式，用法和items一样
align-self: flex-start;
给元素排队，值越小越在前面
order: 1;
（侧轴）两端对其，中间留白，一行内才有效果
justify-content: center;
justify-content: space-between;
<img src="C:\Users\nnf\AppData\Roaming\Typora\typora-user-images\image-20210226210406965.png" alt="image-20210226210406965" style="zoom:25%;" />
（侧轴）两边留白，中间也留白，一行内才有效果
justify-content: space-around;
<img src="C:\Users\nnf\AppData\Roaming\Typora\typora-user-images\image-20210226210706505.png" alt="image-20210226210706505" style="zoom:25%;" />
（主轴）两端对其，中间留白，要有换行，多行才有效果
align-content: space-between;
<img src="C:\Users\nnf\AppData\Roaming\Typora\typora-user-images\image-20210226211625450.png" alt="image-20210226211625450" style="zoom:25%;" />

### div---flex布局垂直居中

```css
display: flex;
align-items: center;/*垂直*/
justify-content: space-around;/*水平*/
```

### 媒体查询，当html宽度少于一定的时候发生的变化，就是html宽度变小时响应式，适配电脑，手机，平板之间的转换，(min-width max-width) 在这个宽度范围时变化

```css
@media screen and (max-width: 700px) and (min-width){
}
```

### h5新标签

<header>头部</header>
<main>
 主体
 <article>文章</article>
 <nav>导航(左)</nav>
 <aside>侧边栏(右)</aside>
 <section>不知道用什么</section>
</main>
<footer>底部</footer>

### 视频

```css
<video controls(加上才可以播放) muted(静音，有时候不能自动播放加这个就可以了) autoplay(自动播放，大部分浏览器不支持) loop(循环播放) poster=""(换封面图片) src=""></video>
```

### 音乐

```html
<audio  src=""></audio>
```
### 小网页，网页中的网页，可以放其他的，如视频

```html
<iframe src="" frameborder="0"></iframe>
```

### 可以和a元素配合

```html
<a href="baidu.com" target="wyf"></a>
<iframe src="" name="wyf"></iframe>
```

### 代码书写规范

1.content: ""
2.布局位置相关的属性 position top left
3.盒模型 width height padding
4.文字样式 font-size text-align
5.视觉效果 bgc color



# 备注

### 问题：添加      font-size: 0;  后面的文字消失

> 答：需要重新设置font-size: 16px;

### span底部对齐

```css
vertical-align: middle;/*span中加入*/
```

### 两个大div，需要一个固定宽度，一个自动伸缩

```css
height: calc(100% - 50px);/*50px为固定div的宽度
```

### 文字竖着排

```css
writing-mode: tb-rl;/*字向下排布*/
writing-mode:vertical-lr;/*字头向上,竖着排,下一行为右边*/
writing-mode:sideways-rl;/*字头向右,竖着排,下一行为左边*/
```

### 让盒子加padding时不会增加高度宽度

```css
box-sizing: border-box;
```

### 两个span字体以垂直方向的中心对齐，图片和字对齐

```css
vertical-align: middle;
```

### 字母和字母间隔

```css
letter-spacing: 1px;
```



### 字体颜色混合

> 1.mix-blend-mode混合模式的元素可以和该元素下方的元素实现混合效果
> 2.mix-blend-mode混合模式的元素只能和正下方的第一层元素实现混合效果(此处第一层指的是下方的层叠区域)
> 3.如果想实现下方多层混合，下方的元素也需要使用mix-blend-mode混合模式.
> 4.使用mix-blend-mode混合模式的元素不能和html,body标签的背景图或者背景色产生混合效果

```css
mix-blend-mode: normal;         // 正常
mix-blend-mode: multiply;       // 正片叠底
mix-blend-mode: screen;         // 滤色
mix-blend-mode: overlay;        // 叠加
mix-blend-mode: darken;         // 变暗
mix-blend-mode: lighten;        // 变亮
mix-blend-mode: color-dodge;    // 颜色减淡
mix-blend-mode: color-burn;     // 颜色加深
mix-blend-mode: hard-light;     // 强光
mix-blend-mode: soft-light;     // 柔光
mix-blend-mode: difference;     // 差值
mix-blend-mode: exclusion;      // 排除
mix-blend-mode: hue;            // 色相
mix-blend-mode: saturation;     // 饱和度
mix-blend-mode: color;          // 颜色
mix-blend-mode: luminosity;     // 亮度
```

### 文字斜体

```css
font-style: italic;
```

### border边框的虚线

```css
border-style:dotted;/*点状*/
border-style:solid; /*实线*/
border-style:double;/*双线*/
border-style:dashed;/*虚线*/
```

### 加下划线，字下面的线

```css
text-decoration: underline;
```

### 行高

```css
line-height:20px;
```

### 去掉input:text点击后出现的框

```css
input {
      outline: none;
}
```

### 三个小点---文字溢出省略

```css
/*1.实现单行文本的溢出显示省略号*/
{
     overflow: hidden;
     text-overflow:ellipsis;
     white-space: nowrap;
} 

/*2.实现多行溢出显示省略号（因使用了WebKit的CSS扩展属性，该方法适用于WebKit浏览器及移动端）*/
{
     display: -webkit-box;
     -webkit-box-orient: vertical;
     -webkit-line-clamp: 3;
     overflow: hidden;
}
```

### 文本特殊css样式

- 空白忽略

  ```css
  white-space: nowrap;
  ```

- 文本超出宽度写三个小点

  ```css
  text-overflow:ellipsis;
  ```

- 文本超出换行

  ```css
  word-break: break-all;
  ```

### 滚动条样式

```css
::-webkit-scrollbar {
    height: 100%;
     width: 12px;
}
/* 滚动槽 */

::-webkit-scrollbar-track {
     /* -webkit-box-shadow: inset006pxrgba(0, 0, 0, 0.3); */
     border-radius: 10px;
}
/* 滚动条滑块 */

::-webkit-scrollbar-thumb {
     border-radius: 10px;
     background: rgba(0, 0, 0, 0.1);
}

::-webkit-scrollbar-thumb:window-inactive {
     background: rgba(0, 0, 0, 0.1);
     /* background: rgba(255, 255, 255, 0.4); */
}
```

### 隐藏水平滚动条，同时允许垂直滚动条

```css
.scrollbar::-webkit-scrollbar {
  display: none; /* Chrome Safari */
}

.scrollbar {
  scrollbar-width: none; /* firefox */
  -ms-overflow-style: none; /* IE 10+ */
  overflow-x: hidden;
  overflow-y: auto;
}
```

### 按钮点击有个框，去除这个框

```css
.btn{
     outline:none;
}
```

### 字体渐变色

```css
background-image: -webkit-linear-gradient(bottom, #fd8403, #ff0000);
/* 把背景颜色附着到文字上*/
-webkit-background-clip: text;
/* 把文字颜色设为透明*/
-webkit-text-fill-color: transparent;
```

### 仿苹果的高斯模糊

```css
backdrop-filter: blur(10px);
-webkit-backdrop-filter: blur(10px);
background-color: #33333350;
```

### 字体镂空

```css
span{
  color:#ffffff00;
  -webkit-text-stroke:1px #ffffff;
}
```

### calc()函数计算像素

```css
.div {
  width: calc(100% / 6);
}
```

### 瀑布流布局

- column 实现瀑布流主要依赖两个属性。
- 一个是 column-count 属性，是分为多少列。
- 一个是 column-gap 属性，是设置列与列之间的距离。

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        .box {
            margin: 10px;
            column-count: 3;
            column-gap: 10px;
        }
        
        .item {
            margin-bottom: 10px;
        }
        
        .item img {
            width: 100%;
            height: 100%;
        }
    </style>
</head>

<body>
    <div class="box">
        <div class="item">
            <img src="./img/hotel1.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel2.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel3.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel4.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel5.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel6.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel7.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel8.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel9.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel10.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel11.jpg" alt="" />
        </div>
        <div class="item">
            <img src="./img/hotel12.jpg" alt="" />
        </div>
    </div>
</body>
```

### 字体的分类

1. UItralight
2. Thin
3. Light
4. Regular
5. Medium
6. Semibold
7. Bold
8. Heavy
9. Black
