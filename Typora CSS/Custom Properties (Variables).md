## Custom Properties (Variables)

CSS Variables allow authors to create reusable values which can be used throughout a CSS document.
For example, it's common in CSS to reuse a single color throughout a document. Prior to CSS Variables this would
mean reusing the same color value many times throughout a document. With CSS Variables the color value can be
assigned to a variable and referenced in multiple places. This makes changing values easier and is more semantic
than using traditional CSS values.

## Variable Color

```css
:root{
	--red: #b00;
	--blue: #4679bd;
	--grey: #ddd;
}
.Bx1{
	color: var(--red);
	background: var(--grey);
	border: 1px solid var(--red);
}
```

## Variable Dimensions

```css
:root{
	--W200: 200px;
	--W10: 10px;
}
.Bx2{
	width: var(--W200);
	height: var(--W200);
	margin: var(--W10);
}
```

## Variable Cascading
CSS variables cascade in much the same way as other properties, and can be restated safely.
You can deﬁne variables multiple times and only the deﬁnition with the highest speciﬁcity will apply to the element
selected.

![image-20210704101756899](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704101756899.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .button{
                --color: green;
                padding: .5rem;
                border: 1px solid var(--color);
                color: var(--color);
            }
            .button:hover{
                --color: blue;
            }
            .button_red{
                --color: red;
            }
        </style>
    </head>
    <body>
        <a class="button">Button Green</a>
        <a class="button button_red">Button Red</a>
        <a class="button">Button Hovered On</a>
    </body>
</html>
```

## Valid/Invalids
Naming When naming CSS variables, it contains only letters and dashes just like other CSS properties (eg: line-
height, -moz-box-sizing) but it should start with double dashes (--)

```css
//These are Invalids variable names
--123color: blue;
--#color: red;
--bg_color: yellow
--width: 100px;
// Varial variable name
--color: red;
--bg-color: yellow
--width: 100px;
```

**Careful when using Units**

```css
--width: 10;
width: var(--width)px;
--width: 10px;
width: var(--width);

--width: 10;
width: calc(1px * var(--width));
width: calc(1em * var(--width));
```

## With media queries
You can re-set variables within media queries and have those new values cascade wherever they are used,
something that isn't possible with pre-processor variables.
Here, a media query changes the variables used to set up a very simple grid:

![image-20210704103819688](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704103819688.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            :root{
            --width: 25%;
            --content: 'This is desktop';
            }
            @media only screen and (max-width: 767px){
            :root{
            --width:50%;
            --content: 'This is mobile';
            }
            }
            @media only screen and (max-width: 480px){
            :root{
            --width:100%;
            }
            }
            div{
            width: calc(var(--width) - 20px);
            height: 100px;
            }
            div:before{
            content: var(--content);
            }
        </style>
    </head>
    <body>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </body>
</html>
```

