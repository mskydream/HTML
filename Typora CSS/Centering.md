# Centering

## Using Flexbox

![image-20210701164452893](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701164452893.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            html,body, .container{
                height: 100%;
            }
            .container{
                display: flex;
                justify-content: center;
            }
            img{
                align-self: center;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <img src="http://lorempixel.com/400/200">
        </div>
    </body>
</html>
```

OR

![image-20210701164652778](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701164652778.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            html,body{
                height: 100%;
            }
            body{
                display: flex;
                justify-content: center;
                align-items:center;
            }
        </style>
    </head>
    <body>
        <img src="http://lorempixel.com/400/200">
    </body>
</html>
```

## Using margin: 0 auto;

Objects can be centered by using margin: 0 auto; if they are block elements and have a deﬁned width.

![image-20210701165442027](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701165442027.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .containerDiv{
                width: 100%;
                height: 100px;
                padding-bottom: 40px;
            }
            #centeredDiv{
                margin: 0 auto;
                width: 200px;
                height: 100px;
                border: 1px solid #000;
            }
            #centeredParagraph{
                width: 200px;
                margin: 0 auto;
            }
            #centeredImage{
                display: block;
                width: 200px;
                margin: 0 auto;
            }
        </style>
    </head>
    <body>
        <div class="containerDiv">
            <div id="centeredDiv"></div>
        </div>

        <div class="containerDiv">
            <p id="centeredParagraph">This is a centered paragraph.</p>
        </div>

        <div class ="containerDiv">
            <img id="centeredImage" src="https://i.kinja-img.com/gawker-media/image/upload/s--c7Q9b4Eh--/c_scale,fl_progressive,q_80,w_800/qqyvc3bkpyl3mfhr8all.jpg">
        </div>
    </body>
</html>
```

## Using text-align

The most common and easiest type of centering is that of lines of text in an element. CSS has the rule text-align:
center for this purpose:

![image-20210701165636662](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701165636662.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            p{
                text-align:center;
            }
        </style>
    </head>
    <body>
        <p>Lorem ipsum</p>
    </body>
</html>
```

## Using position: absolute

Automatic margins, paired with values of zero for the left and right or top and bottom oﬀsets, will center an
absolutely positioned elements within its parent.

