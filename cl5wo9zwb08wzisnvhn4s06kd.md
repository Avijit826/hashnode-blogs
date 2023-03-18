---
title: "A Quick Note Of CSS Selector"
datePublished: Fri Jul 22 2022 16:24:11 GMT+0000 (Coordinated Universal Time)
cuid: cl5wo9zwb08wzisnvhn4s06kd
slug: a-quick-note-of-css-selector-with-simple-examples
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1658517592697/P0VQs6hZA.jpg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1658507010856/wu0F0foaL.png
tags: css-selectors, css, html, html5, iwritecode

---

# CSS selectors

**CSS selectors** define the elements to which you want to apply specific CSS rules.


### Universal selectors

The CSS **universal selector** (`*`) selects all elements in the document.

#### Syntax
```css
* { style properties }
```

#### Example

##### css
```css
* {
        background-color: #03203C;
        color: #fff;
}
```
##### html
```html
 <p>We all know paragraph</p>
    <ul>
      <li>item1</li>
      <li>item2</li>
      <li>item3</li>
      <li>item4</li>
      <li>item5</li>
    </ul>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658485715547/MhuLkRJIe.png align="left")



### Type selectors

The CSS **type selector** selects all elements of the given `type` within a document.

#### Syntax
```css
element { style properties }
```

#### Example

##### css
```css
p {
        color: #2827cc;
}
ul {
        background-color: #ff6263;
}
``` 
##### html
```html
 <p>We all know paragraph</p>
    <ul>
      <li>item1</li>
      <li>item2</li>
      <li>item3</li>
      <li>item4</li>
      <li>item5</li>
    </ul>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658486679291/bgO0XTm1w.png align="left")

### Class selectors

The CSS **class selector** matches elements based on the contents of their `class` attribute.

#### Syntax
```css
.class_name { style properties }
```

#### Example

##### css
```css
.bg-blue {
        background-color: #2827cc;
        color: #fff;
}
```
##### html
```html
 <p class="bg-blue">We all know paragraph</p>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658487831607/-Gz29cWsS.png align="left")

### ID selectors

The CSS **id selector** matches elements based on the values of their `id` attribute.

#### Syntax
```css
#id_value { style properties }
```

#### Example

##### css
```css
#unique_text {
        color: #3dbe29;
        background-color: #000;
}
```
##### html
```html
<ul>
      <li>item1</li>
      <li>item2</li>
      <li id="unique_text">item3</li>
      <li>item4</li>
      <li>item5</li>
    </ul>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658488449497/MK2naJYtm.png align="left")

### Combined selectors

The **combined selector** (`,`) selects all the macing elements in groups.

#### Syntax
```css
element,element { style properties }
```

#### Example

##### css
```css
p,li {
        background-color: #6ee4da;
      }
```
##### html
```html
<p> It's awesome</p>
      <ul>
        <li>highlight me</li>
        <li>highlight me</li>
      </ul>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658491155075/yXhRCDUS1.png align="left")

### Combinator selectors

- **Descendant combinator**

The **Descendant combinator** " " (space) selects nodes that are descendants of the parent element

#### Syntax
```css
selector1 selector2 {
  /* property declarations */
}
```

#### Example

##### css
```css
ul li {
        background-color: #e83a59;
        color: white;
      }
```
##### html
```html
<li>awesome</li>
      <ul>
        <li>highlight me</li>
        <li>highlight me</li>
      </ul>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658492040028/Lvc2mNV9J.png align="left")

- **Direct child combinator**

The **Direct child combinator** "`>` " selects only those elements matched by the second elemnts that are the direct children of elements matched by the parent.

#### Syntax
```css
selector1 > selector2 { style properties }
```

#### Example

##### css
```css
div > li {
        background-color: #3dbe29;
        color: white;
      }
```
##### html
```html
<div>
      <p>It's awesome</p>
      <li>awesome</li>
      <ul>
        <li>highlight me</li>
        <li>highlight me</li>
      </ul>
    </div>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658492577030/DijFSoiVwN.png align="left")


- **Sibling combinator**


**1. Next sibling**


The **next sibling combinator** (`+`) separates two selectors and matches the second element *if it immediately follows the first element, and both are sibling*.

It **only selects** immediate next child of same parent.

#### Syntax
```css
former_element + target_element { style properties }
```

#### Example

##### css
```css
.sibling + p {
        font-weight: 900;
        color: #e07c24;
      }
```
##### html
```html
      <p>Test 1</p>
      <p class="sibling">Test 2</p>
      <p>Test 3</p>
      <p>Test 4</p>
      <p>Test 5</p>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658493407960/4QMO4P22-.png align="left")

**1. Subsequent sibling**


The **subsequent sibling combinator** (`~`) separates two selectors and matches all the sibling elements of same parent after the first

It **selects** all next same childs of same parent of selected element.

#### Syntax
```css
former_element ~ target_element { style properties }
```

#### Example

##### css
```css
.sibling ~ p {
        font-weight: 900;
        background-color: #5a20cb;
        color: #fff;
}
```
##### html
```html
      <p>Test 1</p>
      <p class="sibling">Test 2</p>
      <p>Test 3</p>
      <p>Test 4</p>
      <p>Test 5</p>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658502470162/zR6u9UiWo.png align="left")

### Pseudo selectors


- Pseudo class


A **pseudo-class**  (`:`) is a keyword added to a selector that specifies a special state of the selected elements.

#### For Example

##### css
```css
li:hover {
        background-color: aqua;
      }
```
##### html
```html
 <ul>
      <li >item1</li>
      <li>item2</li>
      <li>item3</li>
      <li>item4</li>
      <li>item5</li>
    </ul>
```
##### Result


![chrome-capture-2022-6-22 (1).gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1658504427973/mTdPgCTWk.gif align="left")
With `:hover` when we hover our mouse over element it applies the properties.

- Pseudo elements


A **pseudo-elements**  (`: :`) is a keyword added to a selector that lets us style a specific part of the selected elements.

#### For Example

##### css
```css
li::before {
        content: "This is ";
        color: #235583;
      }
```
##### html
```html
 <ul>
      <li >item1</li>
      <li>item2</li>
      <li>item3</li>
      <li>item4</li>
      <li>item5</li>
    </ul>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658504814563/aYyJlx2ee.png align="left")
Here using `::before` we add some common text before `<li>` elements without touching HTML.

### Attribute selectors

The CSS **attribute selector** matches elements based on the presence or value of a given attribute.


#### Example

##### css
```css
button[type="reset"] {
        background-color: #8a2be2;
        color: #fff;
      }
```
##### html
```html
<button type="reset">Reset</button><br /><br />
<button type="submit">Submit</button>
```
##### Result

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658505914031/U1GI1Z26j.png align="left")
