# Anchors and Hyperlinks 

## href

Speciﬁes the destination address. It can be an absolute or relative URL, or the name of an anchor. An
absolute URL is the complete URL of a website like http://example.com/. A relative URL points to
another directory and/or document inside the same website, e.g. /about-us/ points to the directory
“about-us” inside the root directory ( / ). When pointing to another directory without explicitly specifying
the document, web servers typically return the document “index.html” inside that directory.

## hreflang 

Speciﬁes the language of the resource linked by the href attribute (which must be present with this
one). Use language values from BCP 47 for HTML5 and RFC 1766 for HTML 4.

## rel

Speciﬁes the relationship between the current document and the linked document. For HTML5, the
values must be deﬁned in the speciﬁcation or registered in the Microformats wiki.

## target

Speciﬁes where to open the link, e.g. in a new tab or window. Possible values are _blank , _self ,
_parent , _top , and framename (deprecated). Forcing such behaviour is not recommended since it
violates the control of the user over a website.

## title

Speciﬁes extra information about a link. The information is most often shown as a tooltip text when
the cursor moves over the link. This attribute is not restricted to links, it can be used on almost all
HTML tags.

## download

Speciﬁes that the target will be downloaded when a user clicks on the hyperlink. The value of the
attribute will be the name of the downloaded ﬁle. There are no restrictions on allowed values, and the
browser will automatically detect the correct ﬁle extension and add it to the ﬁle (.img, .pdf, etc.). If the
value is omitted, the original ﬁlename is used.

# Link to another site

This is the basic use of the <a> (anchor element) element:

![image-20210629132544186](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629132544186.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <a href="http://example.com">Link to example.com</a>
    </body>
</html>	
```

# Link to an anchor

Anchors can be used to jump to speciﬁc tags on an HTML page. The <a> tag can point to any element that has an id
attribute. To learn more about IDs, visit the documentation about Classes and IDs. Anchors are mostly used to jump
to a subsection of a page and are used in conjunction with header tags.
Suppose you've created a page ( page1.html ) on many topics:

Now you can use the anchor in your table of contents:

![image-20210629133304855](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629133304855.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <h1>Table of Contents</h1>
            <a href="#Topic1">Click to jump to the First Topic</a><br>
            <a href="#Topic2">Click to jump to the Second Topic</a>
    </body>
</html>
```

# Open link in new tab/window

The target attribute speciﬁes where to open the link. By setting it to _blank , you tell the browser to open it in a
new tab or window (per user preference).

![image-20210629133541633](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629133541633.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <a href="example.com" target='_blanck'>Text Here</a>
    </body>
</html>
```

# Link that runs JavaScript

### Simply use the javascript: protocol to run the text as JavaScript instead of opening it as a normal link:

![image-20210629133810039](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629133810039.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <a href="javascript:myFunction();">Link Js</a>
    </body>
</html>
```

### You can also achieve the same thing using the onclick attribute:

![image-20210629134002347](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629134002347.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <a href="#" onclick="myFunction(); return false;">Run this code</a>
    </body>
</html>
```

# Link that runs email client

### If the value of the href -attribute begins with mailto: it will try to open an email client on click:

![image-20210629134206500](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629134206500.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <a href="mailto:example@example.com">Send email</a>
    </body>
</html>
```

### You can populate the subject and body for the new email as well:

![image-20210629134455367](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629134455367.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <a href="mailto:example@example.com?cc=john@example.com&bcc=jane@example.comSend</a>
    </body>
</html>
```

### You can populate the subject and body for the new email as well:

![image-20210629134747615](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629134747615.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <a href="mailto:example@example.com?subject=Example+subject&body=Message+text">Send email</a>
    </body>
</html>
```









