# 3D Transforms

Compass pointer or needle shape using 3D transforms

![image-20210703154207530](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703154207530.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div.needle{
                margin: 100px;
                height: 150px;
                width: 150px;
                transform: rotateY(85deg) rotateZ(45deg);
                background-image: linear-gradient(to top left, #555 0%, #555 40%, #333 97%);
                box-shadow: inset 6px 6px 22px 8px #272727;
            }
        </style>
    </head>
    <body>
        <div class="needle"></div>
    </body>
</html>
```

## 3D text eect with shadow

![image-20210703155635168](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703155635168.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            *{margin:0;padding: 0;}
            html, body{height: 100%;width: 100%;overflow: hidden;background:#09c}
            #title{
                position:absolute;
                top:50%; left:50%;
                transform: translate(-50%,-50%);
                perspective-origin: 50% 50%;
                perspective: 300px;
            }
            h1{
                text-align: center;
                font-size:12vmin;
                font-family: 'Open Sans', sans-serif;
                color:rgba(0,0,0,0.8);
                line-height: 1em;
                transform: rotateY(50deg);
                perspective: 150px;
                perspective-origin: 0% 50%;
            }
            h1:after{
                content:attr(data-content);
                position:absolute;
                left:0;top:0;
                transform-origin: 50% 100%;
                transform: rotateX(-90deg);
                color:#09c;
            }
            #title:before{
                content:'';
                position:absolute;
                top:-150%; left:-25%;
                width: 180%; height: 328%;
                background: rgba(255,255,255,0.7);
                transform-origin: 0 100%;
                transform: translateZ(-200px) rotate(40deg) skewX(35deg);
                border-radius:0 0 100% 0;
            }
        </style>
    </head>
    <body>
        <div id="title">
            <h1 data-content="HOVER">HOVER</h1>
        </div>
    </body>
</html>
```

## backface-visibility

 The backface-visibility property relates to 3D transforms. With 3D transforms and the backface-visibility property, you're able to rotate an element such that the original front of an element no longer faces the screen.

For example, this would flip an element away from the screen:

![image-20210703160256588](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703160256588.png)

````html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .flip{
                -webkit-transform: rotateY(180deg);
                -moz-transform: rotateY(180deg);
                -ms-transform: rotateY(180deg);
                -webkit-backface-visibility: visible;
                -moz-backface-visibility: visible;
                -ms--moz-backface-visibility: visible;
                -ms-backface-visibility: visible;
            }
            .flip.back{
                -webkit-backface-visibility: hidden;
                -moz-backface-visibility: hidden;
                -ms--ms-backface-visibility: hidden;    
            }
        </style>
    </head>
    <body>
        <div class="flip">Loren ipsum</div>
        <div class="flip back"></div>
    </body>
</html>
````

## 3D cube 

3D transforms can be use to create many 3D shapes. Here is a simple 3D CSS cube example:

![image-20210703161708089](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703161708089.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            body{
                perspective-origin: 50% 100%;
                perspective: 1500px;
                overflow: hidden;
            }         
            .cube{
                position: relative;
                padding-bottom: 20%;
                transform-style: preserve-3d;
                transform-origin: 50% 100%;
                transform: rotateY(45deg) rotateX(0);
            }
            .cubeFace{
                position:absolute;
                top:0;
                left: 40%;
                width: 20%;
                height: 100%;
                margin: 0 auto;
                transform-style: inherit;
                background: #c52329;
                box-shadow: inset 0 0 0 5px #333;
                transform-origin: 50% 50%;
                transform: rotateX(90deg);
                backface-visibility: hidden; 
            }
            .face2{
                transform-origin: 50% 50%;
                transform: rotateZ(90deg) translateX(100%) rotateY(90deg);
            }
            .cubeFace:before, .cubeFace:after{
                content: '';
                position: absolute;
                width: 100%;
                height: 100%;
                transform-origin: 0 0 ;
                background: inherit;
                box-shadow: inherit;
                backface-visibility: inherit;
            }
            .cubeFace:before{
                top:100%;
                left: 0;
                transform: rotateX(-90deg);
            }
            .cubeFace:after{
                top:0;
                left: 100%;
                transform: rotateY(90deg);
            }
        </style>
    </head>
    <body>
        <div class="cube">
            <div class="cubeFace"></div>
            <div class="cubeFace face2"></div>
        </div>
    </body>
</html>
```

