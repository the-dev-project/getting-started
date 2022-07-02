# HTML Part 1

## Table of Contents

- [What Is HTML?](#htmlintro)
- [Structure Of An HTML Page](#htmlstructure)
- [How And Where Can We Write HTML Code?](#htmlcode)
- [HTML Playground](#playground)
- [References](#references)

## <a name="htmlintro"></a> What Is HTML?

HTML stands for <strong style="color:red">H</strong>yper<strong style="color:red">t</strong>ext <strong style="color:red">M</strong>arkup <strong style="color:red">L</strong>anguage. It is a markup language for the web that defines the structure of web pages.

It is the basic building blocks of every website so it is the foundation of web development.

Abbreviation breakdown:

- **Hypertext** - Text that connects one web page to the other.
- **Markup** - A style guide for anything to be printed in hard copy or soft copy format.
- **Language** - A language that can be understood by the computer.

_Note: Hypertext is a specific case of Hyperlink. Hypertext is text with hyperlinks and hyperlink is a link that can be on an image, video, etc._

## <a name="htmlstructure"></a> Structure Of An HTML Page

A very basic and complete HTML page is like this:

```html
<!DOCTYPE html>
<html>
  <head></head>
  <body></body>
</html>
```

HTML pages consist of HTML elements. An element is defined by a start tag, some content, and maybe an end tag. For example:

- `<h1>This is a heading</h1>`
  - Everything from `<h1>...</h1>` is an element.
  - `<h1>` is the start tag.
  - `</h1>` is the end tag.
  - `This is a heading` is the element content.

There are two types of _tags_:

1. A tag that requires an opening and a closing. For e.g. The paragraph tag `<p>This is a paragraph</p>`
2. A self closing tag. For e.g. The image tag `<img src="image.jpg" alt="Alternate Text for the image" />`

Let's take a closer look at the tags we seen so far.

- `<!DOCTYPE html>` : This declaration defines that this document is an HTML5 document. This helps the browser to display the webpage correctly.
- `<html>` : This element is the root element of an HTML page.
- `<head>` : This element contains information about the HTML page.
- `<body>` : This element defines the HTML document's body and it is a container for all the visible content on a page like, headings, paragraphs,links, images, lists, etc.

HTML tags also contain something called _"attributes"_. Attributes are present in the opening tag. Attributes contain values which convey more information about the element and they can also help do things like, styling the element and manipulating the element with JavaScript.

An example would be:

```html
<h1 class="heading">This Is A Heading</h1>
```

In the above example:

- `class` : Is an attribute.
- `heading` : Is the value of the `class` attribute.

## <a name="htmlcode"></a> How And Where Can We Write HTML Code?

Fortunately writing HTML doesn't require any specific software. We can write HTML code in any text editor we like! We can write HTML even in Notepad! However, there are some text editors that are specifically made for web development, like VS Code!

The advantage of writing HTML in something like VS Code as opposed to Notepad is that VS Code provides a lot of tools that can make writing HTML very simple. For example, VS Code provides syntax highlighting, auto closing of tags, etc.

## <a name="playground"></a> Playground

- [JSFiddle](https://jsfiddle.net/)
- [JSBin](https://jsbin.com/?html,output)

## <a name="references"></a> References

- [FreeCodeCamp: What is HTML?](https://www.freecodecamp.org/news/what-is-html-definition-and-meaning/) - FreeCodeCamp is an excellent resource to start learning HTML. All the lessons here are interactive.
- [W3Schools: HTML](https://www.w3schools.com/html/default.asp) - W3Schools is another great resource to learn HTML.
- [MDN Web Docs: HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) - Mozilla Developer Network (MDN) Web Docs consists of documentation about everything there is to know about the web.
