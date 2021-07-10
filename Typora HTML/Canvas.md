# Canvas

height---------Speciﬁes the canvas height
width----------Speciﬁes the canvas width

## Basic example

The canvas element was introduced in HTML5 for drawing graphics.

Drawing two rectangles on a <canvas>

![image-20210630142254482](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630142254482.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
            canvas{
                border:1px solid gray;
            }
        </style>
        <script>
            window.onload = init;
            function init(){
                var canvas = document.querySelector('canvas');
                var ctx = canvas.getContext('2d');
                ctx.fillStyle = 'red';
                ctx.fillRect(0,0,100,100);
                ctx.fillStyle = 'green';
                ctx.fillRect(25,25,50,50);
            }
        </script>
    </head>
    <body>
        <canvas width=300 height=200>Your browser does not support canvas.</canvas>
    </body>
</html>
```

