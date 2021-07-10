# Margins

## Margin Collapsing

When two margins are touching each other vertically, they are collapsed. When two margins touch horizontally,
they do not collapse.

**Example of adjacent vertical margins:**

Consider the following styles and markup:

![image-20210702091853488](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702091853488.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                margin:10px;
            }
        </style>
    </head>
    <body>
        <div>
            some content
        </div>
        <div>
            some more content
        </div>
    </body>
</html>
```

They will be 10px apart since vertical margins collapse over one and other. (The spacing will not be the sum of two
margins.)

**Example of adjacent horizontal margins:**

Consider the following styles and markup:

![image-20210702092119523](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702092119523.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            span{
                margin: 10px;
            }
        </style>
    </head>
    <body>
        <span>some</span><span>content</span>
    </body>
</html>
```

They will be 20px apart since horizontal margins don't collapse over one and other. (The spacing will be the sum of
two margins.)

**Overlapping with diﬀerent sizes**

![image-20210702093237753](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702093237753.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .top{
                margin:10px;
            }
            .bottom{
                margin: 15px;
            }
        </style>
    </head>
    <body>
        <div class="top">
            some content
        </div>
        <div class="bottom">
            some more content
        </div>
    </body>
</html>
```

These elements will be spaced 15px apart vertically. The margins overlap as much as they can, but the larger
margin will determine the spacing between the elements.

**Overlapping margin gotcha**

![image-20210702093925567](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702093925567.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .outer-top{
                margin:10px;
            }
            .inner-top{
                margin:15px;
            }
            .outer-bottom{
                margin:20px;
            }
            .inner-bottom{
                margin:25px;
            }
        </style>
    </head>
    <body>
        <div class="outer-top">
            <div class="inner-top">
                some content
            </div>
        </div>
        <div class="outer-bottom">
            <div class="inner-bottom">
                some more content
            </div>
        </div>
    </body>
</html>
```

**Collapsing Margins Between Parent and Child Elements:**

![image-20210702094352617](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702094352617.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            h1{
                margin:0;
                background: #cff;
            }
            div{
                margin: 50px 0 0 0;
                background: #cfc;
            }
            p{
                margin: 25px 0 0 0;
                background: #cf9;
            }
        </style>
    </head>
    <body>
        <h1>Title</h1>
        <div>
            <p>Paragraph</p>
        </div>
    </body>
</html>
```

## Apply Margin on a Given Side

![image-20210702094739449](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702094739449.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            #myDiv{
                margin-left:30px;
                height:40px;
                width:40px;
                background-color:red;
            }
        </style>
    </head>
    <body>
        <div id="myDiv"></div>
    </body>
</html>
```

**margin: <top> <right> <bottom> <left>;**

![image-20210702104002092](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702104002092.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            #myDiv{
                margin: 0 10px 50px 100px;
                height: 40px;
                width: 40px;
                background-color:red;
            }
        </style>
    </head>
    <body>
        <div id="myDiv"></div>
    </body>
</html>
```

## Horizontally center elements on a page using margin

As long as the element is a block, and it has an explicitly set width value, margins can be used to center block
elements on a page horizontally.

We add a width value that is lower than the width of the window and the auto property of margin then distributes
the remaining space to the left and the right:

```css
#myDiv{
	width:80%;
	margin:0 auto;
}
```

In the example above we use the shorthand margin declaration to ﬁrst set 0 to the top and bottom margin values
(although this could be any value) and then we use auto to let the browser allocate the space automatically to the
left and right margin values.
In the example above, the #myDiv element is set to 80% width which leaves use 20% leftover. The browser
distributes this value to the remaining sides so:
(100% - 80%) / 2 = 10%

## Example 1:

It is obvious to assume that the percentage value of margin to margin-left and margin-right would be relative to
its parent element.

```css
.parents{
	width: 500px;
	height: 300px;
}
.child{
	width: 100px;
	height:100px;
	margin-left: 10%;
}
```

But that is not the case, when comes to margin-top and margin-bottom . Both these properties, in percentages,
aren't relative to the height of the parent container but to the width of the parent container.
So,

```css
.parent{
	width: 500px;
	height:300px;
}
.child{
	width: 100px;
	height:100px;
	margin-left: 10%;
	margin-top: 20%;
}
```

## Negative margins

Margin is one of a few CSS properties that can be set to negative values. This property can be used to **overlap
elements without absolute positioning.**

![image-20210702104803391](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702104803391.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                display: inline;
            }
            #over{
                margin-left: -20px;
            }
        </style>
    </head>
    <body>
        <div>Base div</div>
        <div id="over">Overlapping div</div>
    </body>
</html>
```

