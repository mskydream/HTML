# Overﬂow

## overﬂow-wrap

overflow-wrap tells a browser that it can break a line of text inside a targeted element onto multiple lines in an
otherwise unbreakable place. Helpful in preventing an long string of text causing layout problems due to
overﬂowing it's container.

![image-20210702114005658](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702114005658.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                width: 100px;
                outline: 1px dashed #bbb;
            }
            #div1{
                overflow-wrap: normal;
            }
            #div2{
                overflow-wrap: break-word;
            }
        </style>
    </head>
    <body>
        <div id="div1">
            <strong>#div1</strong>: Small words are displayed normally, bu a long word like <span stylle="red;">
            supercalifragilisticexpiallidocious</span> is too long so it will overflow past the the edge of the line-break
        </div>

        <div id="div2">
            <strong>#div2</strong>: Small words are displayed normally, but a long word like <span style="red;">
            supercalifragilisticexpiallidocious</span> will be split at the line break and continue on the next line.
        </div>
    </body>
</html>
```

## overﬂow-x and overﬂow-y

These two properties work in a similar fashion as the overflow property and accept the same values. The
overflow-x parameter works only on the x or left-to-right axis. The overflow-y works on the y or top-to-bottom
axis.

![image-20210702114543813](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702114543813.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                width: 200px;
                height: 200px;
            }
            #div-x{
                overflow-x: hidden;
            }
            #div-y{
                overflow-y:hidden;
            }
        </style>
    </head>
    <body>
        <div id="div-x">
            If this div is too small to display its contents,
            the content to the left and right will be clipped.
        </div>

        <div id="div-y">
            If this div is too small to display its contents,
            the content to the top and bottom will be clipped.
        </div>
    </body>
</html>
```

## overﬂow: scroll

![image-20210702114832161](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702114832161.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                width: 100px;
                height: 100px;
                overflow: scroll;
            }
        </style>
    </head>
    <body>
        <div>
            This div is too small to display its content to display the effects of the overflow property.
        </div>
    </body>
</html>
```

## overﬂow: visible

Content is not clipped and will be rendered outside the content box if it exceeds its container size.

![image-20210702115052566](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702115052566.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                width: 50px;
                height: 50px;
                overflow: visible;
            }
        </style>
    </head>
    <body>
        <div>
            Even is this div is too small to display its contents, the content is not clipped.
        </div>
    </body>
</html>
```

## Block Formatting Context Created with Overﬂow

Using the overflow property with a value diﬀerent to visible will create a new block formatting context. This is
useful for aligning a block element next to a ﬂoated element.

![image-20210702115512539](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702115512539.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            img{
                float:left;
                margin-right: 10px;
            }
            div{
                overflow:hidden;
            }
        </style>
    </head>
    <body>
        <img src="http://placehold.it/100x100">
        <div>
            <p>Lorem ipsum dolor sit amet, cum no paulo mollis pertinacia.</p>
            <p>Ad case omnis nam, mutat deseruisse persequeris eos ad, in tollid debitis sea.</p>
        </div>
    </body>
</html>
```

