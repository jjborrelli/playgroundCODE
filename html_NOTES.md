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

```
<first><second> text </second></first>
```


### The head and body  
Everything in the html document goes between the `<html></html>` tags, except the `<DOCTYPE html>` tag

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
	```
	<h1 style="color:red;font-size:12px">Header<h1>
	```

[A list of colors can be found by clicking here](http://www.w3.org/TR/css3-color/#svg-color)  

**Font Family** can also be changed with the `style` attribute. 
	```
	<h1 style="font-family: Arial">Arial Header<h1>
	```
  
[A list of available fonts can be found by clicking here](http://www.w3.org/TR/CSS21/fonts.html#generic-font-families)

**Background color** is yet another `style` option, where you set, for example, `style="background-color:red"`

*Style* also allows us to **align text** using `style="text-align:center"`

The `<strong></strong>` tag allows for **bold words and phrases** while the `<em></em>` tag allows for *italicized words and phrases*  

