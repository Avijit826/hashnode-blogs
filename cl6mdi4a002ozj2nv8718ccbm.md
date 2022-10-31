# A Quick Cheat sheet on CSS Flexbox

## Basics

**Flexbox** is a modern one-dimensional layout method for arranging items in rows or columns.


### Syntax:
```css
.parent{
  display: flex;
}
```

In the flex layout model, the children of a flex container can be laid out in any direction, and can `flex` their sizes, either growing to fill unused space or shrinking to avoid overflowing the parent.

### Example:

<iframe src="https://codesandbox.io/embed/flexbox-template-oby7kc?fontsize=14&hidenavigation=1&initialpath=%2Fflex1.html&module=%2Fflex1.html&theme=dark&view=preview"
     style="width:100%; height:600px; border:0; border-radius: 4px; overflow:hidden;"
     title="flexbox-template"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

> After applying `flex` to parent

<iframe src="https://codesandbox.io/embed/flexbox-template-oby7kc?fontsize=14&hidenavigation=1&initialpath=%2Fflex2.html&module=%2Fflex2.html&theme=dark&view=preview"
     style="width:100%; height:600px; border:0; border-radius: 4px; overflow:hidden;"
     title="flexbox-template"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

## Terminology

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659969547079/WNLnInB7W.png align="left")

- **main axis**:  The main axis of a flex container is the primary axis along which flex items are laid out.

- **cross axis**: The axis perpendicular to the main axis is called the cross axis.

- **main-start & main-end**: The flex items are placed within the container starting on the main-start side and going toward the main-end side.

- **cross-start & cross-end**: Flex lines are filled with items and placed into the container starting on the cross-start side of the flex container and going toward the cross-end side.

- **main size**: A flex item’s width or height, whichever is in the main dimension, is the item’s main size. 

- **cross size**: The width or height of a flex item, whichever is in the cross dimension, is the item’s cross size.

## Flexbox Properties

### Flex direction

The `flex-direction` property specifies how flex items are placed in the flex container, by setting the direction of the flex container’s `main axis`.

```css
.parent {
  flex-direction: row (default) | row-reverse | column | column-reverse;
}
```

- **row**: The flex container’s `main axis` has the same orientation as the `inline axis` of the current writing mode. The `main-start` and `main-end` directions are equivalent to the `inline-start` and `inline-end` directions.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659972432911/Tc1_uf0Fy.png align="left")

- **row-reverse**: Same as `row`, except the `main-start` and `main-end` directions are swapped.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659972573416/UmkRP66tv.png align="left")

- **column**: The flex container’s `main axis` has the same orientation as the block axis of the current writing mode. The `main-start` and `main-end` directions are equivalent to the `block-start` and `block-end` directions.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659972801523/0WXMHM7mE.png align="left")

-**column-reverse**: Same as column, except the main-start and main-end directions are swapped.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659973055681/0OS7wjkpu.png align="left")


### Flex wrap

Flex wrap defines wrap the elements in side parent or not.

```css
.parent {
  flex-wrap: nowrap (default) | wrap | wrap-reverse;
}
```


- **nowrap**: all flex items will be on one line

<iframe src="https://codesandbox.io/embed/flexbox-template-oby7kc?fontsize=14&hidenavigation=1&initialpath=%2Fflex3.html&module=%2Fflex3.html&theme=dark&view=preview"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="flexbox-template"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

- **wrap**: flex items will wrap onto multiple lines, from top to bottom.

<iframe src="https://codesandbox.io/embed/flexbox-template-oby7kc?fontsize=14&hidenavigation=1&initialpath=%2Fflex4.html&theme=dark&view=preview"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="flexbox-template"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

- **wrap-reverse**: flex items will wrap onto multiple lines from bottom to top.

<iframe src="https://codesandbox.io/embed/flexbox-template-oby7kc?fontsize=14&hidenavigation=1&initialpath=flex5.html&theme=dark&view=preview"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="flexbox-template"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

### justify-content

The `justify-content` property aligns flex items along the `main axis` of the current line of the flex container.

```css
.parent {
  justify-content: flex-start (default) | flex-end | center | space-between | space-around | space-evenly;
}
```

- **flex-start**: items are packed toward the start of the flex-direction.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660019662164/ZRhCYhcDR.png align="left")

- **flex-end**: items are packed toward the end of the flex-direction.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660019701149/qaXWFFqCI.png align="left")

- **center**: items are centered along the line.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660019731618/rV625aF-L.png align="left")

- **space-between**: items are evenly distributed in the line; first item is on the start line, last item on the end line.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660019771983/luPVqu3Mm.png align="left")

- **space-around**: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren’t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660019812287/u75i3M8PB.png align="left")

- **space-evenly**: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660019844985/VQ4RsN2vc.png align="left")


### align-items

The `align-items` property aligns flex items along the `cross axis` of the current line of the flex container.

```css
.parent {
  align-items: stretch (default) | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end;
}
```

- **stretch**: Flex items are stretched such that the cross-size of the item's margin box is the same as the line while respecting width and height constraints.

- **start | flex-start**: The cross-start margin edges of the flex items are flushed with the cross-start edge of the line.

- **baseline | first baseline**Items are aligned on the start of baseline.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660023297487/X_Un8Dv8j.png align="left")

- **end | flex-end**: The cross-end margin edges of the flex items are flushed with the cross-end edge of the line.

- **last baseline**: Items are aligned on the end of baseline.
>Currently only supported on firefox.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660023575272/u7A0FHsU7.png align="left")


