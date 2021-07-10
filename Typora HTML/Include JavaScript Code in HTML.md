# Include JavaScript Code in HTML
 ## Handling disabled Javascript

It is possible that the client browser does not support Javascript or have Javascript execution disabled, perhaps due
to security reasons. To be able to tell users that a script is supposed to execute in the page, the <noscript> tag can
be used. The content of <noscript> is displayed whenever Javascript is disabled for the current page.

![image-20210629155258201](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629155258201.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>JS in HTML</title>

    </head>
    <body>
        <script>
            document.write("Hello, world!");
        </script>
        <noscript>This browser does not support Javascript.</noscript>

    </body>
</html>
```

## Linking to an external JavaScript ﬁle

The src attribute works like the href attribute on anchors: you can either specify an absolute or relative URL. The
example above links to a ﬁle inside the same directory of the HTML document. This is typically added inside the <head> tags at the top of the html document

```html
<script src="example.js"></script>
```

## Including a JavaScript ﬁle executing asynchronously

```html
<script type="text/javascript src="URL" asunc></script>
```

