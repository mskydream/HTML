# box-shadow

## bottom-only drop shadow using a pseudo-element
![image-20210703165337467](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703165337467.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .box_shadow{
                background-color: #1C90F3;
                width: 200px;
                height: 100px;
                margin: 50px;
            }
            .box_shadow:after{
                content: "";
                width: 190px;
                height: 1px;
                margin-top: 98px;
                margin-left: 5px;
                display: block;
                position: absolute;
                z-index: -1;
                -webkit-box-shadow: 0px 0px 8px 2px #444444;
                -moz-box-shadow: 0px 0px 8px 2px #444444;
                box-shadow: 0px 0px 8px 2px #444444;
            }
        </style>
    </head>
    <body>
        <div class="box_shadow"></div>
    </body>
</html>
```

## inner drop shadow

![image-20210703165855225](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703165855225.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .box_shadow{
                background-color: #1C90F3;
                width: 200px;
                height: 100px;
                -webkit-box-shadow: 0px 0px 10px -1px #444444;
                -moz-box-shadow: 0px 0px 10px -1px #444444;
                box-shadow: 0px 0px 10px -1px;
            }
        </style>
    </head>
    <body>
        <div class="box_shadow"></div>
    </body>
</html>
```

# multiple shadows

![image-20210703170334862](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703170334862.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .box_shadow{
                width: 100px;
                height: 100px;
                margin: 100px;
                box-shadow: 
                    -52px -52px 0px 0px #f65314,
                    52px -52px 0px 0px #7cbb00,
                    -52px 52px 0px 0px #00a1f1,
                    52px 52px 0px 0px #ffbb00;
            }
        </style>
    </head>
    <body>
        <div class="box_shadow"></div>
    </body>
</html>
```





