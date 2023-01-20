# Markdown Cheat Sheet Part-4

# Code and Syntax Highlighting 
Code block is the part of *Markdown spec*, but code highlighting isn't. However many renderer's like *GitHub* and *Markdown Here* supports __Code and Syntax Highlighting__. *Markdown Here* supports a lot of languages. To see the complete list check [this](https://highlightjs.org/static/demo/) `Flash Warning!`.

If you read [part-3](https://dev.to/garimasharma/how-to-write-markdown-part-3-3m0c) you might be knowing about fenced blocks. 
- Fenced blocks are the inline blocks have back ticks around.

Blocks of code are either fenced by lines with three back-ticks, or are indented with four spaces. I recommend only using the fenced code blocks they're easier and only they support syntax highlighting.
```python
s = "Python syntax highlighting"
print(s)
```
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
```
No language indicated, so no syntax highlighting.
```
- This is known as code and syntax highlighting.
- You can achieve this by adding three backticks before for code and the name of the language you have written.
- [Know more](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code-and-syntax-highlighting)

## More Examples
- HTML

```html
<!DOCTYPE html>
<title>Title</title>

<style>body {width: 500px;}</style>

<script type="application/javascript">
  function $init() {return true;}
</script>

<body>
  <p checked class="title" id='title'>Title</p>
  <!-- here goes the rest of the page -->
</body>
```
- CSS

```css
@font-face {
  font-family: Chunkfive; src: url('Chunkfive.otf');
}

body, .usertext {
  color: #F0F0F0; background: #600;
  font-family: Chunkfive, sans;
  --heading-1: 30px/32px Helvetica, sans-serif;
}

@import url(print.css);
@media print {
  a[href^=http]::after {
    content: attr(href)
  }
}
```
- C++

```c++
#include <iostream>

int main(int argc, char *argv[]) {

  /* An annoying "Hello World" example */
  for (auto i = 0; i < 0xFFFF; i++)
    cout << "Hello, World!" << endl;

  char c = '\n';
  unordered_map <string, vector<string> > m;
  m["key"] = "\\\\"; // this is an error

  return -2e3 + 12l;
}
```
- [know more languages](https://highlightjs.org/static/demo/)

# Tables 
Tables aren't part of the core Markdown spec, but they are part of GFM(GitHub Flavored Markdown) and *Markdown Here* supports them. 
```
This is the neat table 

| The           | neat          | table       |
| ------------- | ------------- | ----------- |
| well          | this          | is  the     |
| neat          | and  pretty   | way         |
| to            | make          | tables      |
```

This is the neat table 

| The           | neat          | table       |
| ------------- | ------------- | ----------- |
| well          | this          | is  the     |
| neat          | and  pretty   | way         |
| to            | make          | tables      |

```
There exist a less neat way to make tables
still renders neat and clean.

| The less| neat | table |
| --- | --- | --- |
| well |this| is less |
| neat | and  pretty | but |
| still  | renders | neat |
```
There exist a less neat way to make tables
still renders neat and clean.

| The less| neat | table |
| --- | --- | --- |
| well |this| is less |
| neat | and  pretty | but |
| still  | renders | neat |

### We can use inline blocks, italic and bold words in the tables.
 ```
Using other properties in the table 

| The           | neat          | table       |
| ------------- | ------------- | ----------- |
| well          | this          | is  the     |
| *neat*        | **and pretty**| `way`       |
| to            | make          | tables      |
```
Using other properties in the table

| The           | neat          | table       |
| ------------- | ------------- | ----------- |
| well          | this          | is  the     |
| *neat*        | **and pretty**| `way`       |
| to            | make          | tables      |

- If you don't know these you can have a look to my blogs 
[part-1](https://garimasharma.hashnode.dev/how-to-write-markdown)
[part-2](https://garimasharma.hashnode.dev/how-to-write-markdown-part-2)
[part-3](https://garimasharma.hashnode.dev/how-to-write-markdown-part-3-1)
- There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. 
- It will work if you make them less neat....oh you getting my point. If not leave a comment.