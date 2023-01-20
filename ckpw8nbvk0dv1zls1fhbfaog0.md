# CSS Selectors

If you have got some text that you want to render in Red or any other color How would you do that?
for ex you have this element

```
<div>
<p> This is first paragraph in this div which is to be rendered in Red Color</p>
<p> This is second paragraph in this div which is normal </p>
</div>
```
You use a CSS selector to find that specific element and apply a CSS rule, like this.

```
div p:first-of-type {
  color: red;
  font-size: 1.5em;
}
```
CSS provides us a lot of options to select elements and apply specific rules to them, ranging from very simple to very complex, to help us to tackle situations like this.

%[https://codepen.io/garima-sharma814/pen/yLMQKyG]

## Parts of CSS rules 
To understand how selectors work and their role in CSS, it's important to know the parts of a CSS rule. A CSS rule is a block of code, containing one or more selectors and one or more declarations of property which we want to make change in our HTML element.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vwp7i6rfhvc9sbiwf3e7.png)

In this image, the selector is `.my-css-rule` which finds all elements with a class of `my-css-rule` on the page. There are three declarations within the curly brackets. A declaration is a property and value pair which applies styles to the elements matched by the selectors. A CSS rule can have as many declarations and selectors as you like.

## Simple Selectors
The most simple selectors of CSS are targeting the element by classes, ID and other attributes.

### Universal Selectors 
A universal selector is a selector which selects all the elements in HMTL file. Universal Selector is also known as wildcard. It matches all the elements.

```
*{
color: blue;
}
```

This rule will apply on each and every element of the HTML file.

### Type Selectors
Type selectors directly targets the HMTL element by its type/tag i.e. div, section etc.

```
p{
color: red;
}
``` 
This rule cause every <p> tag to render in red color.

### Class Selectors
An HTML element can have more than one class at a time. The class selector will target every element having that class.

```
<div class="test-class"> This is just a div </div>
```
We can select this div with its class.

```
.test-class{
color: blue;
}
```
In CSS , class is selected by a `.` this dot is not present in the HTML element. This means `.` is a character which instructs CSS to target all the elements having class `test-class`.

A HTML element that has a class of .test-class will still be matched to the above CSS rule, even if they have several other classes, like this:
```
<div class="test-class another-class some-other-classes"></div>
```
### Id Selectors

An HTML element with an `id` attribute should be the only element on a page with that ID value. An HTML element should not have more than 1 ID at a time (_good practices_) and if you have more than 1 ID in an element you code might break. You select elements with an ID selector like this:
```
<div id="test-id"></div>
```
We can select this div with this ID 

```
#test-id{
color: blue;
}
```
As seen in the class selector we can select the id by the `#` symbol. `#` symbol instructs CSS to target the element having this ID.

### Grouping Selectors
A selector doesn't have to match only a single element. You can group multiple selectors by separating them with commas:

```
h1, h2, h3, h4, h5, h6, .test-class, #test-id{
color: white;
```
### Complex selectors
You have already seen a lot of selectors, but sometimes, you will need more fine-grained control with your CSS. This is where complex selectors step in to help.

It's worth remembering at this point that although the following selectors give us more power, we can only cascade downwards, selecting child elements. We are not able to target upwards and select a parent element.

#### Combinators 
A combinator is an element which resides inside another element. For ex `<strong>` tag can reside inside a `<p>` tag. 

#### Descendant Combinators
Let's understand the relationship in Child and Parent tag. 

```
<p>A paragraph of text with some <strong> bold text for emphasis /strong>.</p>
```
The parent element is `<p>` tag child element is the `<strong>` tag. We can understand this because `<strong>` tag sits inside the `<p>` tag. So, <p> tag is the direct parent of `<strong>` tag.

A descendant combinator allows us to target the child element with the help of the parent tag. This use space to instruct about the parent-child relationship.

```
p strong{
color: red;
}
```

This rule will select all the `<strong>` tag which resides inside a `<p>` tag. 

#### Compound Selectors
You can combine selectors to increase specificity and readability. For example, to target `<a>` elements, that also have a class of .my-class, write the following:

```
a.my-class {
  color: red;
}
```