# Images

To add an image to a page, use the image tag.
Image tags ( img ) do not have closing tags. The two main attributes you give to the img tag are src , the image source
and alt , which is alternative text describing the image.

![image-20210629161318915](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629161318915.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <img src="avatarko_anonim.jpg" alt="Hello World!">
    </body>
</html>
```

You can also get images from a web URL:



![image-20210629161512625](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629161512625.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <img src="https://i.stack.imgur.com/ALgZi.jpg?s=48&g=1" alt="StackOverflow user Caleb Kleveter">
    </body>
</html>
```

# Choosing alt text

Alt-text is used by screen readers for visually impaired users and by search engines. It's therefore important to
write good alt-text for your images.
The text should look correct even if you replace the image with its alt attribute. For example:

![image-20210629162319967](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629162319967.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <img src="yin-and-yang.jpg" alt="Anonymous user avatar" /> An anonymous user wrote:
        <blockquote>Lorem ipsum dolor sed.</blockquote>
        <a href="https://google.com"><img src="shortcut.jpg" alt="Edit icon" /></a> /
        <a href="http://google.com"><img src="fav-icon.jpg" alt="Delete icon"></a>
    </body>
</html>
```

To correct this:
Remove the alt-text for the avatar. This image adds information for sighted users (an easily identiﬁable icon
to show that the user is anonymous) but this information is already available in the text.1
Remove the "icon" from the alt-text for the icons. Knowing that this would be an icon if it were there does not
help to convey its actual purpose.

![image-20210629162717293](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629162717293.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <img src="fav-icon.jpg" alt="" />An anonymous user wrote:
        <blockquote>Lorem ipsum dolor sed.</blockquote>
        <a href="https://google.com"><img src="yin-and-yang.jpg" alt="Edit"></a>
        <a href="https://google.com"><img src="shortcut.jpg" alt="Delete"></a>
    </body>
</html>
```

## Responsive image using picture element

To display diﬀerent images under diﬀerent screen width, you must include all images using the source tag in a
picture tag as shown in the above example.

![image-20210629163639982](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629163639982.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <picture>
            <source media="(min-width: 600px)" srcset="shortcut.jpg">
            <source media="(min-width:450px)" srcset="yin-and-yag.jpg">
            <img src="defauld_image.jpg" style="width: auto;">
        </picture>
    </body>
</html>
```