![image-20210701170015839](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701170015839.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .parents{
                position:relative;
                height: 500px;
            }
            .center{
                position:absolute;
                margin:auto;
                top:0;
                right:0;
                bottom: 0;
                left: 0;
            }
        </style>
    </head>
    <body>
        <div class="parent">
            <img class="center" src="http://lorempixel.com/400/200/">
        </div>
    </body>
</html>
```

## Using calc()

The calc() function is the part of a new syntax in CSS3 in which you can calculate (mathematically) what size/position
your element occupies by using a variety of values like pixels, percentages, etc. Note: Whenever you use this
function, always take care of the space between two values calc(100% - 80px) .

![image-20210701170338505](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701170338505.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .center{
                position:absolute;
                height: 50px;
                width: 50px;
                background: red;
                top: calc(50% - 50px/2);
                left: calc(50% - 50px/2);
            }
        </style>
    </head>
    <body>
        <div class="center"></div>
    </body>
</html>
```

## Vertical align anything with 3 lines of code

Use these 3 lines to vertical align practically everything. Just make sure the div/image you apply the code to has a
parent with a height.

![image-20210701170905851](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701170905851.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div.vertical{
                position:relative;
                top:50%;
                transform: translateY(-50%);
            }
        </style>
    </head>
    <body>
        <div class="vertical">Vertical aligned text!</div>
    </body>
</html>
```

## Centering in relation to another item

We will see how to center content based on the height of a near element.
Compatibility: IE8+, all other modern browsers.

![image-20210701171736628](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701171736628.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .content *{
                box-sizing: border-box;
            }
            .content .position-container{
                display:table;
            }
            .content .details{
                display: table-cell;
                vertical-align: middle;
                width: 33.333333%;
                padding: 30px;
                font-size: 17px;
                text-align:center;
            }
            .content .thumb{
                width: 100%;
            }
            .content .thumb img{
                width: 100%;
            }
        </style>
    </head>
    <body>
        <div class="content">
            <div class="position-container">
                <div class="thumb">
                    <img src="http://lorempixel.com/400/200/">
                </div>
                <div class="details">
                    <p class="banner-title">text 1</p>
                    <p class="banner-text">content conten content content content content content content</p>
                    <button class="btn">button</button>
                </div>
            </div>
        </div>
    </body>
</html>
```

## Ghost element technique (Michał Czernow's hack)

This technique works even when the container's dimensions are unknown.
Set up a "ghost" element inside the container to be centered that is 100% height, then use vertical-align:
middle on both that and the element to be centered.

![image-20210701172302194](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701172302194.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .block{
                text-align:center;
                white-space: nowrap;
            }
            .block:before{
                content: '';
                display: inline-block;
                height: 100%;
                vertical-align: middle;
                margin-right: -0.25em;
            }
            .centered{
                display: inline-block;
                vertical-align: middle;
                width: 300px;
                white-space: normal;
            }

        </style>
    </head>
    <body>
        <div class="block">
            <div class="centered">Hello</div>
        </div>
    </body>
</html>
```

## Centering vertically and horizontally without worrying about height or width
The following technique allows you to add your content to an HTML element and center it both horizontally and
vertically without worrying about its height or width.

The outer container
                             should have display: table;
The inner container
                             should have display: table-cell;
                             should have vertical-align: middle;
                             should have text-align: center;
The content box
                             should have display: inline-block;
                             should re-adjust the horizontal text-alignment to eg. text-align: left; or text-align: right; , unless you
                             want text to be centered

![image-20210701173056551](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701173056551.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            body{
                margin:0;
            }
            .outer-container{
                position:absolute;
                display: table;
                width: 100%;
                height: 100%;
                background: #CCC;
            }
            .inner-container{
                display: table-cell;
                vertical-align: middle;
                text-align: center;
            }
            .centered-content{
                display: inline-block;
                text-align:left;
                background: #fff;
                padding: 20px;
                border: 1px solid #000;
            }
        </style>
    </head>
    <body>
        <div class="outer-container">
            <div class="inner-continer">
                <div class="centered-content">
                    You can put anything here!
                </div>
            </div>
        </div>
    </body>
</html>
```

## Vertically align an image inside div

![image-20210701173517081](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701173517081.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .wrap{
                height: 50px;
                width: 100px;
                border: 1px solid blue;
                text-align: center;
            }
            .wrap:before{
                content:"";
                display:inline-block;
                height: 100%;
                vertical-align: middle;
                width: 1px;
            }
            img{
                vertical-align: middle;
            }
        </style>
    </head>
    <body>
        <div class="wrap">
            <img src="http://lorempixel.com/400/200/">
        </div>
    </body>
</html>
```

## Centering with ﬁxed size

If the size of your content is ﬁxed, you can use absolute positioning to 50% with margin that reduces half of your
content's width and height:

![image-20210701174037182](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701174037182.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .center{
                position:absolute;
                background: #ccc;
                left: 50%;
                width: 150px;
                margin-left: -75px;
                top:50%;
                height: 200px;
                margin-top: -100px;      
            }
        </style>
    </head>
    <body>
        <div class="center">
            Center vertically and horizontally
        </div>
    </body>
</html>
```

Horizontal centering with only ﬁxed width
You can center the element horizontally even if you don't know the height of the content:

![image-20210701174303398](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701174303398.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .center{
                position:absolute;
                background: #ccc;

                left:50%;
                width: 150px;
                margin-left: -75px;
            }
        </style>
    </head>
    <body>
        <div class="center">
            Center only horizontally
        </div>
    </body>
</html>
```

Vertical centering with ﬁxed height
You can center the element vertically if you know the element's height:

![image-20210701174455980](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701174455980.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .center{
                position:absolute;
                background: #ccc;

                top:50%;
                height: 200px;
                margin-top: -100px;
            }
        </style>
    </head>
    <body>
        <div class="center">
            Center only vertically
        </div>
    </body>
</html>
```

## Vertically align dynamic height elements

Applying css intuitively doesn't produce the desired results because
				vertical-align:middle isn't applicable to block-level elements
				margin-top:auto and margin-bottom:auto used values would compute as zero
				margin-top:-50% percentage-based margin values are calculated relative to the width of containing block
For widest browser support, a workaround with helper elements:

![image-20210701175002723](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701175002723.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .vcenter-container{
                display: table;
                height: 100%;
                position: absolute;
                overflow: hidden;
                width: 100%;
            }
            .vcenter--helper{
                display: table-cell;
                vertical-align: middle;
            }
            .vcenter--content{
                margin: 0 auto;
                width: 200px;
            }
        </style>
    </head>
    <body>
        <div class="vcenter--container">
            <div class="vcenter--helper">
                <div class="vcenter-content">
                    Stuff
                </div>
            </div>
        </div>
    </body>
</html>
```

## Horizontal and Vertical centering using table layout

One could easily center a child element using table display property.

![image-20210701175818214](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701175818214.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .wrapper{
                display: table;
                vertical-align: center;
                width: 200px;
                height: 200px;
                background-color: #9e9e9e;
            }
            .parent{
                display: table-cell;
                vertical-align: middle;
                text-align: center;
            }
            .child{
                display:inline-block;
                vertical-align: middle;
                text-align: center;
                width: 100px;
                height: 100px;
                background-color: teal;
            }
        </style>
    </head>
    <body>
        <div class="wrapper">
            <div class="parent">
                <div class ="child"></div>
            </div>
        </div>
    </body>
</html>
```

