# Pseudo-Elements

Pseudo-elements are added to selectors but instead of describing a special state, they allow you to style certain
parts of a document.
The content attribute is required for pseudo-elements to render; however, the attribute can have an empty value
(e.g. content: "" ).

```css
div:: after{
    content:'after';
    color:red;
    border: 1px solid red;
}
div{
    color:black;
    border:1px solid black;
    padding: 1px;
}
div::before{
    content: 'before';
    color:green;
    boder: 1px solid green;
}
```

## Pseudo-Elements in Lists
Pseudo-elements are often used to change the look of lists (mostly for unordered lists, ul ).

The ﬁrst step is to remove the default list bullets:

```css
ul{
	list-style-type:none;
}
```

Then you add the custom styling. In this example, we will create gradient boxes for bullets.

![image-20210703114554243](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703114554243.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            li:before{
                content:"";
                display: inline-block;
                margin-right: 10px;
                height: 10px;
                width: 10px;
                background: linear-gradient(red,blue);
            }
        </style>
    </head>
    <body>
        <ul>
            <li>Test I</li>
            <li>Test II</li>
        </ul>
    </body>
</html>
```

