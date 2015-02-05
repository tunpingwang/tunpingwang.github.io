Issues
==

1. Text Becomes Invisible
--

**Below is the styling code for text fading, which has some strange issues** (*I've only written for & tested on webkit browsers for now*).

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

**When shown in browser, the following issues may occur:**

1. first, all texts appear to be invisible for unknown reasons. (*text block is below the "Double Liked"*)

	![invisible](http://i.imgur.com/hmCyNe5.jpg)

2. after highlighted and/or zoomed in, text in **paragraph** may start to display with correct styling effects. The heading may still be invisible at this point.

	![paragraph](http://i.imgur.com/MqHlj5D.jpg)

3. highlight the **heading** and zoom in again, then the heading may re-appear.

	![heading](http://i.imgur.com/QNF4VMt.jpg)

4. However, after reloading/having page remaining on browser tab for some time, this problem sometimes goes away. Is it something to do with caching?
