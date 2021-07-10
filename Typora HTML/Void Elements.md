# Void Elements

Not all HTML tags are of the same structure. While most elements require an opening tag, a closing tag, and
contents, some elements - known as void elements - only require an opening tag as they themselves do not contain
any elements. This topic explains and demonstrates the proper usage of void elements in HTML

## Void elements

**HTML 4.01/XHTML 1.0 Strict includes the following void elements:**

area - clickable, deﬁned area in an image
base - speciﬁes a base URL from which all links base
br - line break
col - column in a table [deprecated]
hr - horizontal rule (line)
img - image
input - ﬁeld where users enter data
link - links an external resource to the document
meta - provides information about the document
param - deﬁnes parameters for plugins

**HTML 5 standards include all non-deprecated tags from the previous list and**

command - represents a command users can invoke [obsolete]
keygen - facilitates public key generation for web certiﬁcates [deprecated]
source - speciﬁes media sources for picture , audio , and video elements

The example below does not include void elements:

![image-20210630111410942](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630111410942.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <div>
            <a href="http://stackoverflow.com">
                <h3>Click here ti visit <i>Stack Overflow</i></h3>
            </a>
            <button onclick="alert('Hello');">Say Hello!</button>
            <p>My favorite language is <b>HTML</b>. Here are my other:</p>
            <ol>
                <li>CSS</li>
                <li>JavaScript</li>
                <li>PHP</li>
            </ol>
        </div>
    </body>
</html>
```



