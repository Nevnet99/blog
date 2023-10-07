---
title: 'Flexbox and CSS Grid Cheat Sheet'
description: 'A cheat sheet for Flexbox and CSS Grid'
pubDate: 'Sep 29 2023'
heroImage: '/codecult-placeholder.png'
---

Let's get started with the basics of Flexbox and CSS Grid. 

## Flexbox 

Flexbox is a one-dimensional layout system that allows you to align and distribute space among items in a container. It's great for laying out items in a single row or column.


### Flexbox Properties

- `display: flex;` - This is the main property that enables flexbox. This should be applied to the parent element of the children you want to affect with flexbox.
```css
.parent {
  display: flex;
}

.child {
  /* This child will be affected by flexbox */
}

```
- `flex-direction: row | row-reverse | column | column-reverse;` - This property determines the direction of the flexbox layout (and is also applied to the parent). The default is `row`, there is a jsfiddle showing the different options: <a href="https://jsfiddle.net/vdwbezkf/27/" target="_blank">here</a>
```css

```css
.parent {
  display: flex;
  flex-direction: column;
}

.child {
  /* This child will be affected by flexbox */
}

```

- `flex-wrap: nowrap | wrap | wrap-reverse;` - This property determines whether the flexbox layout should wrap or not. The default is `nowrap` (also applied to parent), there is a jsfiddle showing the different options: <a href="https://jsfiddle.net/aqLnbcvk/13/" target="_blank">here</a>

```css
.parent {
  display: flex;
  flex-wrap: wrap;
}

.child {
  /* This child will be affected by flexbox */
}
```

- `justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;` - This property determines how the flexbox layout should be justified. The default is `flex-start`, there is a jsfiddle showing the different options: <a href="https://jsfiddle.net/2L3x1q5a/1/" target="_blank">here</a>

```css
.parent {
  display: flex;
  justify-content: center;
}

.child {
  /* This child will be affected by flexbox */
}
```


- `align-items: stretch | flex-start | flex-end | center | baseline;` - This property determines how the flexbox layout should be aligned. The default is `stretch`, there is a jsfiddle showing the different options: <a href="https://jsfiddle.net/2L3x1q5a/1/" target="_blank">here</a>

```css
.parent {
  display: flex;
  align-items: center;
}

.child {
  /* This child will be affected by flexbox */
}
```


- `align-content: stretch | flex-start | flex-end | center | space-between | space-around;` - This property determines how the flexbox layout should be aligned. The default is `stretch`, there is a jsfiddle showing the different options: <a href="https://jsfiddle.net/2L3x1q5a/1/" target="_blank">here</a>

```css
.parent {
  display: flex;
  align-content: center;
}

.child {
  /* This child will be affected by flexbox */
}
```







## CSS Grid 

CSS Grid is a two-dimensional layout system that allows you to align and distribute space among items in a container. It's great for laying out items in a grid.

### CSS Grid Properties

## When to use Flex vs CSS Grid

The key is that Flexbox is for one-dimensional layouts, and CSS Grid is for two-dimensional layouts, to expand on that: 
- Flexbox is for laying out items in a single row or column.
- CSS Grid is for laying out items in a grid so both rows and columns.

in short CSS Grid should be used for layouts and Flexbox should be used for alignment.

Some examples of when to use Flexbox:
- Aligning items
- Simple 1 Row Navigation bars
- Simple 1 Column layouts

Some examples of when to use CSS Grid:
- Complex layouts
- Composition of entire pages (header, footer, main content, etc.)


