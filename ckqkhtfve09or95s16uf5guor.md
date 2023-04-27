---
title: "CSS- The Cascade !"
datePublished: Thu Jul 01 2021 05:49:58 GMT+0000 (Coordinated Universal Time)
cuid: ckqkhtfve09or95s16uf5guor
slug: css-the-cascade
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682614277005/d00b6ec7-defa-4eb7-8829-efcb3f477597.png
tags: css3, webdev, html5, beginners

---

CSS stands for Cascading Stylesheets. The Cascade is the algorithm for solving conflicts where multiple CSS rules are applied to an HTML element. If we have this `<p>` tag ...
```html
<p> Let's Check which color is chosen by the browser </p>
```

```css
p{
color: red;
}

p{
color: blue;
}
```
**Which color will be rendered?**

%[https://codepen.io/garima-sharma814/pen/QWvwRRq]

**So why this happened ?**

Understanding the cascade algorithm helps us understand how the browser resolves the conflicts like these .. 

### The Cascade can split into 4 stages 

**1. Position and order of appearance** :- The order in which the CSS rule appear in the Stylesheet. 

**2. Specificity** :- An algorithm which determines which CSS property have strongest preference.

**3. Origin**:- the order of when CSS appears and where it comes from, whether that is a browser style, CSS from a browser extension, or your authored CSS.

**4. Importance** :- some CSS rules are weighted more heavily than others, especially with the `!important` rule type.

## Position and Order of Appearance

The order in which our CSS rules appear in the Stylesheet and their appearance is always taken into consideration by the cascade to calculate the conflicts if any. 

The demo right at the start of this blog is the most straightforward example of positioning. There are two rules that have selectors of identical specificity, so the last one to be declared won.

Styles can come from various sources on an HTML page, such as a `<link>` tag, an embedded `<style>` tag, and inline CSS as defined in an element's style attribute.

If you have a `<link>` that includes CSS at the top of your HTML page, then another `<link>` that includes CSS at the bottom of your page, the bottom `<link>` will have the most preference. The same thing happens with embedded `<style>` elements, too. They get more specific, the further down the page they are.

This ordering also applies to embedded `<style>` elements. If they are declared before a `<link>`, the linked stylesheet's CSS will have the most specificity.

An inline style attribute with CSS declared in it will override all other CSS, regardless of its position, unless a declaration has `!important` defined.

Position also applies in the order of your CSS rule. In this example, the element will have a purple background because `background: purple` was declared last. Because the green background was declared before the purple background, it is now ignored by the browser.

```css
.my-element {
  background: green;
  background: purple;
}
```

## Specificity

Specificity is an algorithm which determines which CSS selector is the most specific, after those calculations. By making a rule more specific, you can cause it to be applied even if some other CSS that matches the selector appears later in the CSS.

Suppose that we are working this HTML and CSS.

```html
<button class="btn">Hello, Specificity!</button>
```

```css
button {
  color: red;
}

.btn{
  color: blue;
}
```

There's two competing rules here. One will color the button red and the other will color it blue. 

Which rule gets applied to the element? 
Understanding the CSS specification's algorithm about specificity is the key to understanding how CSS decides between competing rules.

Specificity is one of the four distinct stages of the cascade.


### Preference of Selectors from lowest to highest 

**1. Universal Selector**
A universal selector (*) has no specificity and gets 0 points. This means that any rule with 1 or more points will override it.

```css
*{
margin: 0;
padding: 0
}
```

We usually use this to reset the default properties of CSS.

**2. Element or pseudo-element selector**
An element (type) or [pseudo-element](https://dev.to/garimasharma/pseudo-classes-and-pseudo-elements-npp) selector gets 1 point of specificity .

#### Type selector

```css
div {
  color: red;
}
```

#### Pseudo-element selector

```css
::selection {
  color: red;
}
```
**3. Class, pseudo-class, or attribute selector**
A class, pseudo-class or attribute selector gets 10 points of specificity.

#### Class selector

```css
.my-class {
  color: red;
}
```

#### Pseudo-class selector

```css
:hover {
  color: red;
}
```

#### Attribute selector

```css
[href='#'] {
  color: red;
}
```

The :not() pseudo-class itself adds nothing to the specificity calculation. However, the selectors passed in as arguments do get added to the specificity calculation.

```css
div:not(.my-class) {
  color: red;
}
```

This example would have 11 points of specificity because it has one type selector (div) and one class inside the :not().

**4. ID selector**
An ID selector gets 100 points of specificity, as long as you use an ID selector (#myID) and not an attribute selector ([id="myID"]).

```css
#myID {
  color: red;
}
```

**5. Inline style attribute**
CSS applied directly to the style attribute of the HTML element, gets a specificity score of 1,000 points. This means that in order to override it in CSS, you have to write an extremely specific selector.


```html
<div style="color: red"></div>
```

**6. !important rule**
Lastly, an !important at the end of a CSS value gets a specificity score of 10,000 points. This is the highest specificity that one individual item can get.

An !important rule is applied to a CSS property, so everything in the overall rule (selector and properties) does not get the same specificity score.

```css
.my-class {
  color: red !important; /* 10,000 points */
  background: white; /* 10 points */
}
```
There are a lot of [Selectors](https://dev.to/garimasharma/css-selectors-3co4) with their specificities for more go to references.

References

- [MDN specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)
- [CSS SpciFISHity](http://specifishity.com/)
