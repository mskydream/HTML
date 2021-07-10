# List Styles

A list consists of <li> elements inside a containing element ( <ul> or <ol> ). Both the list items and the container can
have margins and paddings which inﬂuence the exact position of the list item content in the document. The default
values for the margin and padding may be diﬀerent for each browser. In order to get the same layout cross-
browser, these need to be set speciﬁcally.
Each list item gets a 'marker box', which contains the bullet marker. This box can either be placed inside or outside
of the list item box.

```css
list-style-position: inside;
```

places the bullet within the <li> element, pushing the content to the right as needed.

```css
list-style-position: outside;
```

places the bullet left of the <li> element. If there is not enough space in the padding of the containing element, the
marker box will extend to the left even if it would fall oﬀ the page.
Showing the result of inside and outside positioning: jsﬁddle

## Section 34.2: Removing Bullets / Numbers

Sometimes, a list should just not display any bullet points or numbers. In that case, remember to specify margin
and padding.

![image-20210703171851827](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703171851827.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            ul{
                list-style-type: none;
            }
            li{
                margin:0;
                padding: 0;
            }
        </style>
    </head>
    <body>
        <ul>
            <li>first item</li>
            <li>second item</li>
        </ul>
    </body>
</html>
```

