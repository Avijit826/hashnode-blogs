# A Quick Note Of CSS Position

# CSS Position

The `position` CSS property sets how an element is positioned in a document. It defines the position behavior of the element.

## Types of position

1.    static      
2.   relative    
3.   absolute    
4.   fixed
5.   sticky

### Syntax:

```css
position: static;
position: relative;
position: absolute;
position: fixed;
position: sticky;
``` 

> **Notes**
> * Initial value: *	static
> * Applies to: *	all elements except table-column-group and table-column

### static

The default value `static` is positioned according to the normal flow of the document. The `top`, `right`, `bottom`, `left`, and `z-index` properties have no effect. 

#### Example:

html 

```html
 <div class="static">
      <p>Static parent</p>
      <div class="absolute">
        <p>Absolute child</p>
      </div>
    </div>
``` 
css


```css
     .static {
         height: 300px;
          width: 300px;
          background-color: #0091ff94;
     }
     .absolute {
          position: absolute;
          bottom: 0;
          right: 0;
          padding: 20px 20px;
          background-color: #1b97f5;
     }
``` 

Result


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658512963344/K-B1qsaWr.png align="left")


### relative

The element is positioned according to the normal flow of the document.
> The property relative to itself based on the values of `top`, `right`, `bottom`, and `left`. 
>The offset does not affect the position of any other elements; thus, the space given for the element in the page layout is the same as if position were static.

#### Example:

html 

```html
 <div class="relative">
      <p>relative parent</p>
      <div class="absolute">
        <p>Absolute child</p>
      </div>
``` 
css


```css
     .relative {
        position: relative;
        height: 300px;
        width: 300px;
        background-color: #0091ff94;
      }
      .absolute {
        position: absolute;
        bottom: 0;
        right: 0;
        padding: 20px 20px;
        background-color: #1b97f5;
      }
``` 

Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658513473091/KUr-K-3_J.png align="left")

### absolute

The element is removed from the normal document flow, and no space is created for the element in the page layout. 
>It is positioned relative to its closest positioned ancestor, if any; otherwise, it is placed relative to the initial containing block.
> Its final position is determined by the values of `top`, `right`, `bottom`, and `left`. 

#### Example:

html 

```html
 <div class="relative">
      <p>relative parent</p>
      <div class="inside-absolute">
        <p>Inside Absolute child</p>
      </div>
    </div>
    <div class="outside-absolute">
      <p>Outside Absolute child</p>
    </div>
``` 
css


```css
     .relative {
        position: relative;
        height: 300px;
        width: 300px;
        background-color: #0091ff94;
      }
      .inside-absolute {
        position: absolute;
        bottom: 0;
        right: 0;
        padding: 20px 20px;
        background-color: #1b97f5;
      }
      .outside-absolute {
        position: absolute;
        bottom: 0;
        left: 0;
        padding: 10px 10px;
        background-color: #3d49f8;
      }
``` 

Result


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658513925328/KVilk2kAD.png align="left")


### fixed

The element will not remain in the natural flow of the page. It will position itself according to the viewport.
> The final position itself based on the values of `top`, `right`, `bottom`, and `left`. 

> There are browser inconsistencies with `perspective` and `filter` contributing to containing block formation.

#### Example:

html 

```html
<div class="relative">
      <p>relative parent</p>
      <div class="fixed">
        <p>fixed child</p>
      </div>
    </div>
    <div class="outside-absolute">
      <p>Outside Absolute child</p>
    </div>
``` 
css


```css
.relative {
        position: relative;
        height: 300px;
        width: 300px;
        background-color: #0091ff94;
      }
      .fixed {
        position: fixed;
        top: 0;
        right: 0;
        padding: 20px 20px;
        background-color: #1b97f5;
      }
      .outside-absolute {
        position: absolute;
        bottom: 0;
        left: 0;
        padding: 10px 10px;
        background-color: #3d49f8;
      }
``` 

Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658514574977/CE3537bgB.png align="left")


### sticky

The element is positioned according to the normal flow of the document, and then offset relative to its nearest scrolling ancestor and containing block (nearest block-level ancestor), including table-related elements, based on the values of `top`, `right`, `bottom`, and `left`. 

#### Example:

html 

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/avijit-das/embed/poLwrmZ?default-tab=html" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/avijit-das/pen/poLwrmZ">
  Untitled</a> by Avijit Das (<a href="https://codepen.io/avijit-das">@avijit-das</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


css
<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/avijit-das/embed/poLwrmZ?default-tab=css" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/avijit-das/pen/poLwrmZ">
  Untitled</a> by Avijit Das (<a href="https://codepen.io/avijit-das">@avijit-das</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Result
<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/avijit-das/embed/poLwrmZ?default-tab=" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/avijit-das/pen/poLwrmZ">
  Untitled</a> by Avijit Das (<a href="https://codepen.io/avijit-das">@avijit-das</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>