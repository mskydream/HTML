# Image Maps

## Introduction to Image Maps

An image maps is an image with clickable areas that usually act as hyperlinks.
The image is deﬁned by the <img> tag, and the map is deﬁned by a <map> tag with <area> tags to denote each
clickable area. Use the usemap and name attributes to bind the image and the map.

![image-20210629164714255](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629164714255.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <img src="http://jaced.com/blogpix/2007/trisquarecircle/002.gif" usemap="#shapes">  
        <map name="shapes">
            <area shape="polygon" coords="79,6,5,134,153,134">
            <area shape="rectangle" coords="177,6,306,134">
            <area shape="circle" coords="397,71,65">
        </map> 
    </body>
</html>
```

