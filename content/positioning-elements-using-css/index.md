---
title: "Positioning elements using CSS"
description: "Positioning elements with CSS can be quite tricky. Things can get quickly complicated as your project gets bigger.There are different…"
date: "2020-01-31T05:02:56.872Z"
categories: []
published: true
canonical_link: https://medium.com/@rishabhcodes/positioning-elements-using-css-5bab2bfbbc64
redirect_from:
  - /positioning-elements-using-css-5bab2bfbbc64
---

Positioning elements with CSS can be quite tricky. Things can get quickly complicated as your project gets bigger.There are different ways/methods for positioning elements with pure CSS. Using CSS **float, display** and **position** properties are the most common methods.

In this article, we shall talk about one of the most complicated properties of CSS, the **position property.**

### CSS Position Properties

So there are 4 main values of the Position Property:

**Static, relative, absolute** and **fixed**. Each property has it’s own use. There are additional properties for setting the coordinates of an element, also known as box-offset properties. These box-offset properties are Top, right, bottom, left and the z-index.

Offset properties don’t work without a declared position or with an element whose position is static.

Let’s take a look at the position properties in CSS:

### 1\. Static

Static is the default value. Whether we declare the position for an element or not, elements are positioned in a normal order on the webpage. If an element’s position is static in a webpage it doesn’t accept any box-offset property. Defining position: static or not doesn't make any difference. The boxes are positioned according to the normal document flow.

### 2\. Relative

If an element’s position is relative then it’s new position will be relative to its normal position.

Starting with position:relative and for all non-static position values, we are able to change an element’s default position by using the offset properties.

Relatively positioned elements always remain in the normal flow of the page. Unlike floated elements relatively positioned elements do not vacate their original position instead their original position is maintained and they float around in z-plane.

A relatively positioned element won’t disturb the other elements, it will always move in its coordinates on the z-plane.

### 3\. Absolute

In position relative the element is positioned relative to itself. However, an absolutely positioned element is relative to its parent. An absolutely positioned element leaves the normal flow of the document and vacate their original position. Any upcoming element can take it’s original position.

An element with position: absolute is removed from the normal document flow. It is positioned automatically to the starting point (top-left corner) of its parent element. If it doesn’t have any parent elements, then the HTML document will be its parent.

Since position: absolute removes the element from the document flow, other elements are affected and behave as the element is removed completely from the webpage.

### 4\. Fixed

Like position:absolute, fixed positioned elements are also removed from the normal document flow. The display property for the fixed element is also changed. Fixed element also takes reference for it’s new position from the parent or the HTML document like any absolute element. Major difference between an absolute element and a fixed element is that the position of the fixed element is fixed on the web page and scrolling through the web page won’t move a fixed element.

Fixed block-level elements will start taking space according to the content it is wrapping inside. At the same time, an inline-level element may start accepting the box model properties(such as width and height), if we fix the position.

#### Z-index

We have height and width (x, y) as 2 dimensions. Z is the 3rd dimension. An element in the webpage comes in front of other elements as its z-index value increases

**_Z-index_** _doesn’t work with position: static or without a declared position._
