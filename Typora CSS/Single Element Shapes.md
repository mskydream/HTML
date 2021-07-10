#  Single Element Shapes

## Trapezoid
A trapezoid can be made by a block element with zero height (height of 0px ), a width greater than zero and a
border, that is transparent except for one side:

![image-20210704105119869](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704105119869.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .trapezoid{
                width: 50px;
                height: 0;
                border-left: 50px solid transparent;
                border-right: 50px solid transparent;
                border-bottom: 100px solid black;
            }
        </style>
    </head>
    <body>
        <div class="trapezoid"></div>
    </body>
</html>
```

## Triangles
To create a CSS triangle deﬁne an element with a width and height of 0 pixels. The triangle shape will be formed
using border properties. For an element with 0 height and width the 4 borders (top, right, bottom, left) each form a
triangle. Here's an element with 0 height/width and 4 diﬀerent colored borders.

## Triangle - Pointing Up

![image-20210704105512560](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704105512560.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .triangle-up{
                width: 0;
                height: 0;
                border-left: 25px solid transparent;
                border-right: 25px solid transparent;
                border-bottom: 50px solid rgb(246, 156, 85);
            }
        </style>
    </head>
    <body>
        <div class="triangle-up"></div>
    </body>
</html>
```

## Triangle - Pointing Down/Left

![image-20210704110031729](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704110031729.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .triangle-down-left{
                width: 0;
                height: 0;
                border-bottom: 50px solid rgb(246, 156, 85);
                border-right: 50px solid transparent;
            }
        </style>
    </head>
    <body>
        <div class="triangle-down-left"></div>
    </body>
</html>
```

## Circles and Ellipses

### Circle

To create a circle, deﬁne an element with an equal width and height (a square) and then set the border-radius
property of this element to 50% .

![image-20210704110351285](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704110351285.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .circle{
                width: 50px;
                height: 50px;
                background: rgb(246, 156, 85);
                border-radius: 50%;
            }
        </style>
    </head>
    <body>
        <div class="circle"></div>
    </body>
</html>
```

### Ellipse
An ellipse is similar to a circle, but with diﬀerent values for width and height .

![image-20210704110538201](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704110538201.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .oval{
                width: 50px;
                height: 80px;
                background: rgb(246, 156, 85);
                border-radius: 50%;
            }
        </style>
    </head>
    <body>
        <div class="oval"></div>
    </body>
</html>
```

## Bursts
A burst is similar to a star but with the points extending less distance from the body. Think of a burst shape as a
square with additional, slightly rotated, squares layered on top.
The additional squares are created using the ::before and ::after psuedo-elements.

## 8 Point Burst

An 8 point burst are 2 layered squares. The bottom square is the element itself, the additional square is created
using the :before pseudo-element. The bottom is rotated 20°, the top square is rotated 135°.

![image-20210704111002378](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704111002378.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .burst-8{
                background: rgb(246, 156, 85);
                width: 40px;
                height: 40px;
                position: relative;
                text-align: center;
                -ms-transform: rotate(20deg);
            }
            .burst-8::before{
                content:"";
                position: absolute;
                top: 0;
                left: 0;
                height: 40px;
                width: 40px;
                background: rgb(246,156,85);
                -ms-transform: rotate(135deg);
                transform: rotate(135deg);
            }
        </style>
    </head>
    <body>
        <div class="burst-8"></div>
    </body>
</html>
```

### 12 Point Burst
An 12 point burst are 3 layered squares. The bottom square is the element itself, the additional squares are created
using the :before and :after pseudo-elements. The bottom is rotated 0°, the next square is rotated 30°, and the
top is rotated 60°.

![image-20210704111301455](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704111301455.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .burst-12{
                background: rgb(246, 156, 85);
                width: 40px;
                height: 40px;
                position: relative;
                text-align: center;
            }
            .burst-12::before, .burst-12::after{
                content:"";
                position: absolute;
                top: 0;
                left: 0;
                height: 40px;
                width: 40px;
                background: rgb(246,156,85);
            }
            .burst-12::before{
                -ms-transform: rotate(30deg);
                transform: rotate(30deg);
            }
            .burst-12::after{
                -ms-transform: rotate(60deg);
                transform: rotate(60deg);
            }
        </style>
    </head>
    <body>
        <div class="burst-12"></div>
    </body>
</html>
```

## Square
To create a square, deﬁne an element with both a width and height. In the example below, we have an element
with a width and height of 100 pixels each.

![image-20210704111455646](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704111455646.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .square{
                width: 100px;
                height: 100px;
                background: rgb(246,156,85);
            }
        </style>
    </head>
    <body>
        <div class="square"></div>
    </body>
</html>
```

## Cube
This example shows how to create a cube using 2D transformation methods skewX() and skewY() on pseudo
elements.

![image-20210704112022644](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704112022644.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .cube{
                background: #dc2e2e;
                width: 100px;
                height: 100px;
                position: relative;
                margin: 50px;
            }
            .cube::before{
                content:'';
                display: inline-block;
                background: #f15757;
                width: 100px;
                height: 20px;
                transform: skewX(-40deg);
                position: absolute;
                top: -20px;
                left: 8px;
            }
            .cube::after{
                content: '';display: inline-block;
                background: #9e1515;
                width: 16px;
                height: 100px;
                transform: skewY(-50deg);
                position: absolute;
                top: -10px;
                left:100%;
            }
        </style>
    </head>
    <body>
        <div class="cube"></div>
    </body>
</html>
```

## Pyramid
This example shows how to create a pyramid using borders and 2D transformation methods skewY() and
rotate() on pseudo elements.

![image-20210704112544473](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704112544473.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .pyramid{
                width: 100px;
                height: 200px;
                position: relative;
                margin: 50px;
            }
            .pyramid::before, .pyramid::after{
                content: '';
                display: inline-block;
                width: 0;
                height: 0;
                border: 50px solid;
                position: absolute;
            }
            .pyramid::before{
                border-color: transparent transparent #ff5656 transparent;
                transform: scaleY(2) skewY(-40deg) rotate(45deg);
            }
            .pyramid::after{
                border-color: transparent transparent #d64444 transparent;
                transform: scaleY(2) skewY(40deg) rotate(-45deg);
            }
        </style>
    </head>
    <body>
        <div class="pyramid"></div>
    </body>
</html>
```

