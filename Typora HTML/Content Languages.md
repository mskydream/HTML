# Content Languages

## Base Document Language

It’s a good practice to declare the primary language of the document in the html element:
<html lang="en">
If no other lang attribute is speciﬁed in the document, it means that everything (i.e., element content and attribute
text values) is in that language.
If the document contains parts in other languages, these parts should get their own lang attributes to "overwrite"
the language declaration.

## Element Language

The lang attribute is used to specify the language of element content and attribute text values:

![image-20210630140007824](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630140007824.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <p lang="en">The content of this element is in English.</p>
        <p lang="en" title="The value of this attribute is also in English">The content of this element
            is in English.
        </p>
    </body>
</html>
```

## Element with Multiple Languages

You can "overwrite" a language declaration:

![image-20210630140253055](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630140253055.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <p lang="en">This English sentence contains the German word <span lang="de">Hallo</span>.</p>
    </body>
</html>
```

## Regional URLs

It is possible to add the attribute hreflang to the elements <a> and <area> that create hyperlinks. Such it speciﬁes
the language of the linked resource. The language deﬁned must be a valid BCP 47[1] language tag.

![image-20210630140555350](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630140555350.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <p>
            <a href="example.org" hreflang="en">example.org</a> is one of IANA's example domains.
        </p>
    </body>
</html>
```

## Handling Attributes with Different Languages

You can "overwrite" a parent element's language declaration by introducing any element apart from applet , base ,
basefont , br , frame , frameset , hr , iframe , meta , param , script (of HTML 4.0) with an own lang attribute:

![image-20210630140833799](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630140833799.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <p lang="en" title="An English paragraph">
            <span lang="de title="A German sentence>Hallo Welt!</span>
        </p>
    </body>
</html>
```

