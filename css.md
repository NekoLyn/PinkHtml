【css selectors】
html label

.class 样式点定义 结构类调用
multiple classes:
<div class="red news size1"></div>

# id 样式#定义 结构类调用 只能调用一次

* ==select all
* {
    margin: 0;
    padding: 0;
}

font-family: 'New Times Roman', Times, 'Microsoft Yahei';

font-size: 20px;
headings excluded, should be defined sperately

font-weight: bold, 400=normal, 100-900;

font-style: normal ==change <em>to normal, italic;

(combined)font: font-style font-weight font-size(*)/line-height font-family(*)
font: italic 700 16px Times;

color: pink;
color: #cc00ff;
color: rgb(255,0,0);

text-align: center, right, left;

text-decoration: none, underline, overline, line-through;

text-indent: 10px, 2em;

line-height: 20px; ===top height+bottom height+text size

<style></style>
<div style=" " ></div>
<link rel="stylesheet" href="style.

Descendant combinator：
<ul>
<li></li>
<li><a href="#"></a></li>
</ul>
ul li a {
    color: red;
}
<ul class="nav">
<li></li>
<li><a href="#"></a></li>
</ul>
.nav li a {
    color: red;
}

Child combinator：
<div class="nav">
   <p></p>
   <a>son</a>
   <p>
     <a>grandson</a>
   </p>
</div>
.nav a {

} == all <a>

.nav > a {

} == only son <a>

combinator:
<div></div>
<p></p>
<ul class="pig">
    <li></li>
     <li></li>
</ul>
div,
p,
.pig li {
    color: red;
}

Pseudo:
LVHA
a: link
a: visited
a: hover == mouse hover
a: active == click
eg.
a{
    color: #333;
    text-decoration: none;
}
a: hover {
    color: #369;
    text-decoration: underline;
}

input: focus{
    background-color: pink;
}

【line and block】
block-level
h1, p, div, ul, ol, li
==>box layout; p cannot contain div/other boxes

line-level
a, strong, b, em, i, del, s, ins, u, span
==>no width/height, width=text length; <a>can contain blocks,  <a>cannot contain <a>

line&block
img, input, td
==> display in one line, can set width/height

turn line to block
eg. <a href="#"><a>
a {
    color: red;
    display: block;}

turn block to line
display: inline ==> automatically disable width/height

turnto inline-block
display: inline-block

vertical-center:
(block)height=40px
line-height=40px

【background】
background-color: transparent|color;
background-image:none|url(url);
background-repeat: repeat(default)|no-repeat|repeat-x|repeat-y;
background-position:x y; x|y === top center left right bottom (default=center if not being defined)
or background-position:x y; x|y===px location; eg 50px center
background-attachment: scroll(default)|fixed;
(combined) background: background image repeat attachment position;
eg. background: transparent url(image.jpg) no-repeat fixed 50xp center;
background: rgba(0,0,0,0.3); a===alpha 0-1 0.3= .3

css三大特性：
层叠性：就近原则
继承性：文本和颜色相关
（行高的继承：font:12px/28px or font:12px/1.5 ===times 1.5）
优先级：
继承 0000《 元素 0001《类|伪类 0010《ID 0100《行内 1000《！important infinite
(<a>has default style)
(权重叠加：combinator 0001+0001=0002 > single selector 0001 but 0002 < 0010; 00010 不会进位成0010)

layout=box float position
【Box model】
border:
border width:1px;
border style:solid/hidden/dashed/dotted;
border-color: pink;
(combined)border: width style color;
border top/bottom/right/left: 5px solid pink; (层叠性)
table,
td {
    border：width style color;
    border-collapse: collapse;
    font-size: 15px;
    text-align: center;
}
box width = content width+padding-r+padding-l+ border width*2

content: border to content = padding

padding:
padding-top/bottom/right/left:5px;
padding: 1px; 4 sides;
padding: 1px 5px; t/b =1px r/l=5px;
padding: 1px 5px 8px; t=5px r/l 5px b=8px;
padding: 1px 5px 8px 10px; t=1 r=5 b=8 l=10;

margin:
margin-l/r/b/t
center a box: (box must have a width) margin: 0 auto;
嵌套元素垂直外边距塌陷 ==>
set father border-top: 1px solid transparent;
set father margin-top: 1px;
overflow: hidden;
清除网页内外边距：

* ｛
  margin：0；
  padding: 0;
｝

border-radius:
border-radius:10px|20% ; ===>50% =circle
border-top-left:px|%;
border-radius:lefttop rightbottom ;
border-radius:lefttop righttop rightbottom leftbottom;

box-shadow:
h-shadow(*) v-shadow(*) blur spread color(rgba) inset(ouset=default)

text-shadow:
h-shadow(*) v-shadow(*) blur spread color(rgba)

float:
none|left|right ===> automatically turn to block

clear float:

1. add a block
.last:{
    clear: both;
}
2. .father: {
    overflow: hidden;
}
3. father add.clearfix: after {
    content: "";
    display: block;
    height: 0;
    clear: both;
    visability: hidden;
}

.clearfix {
    zoom: 1;
}

4. clearfix: after, clearfix: before {
    content: "";
    display: block;
    height: 0;
    clear: both;
    visability: hidden;
}

.clearfix {
    zoom: 1;
}
