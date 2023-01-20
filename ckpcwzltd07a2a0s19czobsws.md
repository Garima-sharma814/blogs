# CSS Box Model

# What is Box model?
Box model refers to how HTML elements are modeled or rendered in browser engines and how much dimensions HTML elements are derived from CSS properties. It is the composition of the HTML elements on the web pages. 

### Say you have an HTML element 

```html
<p> This is a paragraph that has few words in it.</p>
```

### Then you have to write a bit of CSS for it.

```css
p{
 height: 50px;
 width: 100px;
 border: 1px solid black;
 padding: 1rem;
}
```
The content of the paragraph would break out of the element and it would be 136px wide rather than 100px. **Why is that?**

%[https://codepen.io/garima-sharma814/pen/QWpaybX]

#### Try and edit it on codepen.io

As we can see the content of the paragraph is the content of the paragraph is sneaking out of the element why it is so?

If we inspect of the element i.e. the paragraph 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622481217770/gi1nW2v47.png)
The blue area represents  the actual element i.e. 100x50px, but there is a green area named padding, as we added `1rem` of padding in the element it creates a pad inside the element of 16px `1rem=16px` so it adds 16px to the actual height and width of the element now the element is or 136px wide. 

A really important thing to remember when writing CSS, or working on the web as a whole, is that everything displayed by CSS is a box. Whether that's a box that uses `border-radius` to look like a circle, or even just some text: the key thing to remember is that it's all boxes.

## Content and Sizing 
Boxes shows different behaviors based on their `display` value, their `dimensions` and the `content` that is inside them. A Box can have different child boxes inside it. Based on all this is boxes shows different behaviors. 

You can control this by using `extrinsic sizing`, or, you can continue to let the browser make decisions for you based on the content size, using `intrinsic sizing`. Try this on codepen

%[https://codepen.io/web-dot-dev/pen/abpoMBL]
>Note: This pen is not owned by me! all credits to web.dev

The pen has the words, "CSS is awesome" in a box with fixed dimensions and a thick border. The box has a width, so is **extrinsically** sized. It controls the sizing of its child content. The problem with this though, is that the word "awesome" is too large for the box, so it overflows outside of the parent box's border box. One way to prevent this overflow is to allow the box to be intrinsically sized by either unsetting the `width`, or in this case, setting the width to be `min-content`. The min-content keyword tells the box to only be as wide as the intrinsic minimum width of its content (the word "awesome"). This allows the box to fit around "CSS is awesome", perfectly.

## Area of the Box-Model

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622482975517/4PI-qFrLW.png)

This follows a slang ie. MBPE
- Margin
- Border
- Padding 
- Element/Content

The most inner part is the **content box** that is the area where the content resides. As we seen before this can control the size of the parent.

Then comes the **padding area** that surrounds the **content box** this is created by the `padding`
property and this is always inside the box.

The **border box** surrounds the **padding box** and its space is occupied by the border value. The border box is the bounds of your box and the border edge is the limit of what you can visually see. The `border` property is used to visually frame an element.

The final area, the **margin box**, is the space around your box, defined by the margin rule on your box. Properties such as `outline` and `box-shadow` occupy this space too because they are created on top, so they don't affect the size of our box. 

## Resources 
- [Introduction to the box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
- [What are browser developer tools?](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)

## User agent stylesheets 
- [Chromium](https://chromium.googlesource.com/chromium/blink/+/refs/heads/main/Source/core/css/html.css)
- [Firefox](https://searchfox.org/mozilla-central/source/layout/style/res/html.css)
- [Webkit](https://searchfox.org/mozilla-central/source/layout/style/res/html.css)


