---
title: "CSS Box Model"
datePublished: Mon Mar 20 2023 09:26:17 GMT+0000 (Coordinated Universal Time)
cuid: clfgmgui8000a09l8cgq2djbv
slug: css-box-model
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679304250566/fe6d9e68-2f02-4815-ba74-a1ca283411ac.png
tags: css3, css, html5, iwritecode, css-box-model

---

# CSS Box Model

The CSS box model refers to how HTML elements are modelled in browser engines and how the dimensions of those HTML elements are derived from CSS properties.

Every HTML element consists CSS Box Model. And every CSS Box Model contains a content area, padding area, border area and a margin area.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679221482800/8c7401bc-35a1-4432-932f-4caf0f6bbe85.png align="center")

## Content area

The content edge surrounds the rectangle given by the width and height of the box, which often depend on the element's rendered content.

It is defined by the `width` and `height` properties.

* ### width property
    

The width CSS property sets an element's width.

The `min-width` and `max-width` properties override width.

* ### height property
    

The height CSS property specifies the height of an element.

<iframe height="400" style="width:100%" src="https://codepen.io/avijit-das/embed/bGxxqrx?default-tab=css%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/avijit-das/pen/bGxxqrx">
  Untitled</a> by Avijit Das (<a href="https://codepen.io/avijit-das">@avijit-das</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Padding area

The padding area, bounded by the padding edge, extends the content area to extend the element's padding.

* ### padding property
    

The padding CSS shorthand property sets the padding area on all four sides of an element at once.

The thickness of the padding is also individually determined by the `padding-top`, `padding-right`, `padding-bottom`, `padding-left` properties.

<iframe height="400" style="width:100%" src="https://codepen.io/avijit-das/embed/JjaaWvb?default-tab=css%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/avijit-das/pen/JjaaWvb">
  Untitled</a> by Avijit Das (<a href="https://codepen.io/avijit-das">@avijit-das</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Border area

The border area, bounded by the border edge, extends the padding area to include the element's borders.

* ### border property
    

The border shorthand CSS property sets an element's border. It sets the values of `border-width`, `border-style`, and `border-color`.

<iframe height="400" style="width:100%" src="https://codepen.io/avijit-das/embed/yLxxMxB?default-tab=css%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/avijit-das/pen/yLxxMxB">
  Untitled</a> by Avijit Das (<a href="https://codepen.io/avijit-das">@avijit-das</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Margin area

The margin area, bounded by the margin edge, extends the border area to include an empty area used to separate the element from its neighbours. Its dimensions are the margin-box width and the margin-box height.

* ### margin property
    

The margin CSS shorthand property sets the margin area on all four sides of an element.

The size of the margin area is also individualy determined by the `margin-top`, `margin-right`, `margin-bottom`, `margin-left` properties.

<iframe height="400" style="width:100%" src="https://codepen.io/avijit-das/embed/gOddmdK?default-tab=css%2Cresult&editable=true">
  See the Pen <a href="https://codepen.io/avijit-das/pen/gOddmdK">
  Untitled</a> by Avijit Das (<a href="https://codepen.io/avijit-das">@avijit-das</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>