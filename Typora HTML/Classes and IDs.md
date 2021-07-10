# Classes and IDs

Classes and IDs make referencing HTML elements from scripts and stylesheets easier. The class attribute can be
used on one or more tags and is used by CSS for styling. IDs however are intended to refer to a single element,
meaning the same ID should never be used twice. IDs are generally used with JavaScript and internal document
links, and are discouraged in CSS. This topic contains helpful explanations and examples regarding proper usage of
class and ID attributes in HTML.

## Giving an element a class

Classes of the same name can be given to any number of elements on a page and they will all receive the styling
associated with that class. This will always be true unless you specify the element within the CSS.
For example, we have two elements, both with the class highlight :

![image-20210629150901968](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629150901968.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
    </head>
    <body>
        <div class="highlight">Lorem ipsum</div>
        <span class ="highlight">Lorem ipsum</span>
    </body>
</html>
```

## Acceptable Values

So the value can be all digits, just one digit, just punctuation characters, include special characters, whatever. Just
no whitespace.
So these are valid:

![image-20210629152009385](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629152009385.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
    </head>
    <body>
        <div id="container"> ... </div>
        <div id="999"> ... </div>
        <div id="%LV-||"> ... </div>
        <div id="____V"> ... </div>
        <div id="⌘⌥"> ... </div>
        <div id="♥"> ... </div>
        <div id="{}"> ... </div>
        <div id="©"> ... </div>
        <div id="♤₩¤☆€~¥"> ... </div>
    </body>
</html>
```

