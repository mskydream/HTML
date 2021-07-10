# Getting started with CSS

## External Stylesheet

An external CSS stylesheet can be applied to any number of HTML documents by placing a <link> element in each
HTML document.
The attribute rel of the <link> tag has to be set to "stylesheet" , and the href attribute to the relative or absolute
path to the stylesheet. While using relative URL paths is generally considered good practice, absolute paths can be
used, too. In HTML5 the type attribute can be omitted.
It is recommended that the <link> tag be placed in the HTML ﬁle's <head> tag so that the styles are loaded before
the elements they style. Otherwise, users will see a ﬂash of unstyled content.

![image-20210701110258349](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701110258349.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <link rel="stylesheet" type="text/css" href="style/style.css">
        </head>
        <body>
            <h1>Hello world!</h1>
            <p>I ♥ CSS</p>

        </body>
    </html>
```

```css
h1{
    color:green;
    text-decoration:underline;
}
p{
    font-size: 25px;
    font-family: 'Trebuched MS', sans-serif;
}
```

## Internal Styles

CSS enclosed in <style></style> tags within an HTML document functions like an external stylesheet, except that
it lives in the HTML document it styles instead of in a separate ﬁle, and therefore can only be applied to the
document in which it lives. Note that this element must be inside the <head> element for HTML validation (though it
will work in all current browsers if placed in body ).

![image-20210701110701130](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701110701130.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                h1{
                    color: green;
                    text-decoration: underline;
                }
                p{
                    font-size: 25px;
                    font-family: 'Trebuched MS',sans-serif;
                }
            </style>
        </head>
        <body>
            <h1>Hello world!</h1>
            <p>I ♥ CSS</p>
        </body>
    </html>
```

## CSS @import rule (one of CSS at-rule)

The @import CSS at-rule is used to import style rules from other style sheets. These rules must precede all other
types of rules, except @charset rules; as it is not a nested statement, @import cannot be used inside conditional
group at-rules. @import .

**How to use @import**

You can use @import rule in following ways:

A. With internal style tag

```html
<style>
	@import url(' /css/styles.css');
</style>
```

B. With external stylesheet

The following line imports a CSS ﬁle named additional-styles.css in the root directory into the CSS ﬁle in which it
appears:

```css
@import '/additional-styles.css';
```

Importing external CSS is also possible. A common use case are font ﬁles.

```css
@import 'https://fonts.googleapis.com/css?family=Lato';
```

## Inline Styles

Use inline styles to apply styling to a speciﬁc element. Note that this is not optimal. Placing style rules in a <style>
tag or external CSS ﬁle is encouraged in order to maintain a distinction between content and presentation.
Inline styles override any CSS in a <style> tag or external style sheet. While this can be useful in some
circumstances, this fact more often than not reduces a project's maintainability.
The styles in the following example apply directly to the elements to which they are attached.

![image-20210701111357537](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701111357537.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
        </head>
        <body>
            <h1 style="color: green; text-decoration: underline;">Hello world!</h1>
            <p style="fonts-size:25px;font-family: 'Trebuched MS';">I ♥ CSS</p>
        </body>
    </html>
```

## Styling Lists with CSS

There are three diﬀerent properties for styling list-items: list-style-type , list-style-image , and list-style-
position , which should be declared in that order. The default values are disc, outside, and none, respectively. Each
property can be declared separately, or using the list-style shorthand property.
list-style-type deﬁnes the shape or type of bullet point used for each list-item.

disc
circle
square
decimal
lower-roman
upper-roman
none

To use square bullet points for each list-item, for example, you would use the following property-value pair:

```css
li{
	list-style-type:square;
}
```

