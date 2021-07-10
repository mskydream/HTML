# Outlines

## outline-style

The outline-style property is used to set the style of the outline of an element.

![image-20210702113121818](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702113121818.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            p{
                border: 1px solid black;
                outline-color:blue;
                line-height: 30px;
            }
            .p1{
                outline-style: dotted;
            }
            .p2{
                outline-style: dashed;
            }
            .p3{
                outline-style: solid;
            }
            .p4{
                outline-style: double;
            }
            .p5{
                outline-style: groove;
            }
            .p6{
                outline-style: ridge;
            }
            .p7{
                outline-style: inset;
            }
            .p8{
                outline-style: outset;
            }
        </style>
    </head>
    <body>
        <p class="p1">A dotted outline</p>
        <p class="p2">A dashed outline</p>
        <p class="p3">A solid outline</p>
        <p class="p4">A double outline</p>
        <p class="p5">A groove outline</p>
        <p class="p6">A ridge outline</p>
        <p class="p7">An inset outline</p>
        <p class="p8">An outset outline</p>
    </body>
</html>
```

