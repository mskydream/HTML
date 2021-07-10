# Filter Property

![image-20210703163200682](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703163200682.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            img{
                -webkit-filter: blur(1px);
                filter: blur(1px);
            }
        </style>
    </head>
    <body>
        <img src="img/donald-duck14.png" alt="Donald Dcuk" title="Donald Duck">
    </body>
</html>
```

## Drop Shadow (use box-shadow instead if possible)

![image-20210703163426056](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703163426056.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            p{
                -webkit-filter: drop-shadow(10px 10px 1px green);
                filter: drop-shadow(10px 10px 1px green);
            }
        </style>
    </head>
    <body>
        <p>My shadow always follow me.</p>
    </body>
</html>
```

## Hue Rotate

![image-20210703163652331](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703163652331.png)

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>CSS</title>
    <style>
        img{
            -webkit-filter: hue-rotate(120deg);
            filter: hue-rotate(120deg);
        }
    </style>
</head>
<body>
    <img src="img/donald-duck14.png" alt="Donald Duck" title="Donald Duck">
</body>
</html>
```

## Multiple Filter Values
To use multiple ﬁlters, separate each value with a space.

![image-20210703163916803](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703163916803.png)

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>CSS</title>
    <style>
        img{
            -webkit-filter: brightness(200%) grayscale(100%) sepia(100%) invert(100%);
            filter: brightness(200%) grayscale(100%) sepia(100%) invert(100%);
        }
    </style>
</head>
<body>
    <img src="img/donald-duck14.png" alt="Donald Duck" title="Donald Duck">
</body>
</html>
```

# Invert Color

![image-20210703164237224](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703164237224.png)

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>CSS</title>
    <style>
        div{
            width: 100px;
            height: 10  0px;
            background-color: white;
            -webkit-filter: invert(100%);
            filter: invert(100%);
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```

