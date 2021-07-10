# Comments

Similar to other programming, markup, and markdown languages, comments in HTML provide other developers
with development speciﬁc information without aﬀecting the user interface. Unlike other languages however, HTML
comments can be used to specify HTML elements for Internet Explorer only. This topic explains how to write HTML
comments, and their functional applications.

## Creating comments

HTML comments can be used to leave notes to yourself or other developers about a speciﬁc point in code. They can
be initiated with <!-- and concluded with --> , like so:

![image-20210629145715129](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629145715129.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
    </head>
    <body>
        <h1>This part will be displayed <!-- while this will not be displayed -->.</h1>
        <!-- This is a multiline HTML comment.
        Whatever is in here will not be rendered by the browser.
        You can "comment out" entire sections of HTML code.
        -->
    </body>
</html>
```

## Commenting out whitespace between inline elements

Inline display elements, usually such as span or a , will include up to one white-space character before and after
them in the document. In order to avoid very long lines in the markup (that are hard to read) and unintentional
white-space (which aﬀects formatting), the white-space can be commented out.

![image-20210629150436126](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629150436126.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
    </head>
    <body>
        <!-- Use an HTML comment to nullify the newline character below: -->
        <a href="#">I hope there will be no extra whitespace after this!</a><!--
        --><button>Foo</button>
        <hr>
        <!-- Whithout it, you can notice a small formatting difference: -->
        <a href="#">I hope there will be no extra whitespace after this!</a>
        <button>Foo</button>
    </body>
</html>
```

