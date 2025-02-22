# Cascading style sheets 

**Cascading Style Sheets (CSS)** is a stylesheet language used to describe the presentation of a document written in HTML or XML.

CSS describes **how elements should be rendered** on screen or on other media. In short, CSS gives the styling to the content.
## Syntax

![2023-05-30 14_03_12-Excalidraw - Brave](https://github.com/shubhsharma19/web-development-notes/assets/69891912/631feb46-e54b-4343-ab26-55b8e5bf2638)

```html
selector {
  property : value;
}
```

> Note: Selector can be anything like an element or an id or a class


## Comments

`/*    comments    */`

## Cascade effect in CSS

What comes above can be overridden by what comes below. This only happens if both have similar specifity value or the below one has higher.

For exp :
```
p{color: red;}
p{color:blue;}
```
Here, blue color will override the red color because both have same specificity value.

## Selection by relationship

**Parent-child**

- `>` is used to target direct children of a parent. 

for exp: `section > p{}` 

> Here `section` is a parent and `p` is a direct child
- ` ` space is used to target any child. 

for exp: `section p{}` 

> Here `section` is a parent and `p` is a child, here child can be any child like grandchild or direct child or great grand child etc.


**Siblings**
- `+` is used to target next sibling. 

for exp: `section > p + p{}`

> Here `section` is the direct parent of both `p`. `p + p` means target the second p which is a direct sibling of first p.

## Selection using ids and classes

**ID** is a unique identifier. One html document can have only one id with a the same name. To target an id we use `#` character. 

For exp: `#logo {}` here logo is an id which is unique.

**Classes** is a way to target multiple elements at the same time. A class can be targetted using `.` dot.

For exp: `.main {}`

## Specificity

Highest specificity to lowest specificity:

1. Inline css in html or !important (1000)
2. Id (100)
3. Classes (10)
4. Tags (1)

## Box Model

![boxmodel](https://github.com/shubhsharma19/web-development-notes/assets/69891912/3ac2c4a3-e217-4669-a893-e2a1d78c0a6f)


Everything is a box on the web.

Box model is concerned with how things take up space on a webpage.

Box model contains following things:

- Margin: Outside the Border
- Border: Outside the padding, between margin and padding.
- Padding: Outside the content, between content and border.
- Content: This is the content.

**Some points to remember about the Box model:**
- Margin pushes away the box.
- Border pushes away padding from the margin.
- Padding pushes away the border from content.

> Note: In box model everything gets added including borders, so we tell browser to include border as well in the box-size by giving the following property to the whole document.

```
* {
  box-sizing: border-box;
}
```

## Floats

It is a way used in CSS to align the content on the webpage.

Allows an element to be positioned horizontally within its parent container. When an element is floated, it is taken out of the normal flow of the document and positioned to the left or right side of its containing element.

> Note: Whenever you float an item it will fight as hard as it can to get to the corner of the screen. If you float it left it will try to get to the top left corner, if you float it right it will try to get to the top right corner.

for exp: `float: left;` or `float: right;`

> Note: when you float something on the screen it literally floats on the screen above the content. This means everything which was under the floated element will slide up till it reaches the top.

## How to align items using floats

1. `float: left` or `float: right;`
2. `clear:both;`

## Colors in CSS

- RGB (x, y, z)
- Hex (#ffffff) 
- RGBA (x, y, z, a) [a is transparency]
- HSLA (0,x,y,z)

## Shorthands used in box-model

`margin: top, right, bottom, left` 

which is clockwise direction can be shortened to: `margin: top-bottom, left-right;`

To center stuff: `margin: 0 auto` or `margin: auto auto;`
