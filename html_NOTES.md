# Learning HTML with Codecademy

## HTML Basics I
**HTML** = HyperText Markup Language   

-where *hypertext* is just "text with links in it"  
- a markup language is a programming language that can make text do more interesting things

**CSS** = Cascading Style Sheets, the code that makes webpages pretty

### Setting up the page's skeleton

1. always put `<!DOCTYPE html>` on the first line to tell the browser what language it is dealing with
2. putting an `<html>` on the second line starts the html document
3. don't forget to put the ending `</html>` on the last line  

### Terminology

1. inside the `<>`s are "tags"  
2. these almost always are paired; open and close (e.g. `<html> *other page stuff* </html>)  
	- think of them like parentheses
3. tags nest, so remember to close them in the correct order


		<first><second> text </second></first>



### The head and body  
Everything in the html document goes between the `<html></html>` tags, except the `<!DOCTYPE html>` tag

There are always two parts to an html file
1. the head
	- contains info about the html file, like the title (what you see in the page tab/title bar)
2. the body
	- where content goes, like text or images
	- goes inside `<html></html>` tags and after the `<head></head>`
	- paragraphs require the tag: `<p></p>


### Paragraphs and headings  
Give paragraphs headings with heading tags like `<h1></h1>`  

There are six heading sizes (h1 through h6)  

The parts of a hyperlink:
1. opening tag is `<a>`
2. within `<a>` tag is the `href` value
	- `href` tells the link where to go
3. between the tags `<a href="link">The text you want to click </a>`
4. tag closes with `</a>`

#### Images
Requires the image tag `<img>`  
Rather than putting content between tags, link goes within tag as `src` attribute  

e.g., `<img src = "url" />`  

So the `/` just goes at the end of the tag, but put a space between the url in quotes and the backslash

**Make the image a link**  
Just place the `<img src="url" />` tag in between the `<a href="link"></a>` tags


## HTML Basics II

**Ordered lists** = numbered list
1. starts with `<ol>`
2. each individual list item is bracketed by `<li></li>` tags
3. ends with `</ol>`

**Unordered lists** = list with bullet points
- same as *ordered list* but uses `<ul></ul>` tags  
- also uses `<li></li>` tags for each list item	  

#### Inline CSS:
**Comments** start with `<!--` and end with `-->`  
So a comment would be:  
	```
	<!-- This is my example comment-->
	```  

We can give tags more instructions by including *attributes* in the opening tag. The `src` in `<img>` and the `href` in `<a>` are both attributes. 

**Font Size** is changed with the *style* attribute. 
	```
	<p style="font-size: 12px">
	```  
In this case style is included in the `<p>` paragraph tag, and *font-size* is indicated in quotes, followed by a colon and the size indicated in *px* (pixels). 

**Font Color** is also changed with the `style` attribute. `style` can be used in many different tags. For example, we can change the color of a heading:
	```
	<h1 style="color:red">Red Header<h1>
	```
Like with `font-size` we indicate the attribution (`color` in this case and then tell it what color we want after the colon. 

To change both size and color a semicolon can be used to separate the two. 
	
	<h1 style="color:red;font-size:12px">Header<h1>
	

[A list of colors can be found by clicking here](http://www.w3.org/TR/css3-color/#svg-color)  

**Font Family** can also be changed with the `style` attribute. 

	
	<h1 style="font-family: Arial">Arial Header<h1>
	
  
[A list of available fonts can be found by clicking here](http://www.w3.org/TR/CSS21/fonts.html#generic-font-families)

**Background color** is yet another `style` option, where you set, for example, `style="background-color:red"`

*Style* also allows us to **align text** using `style="text-align:center"`

The `<strong></strong>` tag allows for **bold words and phrases** while the `<em></em>` tag allows for *italicized words and phrases*  

## HTML Basics III  
- Tables
	- store tabular data
	- uses `<table>` tag (with many others
	- `border` attribute draws border around the table: `<table border="1px">
		- `<table style="border-collapse:collapse"> 
- Rows
	- use `<tr>` to create table row
- Data
	- `<td>` tags define the data in the row
	- think of `<td>` tags like the `<li>` tags in a list
		- add multiple `<td>` to each row to generate columns
- Head 
	- `<thead>` info about the table
		- goes inside `<table>`
		- Start with opening `<thead>`
		- Then opening `<tr>` for row
		- The column heading is then contained within `<th></th>`
		- Close row and header with `</tr> and `</thead>`
	- `<tbody>` contains actual tabular data
		- goes inside `<table>`
		- surrounds the `<tr>` and `<td>` tags that have the data
- Title
	- requires *colspan* attribute of `<th>` tag
	- `<th colspan="3">3 columns across</th>`

#### Structure Tags

`<div></div>` is one of the most versatile structure tags. It allows you to divide your page into containers. 

	
	<div style = "width:50px; height:50px; background-color:green"></div>
	

`<span></span>` allows for finer scale control  


	<p>This text is one color while <span style="color:red">this text is another</span></p>
	

Can be used with a variety of attributes  
  
## CSS An Overview  
Two reasons to separate formatting (CSS) from content (HTML)  
1. apply the same formatting to several HTML elements without rewriting the code  
2. Apply similar appearance and formatting to several HTML pages from a single CSS file  

Two ways to apply CSS in one place
1. put the CSS between `<style></style>` tags in the same file as HTML
	- inside of the `<head></head>` tags
2. use a `<link>` tag in the `<head></head>`
	- needs a `type` attribute equal to `"text/css"`
	- needs a `rel` attribute equal to `"stylesheet"`
	- needs a `href` attribute that should point to the web address of the CSS file


	<link type="text/css" rel="stylesheet" href="stylesheet.css"/>


### Syntax
The general format:


	selector {  
		property: value;  
	}


Where the *selector* is any HTML element without the `<>`, the *property* is then the aspect of the selector (e.g., color, font-family, font-size, etc.), and the *value* is the setting for the property (e.g., red, Arial, 44px). Separate each property within a selector by a semicolon.

CSS **comments** are of a slightly different form than HTML comments:  

		
	/*A CSS comment*/


### Overview
To get a variety of different colors, use hexadecimal keys, search 'hex color palette' or 'hex color picker' for many options. These always start with a `#`, are up to 6 digits long, and are case-insensitive

`em` is a unit of relative size. A single `em` is whatever the default font size is of whatever screen is viewing it

#### Fonts 
Basic fonts of CSS:  

1. serif - font with little decorative bits on the ends of letter strokes  
2. sans-serif - plain looking font  
3. cursive - scripty font that looks like cursive writing   

You can provide a list of fonts to try


	p {
	   font-family: Tahoma, Verdana, sans-serif;
	}


In the above example the CSS will try Tahoma first, then Verdana, before going to the sans-serif font.

## Selecting HTML Elements  

Many HTML elements support the `border` property  
For example:

	td{
    	border: 1px dashed blue
	}	
	table{
   		border: 1px solid black
	}

sets a dashed blue border around the cells, and a solid black border around the whole table.

Links can be changed much like regular text. They also have the property of `text-decoration` to give them a bit more flair. 

	a {
    	color:cc0000;

		/*To prevent underlined links using text-decoration*/

    	text-decoration:none
	}  

*sidenote: the `</br>` tag inserts a line break*  

Some CSS attributes of div; creating a button

`margin:auto` tells the HTML to give equal margins to either side of the element
`text-align:center` centers text elements


# CSS Classes and IDs  
## CSS Selectors  

Any HTML element my be a CSS selector (e.g., h1 for `<h1></h1>`). 

If you want to select a particular tag, rather than all tags by selecting an ordered set of tags. For example, to select only the `<p></p>` tag within a nested set of `<div></div>` tags:

```
	<div>
		<div>
			<p>
				Selecting this line
			</p>
		</div>
	</div>
	<p> 
		And not this one
	</p>
```

Would require the css: 

```
	div div p{
		/*CSS things*/
	}
```

Apply CSS styling to *every* element of the page

```
	*{
		/*selector of everything*/
	}
```


### Branching

Thinking of HTML elements like a tree; elements "branch out" from the main trunk (`<html></html>` tags). The first two big branches are `<head>` and `<body>` and the branches multiply and become finer as you move down elements. 

```
	<!DOCTYPE html>
	<html> <!--The trunk of the tree!-->
		<head> <!--Child of html, parent of title,
			   sibling of body-->
			<title></title> <!--Immediate child of head,
							child of head AND html-->
		</head>
		<body> <!--Child of html, parent of p,
			   sibling of head-->
			<p></p> <!--Immediate child of body,
					child of body AND html-->
		</body>
	</html>
```

Above is a diagram of the "familial" relationships of the tags. An element is a child of every element wrapped around it.   

Using `div div p {/* some CSS */}1` will grab any p that is nested within a div somewhere that is also nested around another div. 

To select a p that is directly nested within another element use: `div > p { /* some CSS */}  

Some selectors will override others if they have greater specificity. For example: `ul li p{/*CSS*/}` will override `p{/*CSS*/}`  

Two selectors are more specific than nested selectors: **classes** and **ids**. 

#### Class example: 

Good for assigning the same characteristics to several different tag types.

```
	<div class="classname"></div>
```

With the associated CSS

```
	.classname{/*CSS*/}
```
Note the leading *period* in front of whatever the class is called. 

#### Id example: 

Good for assigning styling to exactly one element.

```
	<div id="idname"></div>
```

With the associated CSS

```
	#idname{/*CSS*/}
```  

### Pseudo-class selector  

A way of accessing HTML items that aren't part of the document tree. Pseudo selectors can control the appearance of unvisited vs visited links, even links that are being hovered over. Used as: 

```
	selector:pseudo-class_selector {
    	property: value;
	}
```
*(Simply the extra colon ":")*

#### Links  

Pseudo-class selectors for links  
- `a:link`: an unvisited link  
- `a:visited`: a visited link  
- `a:hover`: a link you are hovering a mouse over 

 
#### First child

The `first-child` selector is useful to apply styling only to elements that are first children of their parents. 

Can select any level of "child" with a pseudo-class selector.  

```
	p:nth-child(number.of.child){
		/*CSS*/
	}
```

Changes the number.of.child level child with CSS styling.

 
# CSS Positioning  
## CSS box model  

Each HTML element is like a tiny box or container that holds the pictures and text you specify

<img src="http://s3.amazonaws.com/codecademy-blog/assets/ae09140c.png"/>

### Display

1. block
	- element is a block box, takes width of page
2. inline-block
	- element is a block box, but allows other elements to sit next to it  
3. inline
	- element sits on the same line as another element, but without formatting it like a block (only takes as much width as it needs  
4. none
	- element and content disappears entirely  

### Box Layers  

1. margin - space around the element; the larger the margin the more space between the element and those around it
	- adjust the margin to move our HTML elements closer to or farther from each other

	```
	margin: top right bottom left
	```
2. border - edge of the element  
3. padding - spacing between content and border
	- moves border closer or further from the content  

	```
	padding: top right bottom left
	```
4. content - actual stuff in the box 


### Floats  

Tells HTML where to set the element

`clear` tells the element to get out of the way of the other elements  

if you don't specify and element's position it defaults to `static`  

`position` can be absolute, relative, or fixed  