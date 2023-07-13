```
<div>take one line</div>
<span>side by side</span>
<img
    src="imgURL"
    alt="img despription"
    title="img nasme "
    width="100"
    height="200"
    border="10" key="value"
>
src="img.jpg" == same folder
src="images/img.jpg" == "/"
src="../img.jpg" == "../"
```

`src="c:\User\Lyn\images\img.jpg"`  or `"http://www.cat.com/images" == absolute path`

<a href="url" target="\_self" or "\_blank">text or <img src="img.jpg"></a> == open at current window or new window
<a href="img.zip" or ".doc" or ".exe">download</a>
<a href="#two">ankle link</a>

<!-- turn to specific section on the same page by adding id to a label eg. <h2 id="two">Number two</h2> -->

`src="img.jpg" == same folder`

```src="img.jpg" == same folder```

space: &nbsp;
<: &lt; >: &gt;

<table>
<th>bold and in middle</th>
</table>
align : left center right
border: 1 or ""
cellpadding==content to border
cellspacing==cell itself
width
height

merge cell:
rowspan:target cell on top
colspan:target cell on left
<td colspan="3"></td>
then delete the merged cells

The Unordered List
<ul>
<li></li>
<li></li>
</ul>

the ordered list
<ol>
<li></li>
<li></li>
</ol>

user-defined list
<dl>
  <dt>number</dt>
  <dd>1</dd>
  <dd>2</dd>
</dl>

form
<form action="url"  method==submiting method eg. "post" name="form name">
...text...
<input
type="text/password/radio/checkbox/submit/file/reset"
name==input's name
value
checked="checked" ==automatically ticked when loading
maxlength
>
</form>

label
<label for="abc"></label>
<input type="text" id="abc">

select
<select>
<option select="selected">1</option>
<option>2</option>
<option>3</option>
<option>4</option>
</select>

textarea
support multiple lines
<textarea coles="5" rows="50"></textarea>
