# Using HTML with CSS

CSS provides styles to HTML elements on the page. Inline styling involves usage of the style attribute in tags, and is
highly discouraged. Internal stylesheets use the <style> tag and are used to declare rules for directed portions of
the page. External stylesheets may be used through a <link> tag which takes an external ﬁle of CSS and applies the
rules to the document. This topic covers usage of all three methods of attachment.

## External Stylesheet Use

Use the link attribute in the document's head :

```html
<head>
	<link rel="stylesheet" type="text/css" href="stylesheet.css">
</head>
```

You can also use stylesheets provided from websites via a content delivery network, or CDN for short. (for example,
Bootstrap):

```html
<head>
    <link rel="stylesheet"
    href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-
    BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
</head>
```

## Internal Stylesheet

You can also include CSS elements internally by using the <style> tag:

![image-20210629160445199](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629160445199.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style type="text/css">
            body{
                background-color: gray;
            } 
        </style>
    </head>
    <body>
    </body>
</html>
```

## Inline Style

You can style a speciﬁc element by using the style attribute:

```html
<span style="color: red">This text will appear in red</span>
```

