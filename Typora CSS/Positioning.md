# Positioning

## Overlapping Elements with z-index
To change the default stack order positioned elements ( position property set to relative , absolute or fixed ), use
the z-index property.
The higher the z-index, the higher up in the stacking context (on the z-axis) it is placed.
**Example**
In the example below, a z-index value of 3 puts green on top, a z-index of 2 puts red just under it, and a z-index of 1
puts blue under that.

![image-20210703125856534](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703125856534.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                position:absolute;
                height: 200px;
                width: 200px;
            }
            div#div1{
                z-index:1;
                left:0px;
                top:0px;
                background-color: blue;
            }
            div#div2{
                z-index: 3;
                left: 100px;
                top: 100px;
                background-color:green;
            }
            div#div3{
                z-index: 2;
                left:50px;
                top: 150px;
                background-color:red;
            }
        </style>
    </head>
    <body>
        <div id="div1"></div>
        <div id="div2"></div>
        <div id="div3"></div>
    </body>
</html>
```

## Fixed position

Deﬁning position as ﬁxed we can remove an element from the document ﬂow and set its position relatively to the
browser window. One obvious use is when we want something to be visible when we scroll to the bottom of a long
page.

```css
#stickyDiv{
	position:fixed;
	top:10px;
	left:10px;
}
```

## Relative Position

Relative positioning moves the element in relation to where it would have been in normal ﬂow .Oﬀset properties:

top

left

right

bottom

are used to indicate how far to move the element from where it would have been in normal ﬂow.

```css
.repos{
	position:relative;
	top: 20px;
	left: 30;
}
```

This code will move the box containing element with attribute class="relpos" 20px down and 30px to the right from
where it would have been in normal ﬂow.

## Static positioning

```css
.element{
	position:static;
}
```

This keyword lets the element use the normal behavior, that is it is laid out in its current position in the
ﬂow. The top, right, bottom, left and z-index properties do not apply.