# md-slide

## simple use

```
docker run --rm -p 8000:8000 -p 35729:35729 \
  -v "$PWD/slides.md":/reveal.js/md/ piuma/md-slide
```

Open browser at url http://localhost:8000

# Markdowm syntax guide

The separator *---* in a new line defines a stop mark to split
horizontal slides and *-* is a vertical slide separator.

Here's an overview of Markdown syntax that you can use anywhere on
GitHub.com or in your own _slides.md_ text file.

## Headers

## This is an `<h2>` tag
### This is an `<h3>` tag
###### This is an `<h6>` tag
```
## This is an <h2> tag
### This is an <h3> tag
###### This is an <h6> tag
```

## Emphasis
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

```
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

```

## Lists
Unordered

* Item 1
* Item 2
  * Item 2a
  * Item 2b

```
* Item 1
* Item 2
  * Item 2a
  * Item 2b
```

## Lists
Ordered

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
   
```
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

## Images
```
![GitHub Logo](/image/logo.png)
Format: ![Alt Text](url)
```

In this case you also add image directory in /reveal.js/md/ 
```
docker run --rm -p 8000:8000 -p 35729:35729 \
  -v "$PWD/slides.md":/reveal.js/md/ \
  -v "$PWD/image":/reveal.js/md/image \
  piuma/md-slide
```

## Links
http://github.com - automatic!
[GitHub](http://github.com)
```
http://github.com - automatic!
[GitHub](http://github.com)
```

## Blockquotes

As Kanye West said:

> We're living the future so
> the present is our past.

```
As Kanye West said:

> We're living the future so
> the present is our past.
```

## Inline code
I think you should use an
`<addr>` element here instead.

```
I think you should use an
`<addr>` element here instead.
```

## Syntax highlighting
```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
```
```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
```

## Task Lists
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

```
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```

## Tables

You can create tables by assembling a list of words and dividing them
with hyphens - (for the first row), and then separating each column
with a pipe |:

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

```
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
```

## Automatic linking for URLs

Any URL (like http://www.github.com/) will be automatically converted
into a clickable link.

## Strikethrough

Any word wrapped with two tildes (like `~~this~~`) will appear crossed out.

