# Text Formatting 

## Highlighting

### The <mark> element is new in HTML5 and is used to mark or highlight text in a document "due to its relevance in
another context".1
The most common example would be in the results of a search were the user has entered a search query and
results are shown highlighting the desired query.

![image-20210629130445739](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629130445739.png)

``` html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <p>Here is some content from an article that contains the <mark>searched query</mark> that 
        we are looking for. Highlighting the text will make it easier for the user to find what they
        are looking for.</p>
    </body>
</html>
```

### Abbreviation

To mark some expression as an abbreviation, use <abbr> tag:

![image-20210629130823088](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629130823088.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <p>I like to write <abbr title="Hypertext Markup Language">HTML</abbr>!</p>
    </body>
</html>
```

### Inserted, Deleted, or Stricken

To mark text as inserted, use the <ins> tag:
<ins>New Text</ins>
To mark text as deleted, use the <del> tag:
<del>Deleted Text</del>
To strike through text, use the <s> tag:
<s>Struck-through text here</s>

![image-20210629131303404](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629131303404.png)

```Html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <ins>New Text</ins><br>
        <del>Deleted Text</del><br>
        <s>Struck-through text here</s>
    </body>
</html>
```

### Superscript and Subscript

To oﬀset text either upward or downward you can use the tags <sup> and <sub> .

![image-20210629131557254](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629131557254.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <sup>Superscript here</sup>
        <sub>Subscript here</sub>
    </body>
</html>
```

