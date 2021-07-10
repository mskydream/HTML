# Length Units

## Creating scalable elements using rems and ems

You can use rem deﬁned by the font-size of your html tag to style elements by setting their font-size to a value of
rem and use em inside the element to create elements that scale with your global font-size .

![image-20210703113320870](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703113320870.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            html{
                font-size: 16px;
            }
            
        </style>
    </head>
    <body>
        <input type="button" value="Button">
        <input type="range">
        <input type="text" value="Text">
    </body>
</html>
```

## Font size with rem
CSS3 introduces a few new units, including the rem unit, which stands for "root em". Let's look at how rem works.
First, let's look at the diﬀerences between em and rem .
em: Relative to the font size of the parent. This causes the compounding issue
rem: Relative to the font size of the root or <html> element. This means it's possible to declare a single font
size for the html element and deﬁne all rem units to be a percentage of that.
The main issue with using rem for font sizing is that the values are somewhat diﬃcult to use. Here is an example of
some common font sizes expressed in rem units, assuming that the base size is 16px :

```css
html{
    font-size:16px;
}
h1{
    font-size:2rem;
}
p{
    font-size:1rem;
}
li{
    font-size:1.5em;
}
```

## using percent %

One of the useful unit when creating a responsive application.
Its size depends on its parent container.

![image-20210703113904387](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703113904387.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            *{
                color:#CCC;
            }
            .parent{
                background-color: blue;
                width: 100px;
            }
            .child{
                background-color: green;
                width: 50%;
            }
        </style>
    </head>
    <body>
        <div class="parent">
            PARENT 
            <div class="child">
                CHILD 
            </div>
        </div>
    </body>
</html>
```

