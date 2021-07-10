# Floats

## Float an Image Within Text

The most basic use of a ﬂoat is having text wrap around an image. The below code will produce two paragraphs
and an image, with the second paragraph ﬂowing around the image. Notice that it is always content after the
ﬂoated element that ﬂows around the ﬂoated element.

![image-20210702134629675](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702134629675.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            img{
                float:left;
                margin-right: 1rem;
            }
        </style>
    </head>
    <body>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent libero.
            Sed cursus ante dapibus diam. Sed nisi. Nulla quism sem at nibh elementum imperdiet. Duis sagittis 
            ipsum. Praesent mauris. Fusce nec tellus sed augue semper porta. Mauris massa. Vestibulum lacinia 
            arcu eget nulla.
        </p>
        <img src="http://lorempixel.com/200/100/">
        <p>Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptor himenaeos.
            Curbitur sodales ligula in libero. Sed dignissim lacinia nunc. Curabitur tortor. Pellentesque 
            nibh. Aenean quam. In scelerisque sem at dolor. Maeceanas mattis. Sed convallis tristique sem. 
            Proin utligula vel nunc egestas porttitor. Morbi lectus risus, iaculis vel, suscipit quis, luctus 
            non, massa. Fusce ac turpis quis ligula lacinia aliquet.
        </p>
    </body>
</html>
```

## clear property

![image-20210702140332341](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702140332341.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            img{
                float: left;
            }
            p.clear{
                clear:both;
            }
        </style>
    </head>
    <body>
        <img src="https://static.pexels.com/photos/69372/pexels-photo-69372-medium.jpeg" width="100px">
        <p>Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem
            ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum </p>
        <p class="clear">LOrem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem
            ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum Lorem ipsoum
        </p>
    </body>
</html>
```

## In-line DIV using ﬂoat

The div is a block-level element, i.e it occupies the whole of the page width and the siblings are place one below the
other irrespective of their width.

```html
<div>
	<p>This is DIV 1</p>
</div>
<div>
	<p>This is DIV 2</p>
</div>
```

We can make them in-line by adding a float css property to the div .

![image-20210702141100590](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702141100590.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .inner-div1{
                width: 50%;
                margin-right:0px;
                float:left;
                background: #337ab7;
                padding:50px 0px;
            }
            .inner-div2{
                width: 50%;
                margin-right: 0px;
                float:left;
                background: #dd2c00;
                padding: 50px 0px;
            }
            p{
                text-align: center;
            }
        </style>
    </head>
    <body>
        <div class="outer-div">
            <div class="inner-div1">
                <p>This is DIV 1</p>
            </div>
            <div class="inner-div2">
                <p>This is DIV 2</p>
            </div>
        </div>
    </body>
</html>
```

## Simple Two Fixed-Width Column Layout

A simple two-column layout consists of two ﬁxed-width, ﬂoated elements. Note that the sidebar and content area
are not the same height in this example. This is one of the tricky parts with multi-column layouts using ﬂoats, and
requires workarounds to make multiple columns appear to be the same height.

![image-20210702142751355](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702142751355.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .wrapper{
                width:600px;
                padding:20px;
                background-color: pink;
                overflow:hidden;
            }
            .sidebar{
                width:150px;
                float:left;
                background-color: blue;
            }
            .content{
                width: 450px;
                float:right;
                background-color:yellow;
            }
        </style>
    </head>
    <body>
        <div class="wrapper">
            <div class="sidebar">
                <h2>Sidebar</h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio.</p>
            </div>
            <div class="content">
                <h1>Content</h1>
                <p>Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos 
                    himaneos. Curabitur sodales ligula in liero. Sed dignissim lacinia nunc. Curabitur 
                    tortor. Pellentesque nibh. Aenean quam. In scelerisque sem at dolor. Maecenas mattis. 
                    Sed convallis tristique sem. Proin ut ligula vel nunc egestas porttitor. Morbi lectur risus,
                    iaculis vel, suscipit quis, luctus non, massa. Fusce ac turpis quis ligula lacinia aliquet.
                </p>
            </div>
        </div>
    </body>
</html>
```

## Simple Three Fixed-Width Column Layout

![image-20210702164144880](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702164144880.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .wrapper{
                width:600px;
                background-color: pink;
                padding:20px;
                overflow:hidden;
            }
            .left-sidebar{
                width:150px;
                background-color: blue;
                float:left;
            }
            .content{
                width: 300px;
                background-color: yellow;
                float:left;
            }
            .right-sidebar{
                width: 150px;
                background-color: green;
                float: right;
            }
        </style>
    </head>
    <body>
        <div class="wrapper">
            <div class="left-sidebar">
                <h1>Left Sidebar</h1>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
            <div class="content">
                <h1>Content</h1>
                <p>Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. 
                    Curabitur sodales ligula in libero. Sed dignissim lacinia nunc. Curabitur tortor. Pellentesque 
                    nibh. Aenean quam. In scelerisque sem at dolor. Maeceans mattis. Sed conallis tristique sem. Proin 
                    ut ligula vel nunc egestas porttitor. Morbi lectur risus, iaculis vel, suscipit quis, luctor non, massa.
                </p>  
            </div>
            <div class="right-sidebar">
                <h1>Right Sidebar</h1>
                <p>Fusce ac turpis quis ligula lacinia aliquet.</p>
            </div>
        </div>
    </body>
</html>
```

## Two-Column Lazy/Greedy Layout

This layout uses one ﬂoated column to create a two-column layout with no deﬁned widths. In this example the left
sidebar is "lazy," in that it only takes up as much space as it needs. Another way to say this is that the left sidebar is
"shrink-wrapped." The right content column is "greedy," in that it takes up all the remaining space.

![image-20210702164635128](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702164635128.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .sidebar{
                display:table;
                float:left;
                background-color:blue;
            }
            .content{
                overflow:hidden;
                bacground-color: yellow;
            }
        </style>
    </head>
    <body>
        <div class="sidebar">
            <h1>Sidebar</h1>
            <img src="http://lorempixel.com/150/200/" >
        </div>>
        <div class="content">
            <h1>Content</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent libero. Sed
                cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet. Duis sagittis
                ipsum. Praesent mauris. Fusce nec tellus sed augue semper porta. Mauris massa. Vestibulum lacinia
                arcu eget nulla. </p>
                <p>Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.
                Curabitur sodales ligula in libero. Sed dignissim lacinia nunc. Curabitur tortor. Pellentesque
                nibh. Aenean quam. In scelerisque sem at dolor. Maecenas mattis. Sed convallis tristique sem. Proin
                ut ligula vel nunc egestas porttitor. Morbi lectus risus, iaculis vel, suscipit quis, luctus non,
                massa. Fusce ac turpis quis ligula lacinia aliquet. Mauris ipsum. Nulla metus metus, ullamcorper
                vel, tincidunt sed, euismod in, nibh. </p>
        </div>
        
    </body>
</html>
```



