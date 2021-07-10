# IFrames

name-------------------------Sets the element's name, to be used with an a tag to change the iframe's src .
width -------------------------Sets the element's width in pixels.
height -----------------------Sets the element's height in pixels.
src ---------------------------Speciﬁes the page that will be displayed in the frame.
srcdoc -----------------------Speciﬁes the content that will be displayed in the frame, assuming the browser supports it. The
content must be valid HTML.
sandbox---------------------When set, the contents of the iframe is treated as being from a unique origin and features
                                       including scripts, plugins, forms and popups will be disabled. Restrictions can be selectively
relaxed by adding a space separated list of values. See the table in Remarks for possible values.
allowfullscreen--------------Whether to allow the iframe’s contents to use requestFullscreen()

## Basics of an inline Frame

The term "IFrame" means Inline Frame. It can be used to include another page in your page. This will yield a small
frame which shows the exact contents of the base.html .

![image-20210630133423576](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630133423576.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <iframe src="base.html"></iframe>
    </body>
</html>
```

## Sandboxing

The following embeds an untrusted web page with all restrictions enabled

![image-20210630133654045](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630133654045.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <iframe src="http://example.com"></iframe>
    </body>
</html>
```

To allow the page to run scripts and submit forms, add allow-scripts and allow-forms to the sandbox attribute .

![image-20210630133922193](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630133922193.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <iframe sandbox="allow-scripts allow-forms" src="http://example.com"></iframe>
    </body>
</html>
```

If there is untrusted content (such as user comments) on the same domain as the parent web page, an iframe can
be used to disable scripts while still allowing the parent document to interact with it's content using JavaScript.

![image-20210630134200770](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630134200770.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <iframe sandbox="allow-same-origin allow-top-navigation" 
        src="http://example.com/untrusted/comments/page2">
    </body>
</html>
```

## Setting the Frame Size

The IFrame can be resized using the width and height attributes, where the values are represented in pixels (HTML
4.01 allowed percentage values, but HTML 5 only allows values in CSS pixels).

```html
<iframe src="base.html" width="800" heiht="600"></iframes>
```

## Using the "srcdoc" Attribute

The srcdoc attribute can be used (instead of the src attribute) to specify the exact contents of the iframe as a
whole HTML document. This will yield an IFrame with the text "IFrames are cool!"

```html
<iframe srcdoc="<p>IFrame are cool!</p>"></iframe>
```

If the srcdoc attribute isn't supported by the browser, the IFrame will instead fall back to using the src attribute,
but if both the src and srcdoc attributes are present and supported by the browser, srcdoc takes precedence.

```html
<iframe srcdoc="<p>Iframes are cool!"</p> src="base.html"></iframe>
```

In the above example, if the browser does not support the srcdoc attribute, it will instead display the contents of
the base.html page.

## Using Anchors with IFrames

Normally a change of webpage within an Iframe is initiated from with the Iframe, for example, clicking a link inside
the Ifame. However, it is possible to change an IFrame's content from outside the IFrame. You can use an anchor
tag whose href attribute is set to the desired URL and whose target attribute is set to the iframe's name attribute.

![image-20210630135414816](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630135414816.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <iframe src="base.html" name="myIframe"></iframe>
        <a href="base.html" target="myIframe">Change the Iframe content to different_base.html</a>
    </body>
</html>
```

