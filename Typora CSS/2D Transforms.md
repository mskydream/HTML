# 2D Transforms

## Rotate

![image-20210703151555381](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703151555381.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .rotate{
                width:100px;
                height: 100px;
                background: teal;
                transform: rotate(45deg);
            }
        </style>
    </head>
    <body>
        <div class="rotate"></div>
    </body>
</html>
```

## Scale

![image-20210703151755949](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703151755949.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .scale{
                width: 100px;
                height: 100px;
                background: teal;
                transform: scale(0.5, 1.3);
            }
        </style>
    </head>
    <body>
        <div class="scale"></div>
    </body>
</html>
```

##  Skew

![image-20210703151954656](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703151954656.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .skew{
                width: 100px;
                height: 100px;
                background: teal;
                transform: skew(20deg, -30deg);
            }
        </style>
    </head>
    <body>
        <div class="skew"></div>
    </body>
</html>
```

## Multiple transforms 

Multiple transforms can be applied to an element in one property like this:

```css
transform: rotate(15deg) translateX(200px);
```

## Translate

![image-20210703152539130](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703152539130.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .translate{
                width: 100px;
                height: 100px;
                background: teal;
                transform: translateX(200px, 50%);
            }
        </style>
    </head>
    <body>
        <div class="translate"></div>
    </body>
</html>
```

On the X axis:

```css
.translate{
	transform: translateX(200px);
}
```

On the Y axis:

```css
.translate{
	transform: translateY(50%);
}
```

## Transform Origin

Transformations are done with respect to a point which is defined by the transform-origin property. 

The property takes 2 values : transform-origin: X Y; 

In the following example the first div (.tl) is rotate around the top left corner with transform-origin: 0 0; and the second (.tr)is transformed around it's top right corner with transform-origin: 100% 0. The rotation is applied on hover :

![image-20210703153254507](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703153254507.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .transform{
                display:inline-block;
                width: 200px;
                height: 100px;
                background: teal;
                transition: transform 1s;
            }
            .origin1{
                transform-origin: 0 0;
            }
            .origin2{
                transform-origin: 100% 0;
            }
            .transform:hover{
                transform: rotate(30deg);
            }
        </style>
    </head>
    <body>
        <div class="transform origin1"></div>
        <div class="transform origin2"></div>
    </body>
</html>
```

