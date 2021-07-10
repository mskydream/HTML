# Marking up computer code

## Block with <pre> and <code>

If the formatting (white space, new lines, indentation) of the code matters, use the pre element in combination with
the code element:

![image-20210630145311675](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630145311675.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <pre>
            <code>
                x = 42
                if x == 42:
                    print "x is ...            ...42"
            </code>
        </pre>
    </body>
</html>
```

You still have to escape characters with special meaning in HTML (like < with &lt; ), so for displaying a block of HTML
code ( <p>This is a paragraph.</p> ), it could look like this:

![image-20210630145500178](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630145500178.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <pre>
            <code>
                &lt;p>This is a paragraph.&lt;/p>
            </code>
        </pre>
    </body>
</html>
```

## Inline with <code>

If a sentence contains computer code (for example, the name of an HTML element), use the code element to mark it
up:

![image-20210630145651623](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630145651623.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <p>The <code>a</code> element creates a huperlink.</p>
    </body>
</html>
```

