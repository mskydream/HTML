# Border

## border-radius

The border-radius property allows you to change the shape of the basic box model.
Every corner of an element can have up to two values, for the vertical and horizontal radius of that corner (for a
maximum of 8 values).

![image-20210702105602023](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702105602023.png)

The ﬁrst set of values deﬁnes the horizontal radius. The optional second set of values, preceded by a ‘/’ , deﬁnes the
vertical radius. If only one set of values is supplied, it is used for both the vertical and horizontal radius.

```css
border-radius: 10px 5% / 20px 25em 30px 35em;
```

The 10px is the horizontal radius of the top-left-and-bottom-right. And the 5% is the horizontal radius of the top-
right-and-bottom-left. The other four values after '/' are the vertical radii for top-left, top-right, bottom-right and
bottom-left.
As with many CSS properties, shorthands can be used for any or all possible values. You can therefore specify
anything from one to eight values. The following shorthand allows you to set the horizontal and vertical radius of
every corner to the same value:

![image-20210702105955708](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702105955708.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .box{
                width: 250px;
                height: 250px;
                background-color:black;
                border-radius:10px;
            }
        </style>
    </head>
    <body>
        <div class='box'></div>
    </body>
</html>
```

## border-style

The border-style property sets the style of an element's border. This property can have from one to four values
(for every side of the element one value.)

Example:

```css
border-style: dotted;
border-style: dotted solid double dashed;
```

![image-20210702110205219](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702110205219.png)

# border-[left|right|top|bottom]

The border-[left|right|top|bottom] property is used to add a border to a speciﬁc side of an element.
For example if you wanted to add a border to the left side of an element, you could do:

```css
#element{
	border-left: 1px solid black;
}
```

