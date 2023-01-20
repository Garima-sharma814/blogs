# Pseudo-classes and pseudo-elements

CSS provide useful selector types that focus on specific platform state, like when the element is hovered, active etc.

## Pseudo-Classes
HTML here find themselves in various stages either because they are interacted with user or one of their child element is in a certain state. 

For example, an HTML element could be hovered with the mouse pointer by a user or a child element could also be hovered by the user. For those situations, use the `:hover` pseudo-class.

```css
/*When the link is hovered with a mouse pointer this code is fired*/
a:hover {
color: blue;
text-decoration: underline;
}
```

> *Pseudo-classes let you apply CSS based on state changes. This means that your design can react to user input and changes accordingly.*

For example 
you have an email signup form, you can change the border color of the field to red, if it contains invalid email address and green when it contains correct email address.

As stated above pseudo-class let us apply CSS based on user input. Entering an email address is the input of the user. (whether right or wrong)

**How do you do that?**
Well, we have a pseudo-class `:invalid`, this is one of many browser-provided **pseudo-class**

%[https://codepen.io/garima-sharma814/pen/MWpNWqJ]

A pseudo-class lets you apply styles based on state changes and external factors. This means that your design can react to user input such as an invalid email address. 

### Interactive States

We can apply the following pseudo-classes on the interaction of a user with our page.

- **:hover**
If the user is pointing to an element with a pointing device (can be a mouse), an they place it over an element, we can trigger the action of the user with `:hover` class to apply different style when user *hovers* on it.

%[https://codepen.io/garima-sharma814/pen/mdWNdZZ]

**We can achieve this effect with little effort**
```html
<p> This is link <a href="#"> Try hovering me! </a> </p>
```

```css 
/*This line is to remove the default behavior of anchor tag we want underline effect one hover */
a{ 
    text-decoration: none; 
}

/*When the user hover on a tag this code will be fired*/
a:hover{
    text-decoration: underline;
    color: #8e44ad;
}
```

- **:active**
This state is triggered when an element is actively being interacted with— such as a click—before click is released. If a pointing device like a mouse is used, this state is when the click starts and hasn't yet been released.

%[https://codepen.io/garima-sharma814/pen/QWpewNd]

**We can achieve this effect with little effort**
```html
<div>
<button class="btn">Click and hold to see the active state</button>
</div>
```

```css
.btn:active {
  transform: scale(0.99);
  box-shadow: none;
}
```

There are tons of pseudo-classes for us to explore on. If you want to know more go to [Pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

## Pseudo-Elements 
Pseudo-elements differ from pseudo-classes because instead of responding to the platform state, they act as if they are inserting a new element with CSS. Pseudo-elements are also syntactically different from pseudo-classes, because instead of using a single colon (:), we use a double colon (::).

>A pseudo-element is like adding or targeting an extra element without having to add more HTML. 


For example
If you've got an article of content and you want the first letter to be a much bigger drop cap— how do you achieve that?

In CSS, you can use the `::first-letter` pseudo-element to achieve this sort of design detail.

```css
p::first-letter {
  color: blue;
  float: left;
  font-size: 2.6em;
  font-weight: bold;
  line-height: 1;
}
```
%[https://codepen.io/garima-sharma814/pen/yLMmyjK]

**::before and ::after**

Both the `::before` and `::after` pseudo-elements create a child element inside an element only if you define a content property.

```css
.my-element::before {
  content: "";
}
```

```css
.my-element::after{
  content: "";
}
```

`::before` pseudo-element to insert content at the start of an element, or the `::after` pseudo-element to insert content at the end of an element.

Pseudo-elements aren't limited to inserting content, though. We can also use them to target specific parts of an element.

The content can be any string even an empty one but be mindful that anything other than an empty string will likely be announced by a screen reader. We can add an image `url`, which will insert an image at its original dimensions, so we won't be able to resize it.

There are tons of pseudo-classes for us to explore on. If you want to know more go to [Pseudo-Elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

Written and Edited by [me](https://twitter.com/garimavatss)❤.



