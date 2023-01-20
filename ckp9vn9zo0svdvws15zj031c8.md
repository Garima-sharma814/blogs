# Markdown Cheat Sheet Part-3

# Images 
There are 2 ways to add an image to the Markdown.
1. Inline style 
2. Referenced style 

```
Inline Style:
![First image](http://picsum.photos/200/200)
Referenced Style:
![First image][I'm referenced]
- [I'm referenced]: http://picsum.photos/200/200
```
> Make sure you don't add any symbol in the referenced style I just used it to make it visible.

Inline Style:
![First image](http://picsum.photos/200/200)
Referenced Style:
![First image][I'm referenced]
[I'm referenced]: http://picsum.photos/200/200

## How to add logo to the image?
As you can see in the above images if you hover nothing is appearing but if we add a logo to the image it can just give an instance what the images is about or the info of the image.
### Let's see how to add logo to the image
```
Inline Style: 
![First image](http://picsum.photos/200/200 "Hey I'm the logo")

Referenced Style:
![First image][I'm referred]
- [I'm referred]: http://picsum.photos/200/200 "Hey I'm the logo"

```
> Make sure you don't add any symbol in the referenced style I just used it to make it visible.

- We just added a logo after the link in double quotes

# How to add Inline text?
``` Inline codes or text have `back ticks` around it. ```
    or when intended by 4 spaces.

 
* But if you want to add multiple lines to the inline block use 3 ticks ' ``` ' around it or when intended by 4 spaces. 


* But the fenced blocks(having `backticks` around it) are always preferred and recommended because only the fenced blocks can support code syntax highlighting.

# What is Code and syntax highlighting?

Stay tuned for part-4...