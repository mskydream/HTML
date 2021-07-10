#  Marking-up Quotes

## Inline with <q>

The q element can be used for a quote that is part of a sentence:

![image-20210630150137997](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630150137997.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <p>She wrote <q>The answer is 42.</q> and everyone agreed.</p>
    </body>
</html>
```

**Quotation marks**

Quotation marks should not be added. User agents should (in HTML 4.01) resp. must (in HTML 4.0) render them
automatically.

Quotation marks must not be added. User agents will render them automatically.

**Source URL ( cite attribute)**

The cite attribute can be used to reference the URL of the quoted source:

![image-20210630150506971](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630150506971.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <p>She wrote <q cite="http://example.com/blog/hello-world">The answer is 42.</q> and eveyone
        agreed.</p>
    </body>
</html>
```

## Block with <blockquote>

The blockquote element can be used for a (block-level) quote:

![image-20210630150724574](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630150724574.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <blockquote>
            <p>The answer is 42.</p>
        </blockquote>
    </body>
</html>
```

The cite attribute can be used to reference the URL of the quoted source:

![image-20210630150932274](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630150932274.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <blockquote cite="http://example.com/blog/hello-world">
            <p>The answer is 42.</p>
        </blockquote>
    </body>
</html>
```

Note that browsers typically don’t show this URL, so if the source is relevant, you should add a hyperlink ( a element)
in addition (see the section Citation/Attribution about where to place this link).

**Citation/Attribution**

The citation/attribution should not be part of the blockquote element:

![image-20210630151313476](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630151313476.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <blockquote>
            <p>The answer is 42.</p>
        </blockquote>
        <p>Source: <cite><a href="http://example.com/blog/hello-world" rel="external">Hello World</a></cite></p>
    </body>
</html>
```