- **center**: The flex items' margin boxes are centered within the line on the cross-axis. If the cross-size of an item is larger than the flex container, it will overflow equally in both directions.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660023936549/t4EvgNyz8.png align="left")

### align-content

The `align-content` property sets the distribution of space between and around content items along a flexbox's `cross-axis`.

```css
.parent {
  align-content: flex-start (default) | flex-end | center | space-between | space-around | space-evenly;
}
```
- **flex-start**: The items are packed flush to each other against the edge of the alignment container depending on the flex container's cross-start side.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660024858034/JdPP0UnNL.png align="left")

- **flex-end**: The items are packed flush to each other against the edge of the alignment container depending on the flex container's cross-end side.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660024928715/WDUPsmrTh.png align="left")

- **center**: The items are packed flush to each other in the center of the alignment container along the cross axis.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660024997170/T5s46VSmO.png align="left")

- **space-between**: The items are evenly distributed within the alignment container along the cross axis. The spacing between each pair of adjacent items is the same. 


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660025090497/PXOw457N1.png align="left")

- **space-around**: The items are evenly distributed within the alignment container along the cross axis. The spacing between each pair of adjacent items is the same. The empty space before the first and after the last item equals half of the space between each pair of adjacent items.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660025174025/cnt_8Azox.png align="left")

- **space-evenly**: The items are evenly distributed within the alignment container along the cross axis. The spacing between each pair of adjacent items, the start edge and the first item, and the end edge and the last item, are all exactly the same.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660025253388/T0lBXT3d8.png align="left")

## gap

The gap property explicitly controls the space between flex items.

```css
.parent{
  gap : <'row-gap'> <'column-gap'>;
}
```

#### Example: 
```css
 .parent {
        display: flex;
        gap: 30px;
}
```
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660025892652/PE5J8UWsB.png align="left")


## flex-grow

The flex-grow CSS property sets the flex grow factor of a flex item's main size.

>default value of flex-grow is 0.

#### Example: 
```css
.child:nth-child(2) {
        flex-grow: 1.5;
        background-color: #777;
      }
.child:nth-child(4) {
        flex-grow: 0.7;
        background-color: #777;
      }
.parent {
        display: flex;
        gap: 20px;
}
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660026837907/SGJyYuSJb.png align="left")


## flex-shrink
The `flex-shrink` CSS property sets the flex shrink factor of a flex item. If the size of all flex items is larger than the flex container, items shrink to fit according to `flex-shrink`.

>default value of flex-shrink is 1.

#### Example: 
```css
.child:nth-child(2) {
        flex-shrink: 2;
      }
.child{
        flex-shrink: 1;
        background-color: #777;
      }
.parent {
        display: flex;
        gap: 20px;
}
```
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660031100004/qpyoGweXe.png align="left")

## order

The `order` property sets the order to lay out an item in a flex container. Items in a container are sorted by ascending `order` value and then by their source code order.

>default value of order is 0.

#### Example: 

default layout

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660032096626/kqmoaJ_qI.png align="left")

After adding a higher order value

```css
.child:nth-of-type(2) {
        order: 1;
}
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660032142964/fSY7ZBEet.png align="left")

Similarly, after adding lower order value 
```css
.child:nth-of-type(2) {
        order: -2;
}
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660032259853/CxpPlFLUE.png align="left")

## align-self

The `align-self` CSS property overrides a flex item's `align-items` value.

```css
.parent {
  align-self: auto (default) | flex-start | flex-end | center | baseline | stretch;
}
```
- **auto**: Computes to the parent's align-items value.
- **normal**: For flex items, the keyword behaves as stretch.
- **stretch**: If the combined size of the items along the cross axis is less than the size of the alignment container and the item is auto-sized, its size is increased equally (not proportionally), while still respecting the constraints imposed by max-height/max-width (or equivalent functionality), so that the combined size of all auto-sized items exactly fills the alignment container along the cross axis.

#### Example: 
```css
.child:nth-of-type(2) {
        align-self: stretch;
}
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660056204717/NV8rO6Ljn.png align="left")


- **self-start**: Aligns the items to be flush with the edge of the alignment container corresponding to the item's start side in the cross axis.
- **flex-start**: The cross-start margin edge of the flex item is flushed with the cross-start edge of the line.

- **baseline | first baseline**: Aligns the alignment baseline of the box's first baseline set with the corresponding baseline in the shared first baseline set of all the boxes in its baseline-sharing group. 

#### Example: 
```css
.child:nth-of-type(2) {
        align-self: flex-start;
}
```
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660056597216/_IoYuqR4h.png align="left")


- **center**: The flex item's margin box is centered within the line on the cross-axis. If the cross-size of the item is larger than the flex container, it will overflow equally in both directions.

#### Example: 
```css
.child:nth-of-type(2) {
        align-self: center;
}
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660057143888/7Wvqb2ETQ.png align="left")

- **last baseline**: Aligns the alignment baseline of the box's last baseline set with the corresponding baseline in the shared last baseline set of all the boxes in its baseline-sharing group. 
>Currently only supported on firefox.


- **self-end**: Aligns the items to be flush with the edge of the alignment container corresponding to the item's end side in the cross axis.


- **flex-end**: The cross-end margin edge of the flex item is flushed with the cross-end edge of the line.

#### Example: 
```css
.child:nth-of-type(2) {
        align-self: flex-end;
}
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660056808426/8C-v39BxP.png align="left")
