# Clipping and Masking

## Clipping and Masking: Overview and Difference

With Clipping and Masking you can make some speciﬁed parts of elements transparent or opaque. Both can be
applied to any HTML element.
**Clipping**
Clips are vector paths. Outside of this path the element will be transparent, inside it's opaque. Therefore you can
deﬁne a clip-path property on elements. Every graphical element that also exists in SVG you can use here as a
function to deﬁne the path. Examples are circle() , polygon() or ellipse() .

## Simple mask that fades an image from solid to transparent

![image-20210704130755089](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704130755089.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                height: 200px;
                width: 200px;
                background: url(http://lorempixel.com/200/200/nature/1);
                mask-image: linear-gradient(to right, white, transparent);
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```

# Clipping (Circle)

![image-20210704130941783](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704130941783.png)

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
                background: teal;
                clip-path: circle(30% at 50% 50%);
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```

## Clipping (Polygon)

![image-20210704131328203](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704131328203.png)

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
                background: teal;
                clip-path: poligon(0 0, 0 100%,100% 50%);
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```

## Using masks to cut a hole in the middle of an image
![image-20210704131603276](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704131603276.png)

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
                background: url(http://lorempixel.com/200/200/abstract/6);
                mask-image: radial-gradient(circle farthest-side at center, transparent 49%, white 50%);
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```

## Using masks to create images with irregular shapes

![image-20210704132311306](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704132311306.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                height: 200px;
                width: 400px;
                background-image: url(http://lorempixel.com/400/200/nature/4);
                mask-image: linear-gradient(to top right, transparent 49.5%, white 50.5%), linear-gradient(to top left, transparent 49.5%, white 50.5%), linear-gradient(white,white);
                mask-size: 75% 25%, 25% 25%, 100% 75%;
                mask-position: bottom left, bottom right, top left;
                mask-repeat: no-repeat
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
</html>
```

