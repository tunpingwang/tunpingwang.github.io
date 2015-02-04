Issues
==

1. Text Becomes Invisible
--

the following styling for text fading has some strange issues (*I only wrote for webkit for now*).

this block contains a heading before the paragraph. when displayed, the following issues occur: 

- first, all texts appear to be invisible for unknown reasons.
- when highlighted and/or zoomed in, text in **paragraph** may start to display with correct styling effects. The heading may still be invisible at this point.
- highlight the **heading** and zoom in again, then the heading may start to appear.
- after reloading/remaining on browser tab for some time, text may appear 

```html
<section class="article2">
	<h3>Title of 1st article </h3>
	<p>Serp derpler ter herp berp derpy herpler. Derperker derps merp ner perper herderder derpler herp derp. Derperker sherpus derps der berp derpy.
	</p>
</section>
```

```css
.article2 {
max-width: 40%;
height: 300px;
margin: 20px auto 20px auto;
font-family: "minerva-modern",sans-serif;
text-indent: 50px;
line-height: 1.3em;
display: block;
overflow: hidden;
text-overflow: ellipsis;
content: "";
background: -webkit-linear-gradient(#000 120px, #fff);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
}

.article2 h3 {
text-indent: 0;
text-align: center;
}
```
1. text becomes invisible

![invisible]
{http://i.imgur.com/hmCyNe5.jpg}

2. after highlighting & zoomed in, paragraph text appears

![paragraph]
{http://i.imgur.com/MqHlj5D.jpg}

3. highlight & zoom to make heading appear

![heading]
{http://i.imgur.com/QNF4VMt.jpg}
