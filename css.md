css selectors:
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

font: font-style font-weight font-size(*)/line-weight font-family(*)
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

background:
background-color: transparent|color;
background-image:none|url(url);
