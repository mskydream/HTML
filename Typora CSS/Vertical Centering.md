# Vertical Centering

## Centering with display: table

![image-20210704135348153](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704135348153.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .wrapper{
                height: 600px;
                text-align: center;
            }
            .outer{
                display: table;
                height: 100%;
                width: 100%;
            }
            .outer .inner{
                display: table-cell;
                text-align: center;
                vertical-align: middle;
            }
        </style>
    </head>
    <body>
        <div class="wrapper">
            <div class="outer">
                <div class="inner">
                    centered
                </div>
            </div>
        </div>
    </body> 
</html>
```

## Centering with Flexbox

![image-20210704135922530](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704135922530.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .container{
                height: 500px;
                width: 500px;
                display: flex;
                align-items: center;
                justify-content: center;
                background: white;
            }
            .child{
                width: 100px;
                height: 100px;
                background: blue;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <div class="child"></div>
        </div>
    </body> 
</html>
```

# Centering with Transform

![image-20210704140410134](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704140410134.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .wrapper{
                position: relative;
                height: 600px;
            }
            .centered{
                position: absolute;
                z-index: 999;
                transform: translate(-50%, -50%);
                top: 50%;
                left: 50%;
            }
        </style>
    </head>
    <body>
        <div class="wrapper">
            <div class="centered">
                centered
            </div>
        </div>
    </body> 
</html>
```

# Centering Text with Line Height

![image-20210704140616315](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704140616315.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .container{
                height: 50px;
                line-height: 50px;
                vertical-align: middle;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <span>vertically centered</span>
        </div>
    </body> 
</html>
```

# Centering with Position: absolute

![image-20210704140922781](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704140922781.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .wrapper{
                position: relative;
                height: 600px;
            }
            .wrapper img{
                position: absolute;
                top:0;
                left:0;
                right:0;
                bottom: 0;
                margin:auto;
            }
        </style>
    </head>
    <body>
        <div class="wrapper">
            <img src="http://cdn.sstatic.net/Sites/stackoverflow/company/img/logos/so/so-icon.png?v=c78bd457575a"">
        </div>
    </body> 
</html>
```

If you want to center other then images, then you must give height and width to that element.

![image-20210704141148941](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704141148941.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .wrapper{
                position: relative;
                height: 600px;
            }
            .wrapper .child{
                position: absolute;
                top:0;
                left:0;
                right:0;
                bottom: 0;
                margin:auto;
                width: 200px;
                height: 30px;
                border: 1px solid #f00;
            }
        </style>
    </head>
    <body>
        <div class="wrapper">
            <div class="child">
                make me center
            </div>
        </div>
    </body> 
</html>
```

