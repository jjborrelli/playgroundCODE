# Learning HTML with Codecademy

## HTML Basics
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