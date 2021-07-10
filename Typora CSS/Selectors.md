# Selectors

CSS selectors identify speciﬁc HTML elements as targets for CSS styles. This topic covers how CSS selectors target
HTML elements. Selectors use a wide range of over 50 selection methods oﬀered by the CSS language, including
elements, classes, IDs, pseudo-elements and pseudo-classes, and patterns.

**Selects elements with the given attribute.**

![image-20210701113217103](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701113217103.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                div[data-color]{
                    color: RED;
                }
            </style>
        </head>
        <body>
            <div data-color="red">This will be red</div>
            <div data-color="green">This will be red</div>
            <div data-background="red">This will NOT be red</div>
        </body>
    </html>
```

**Selects elements with the given attribute and value where the given attribute contains the given value anywhere (as a substring).**

![image-20210701113724552](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701113724552.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                [class*=foo]{
                    color:red;
                }
            </style>
        </head>
        <body>
            <div class="foo-123">This will be red</div>
            <div class="foo123">This will be red</div>
            <div class="bar123foo">This will be red</div>
            <div class="barfoooo123">This will be red</div>
            <div class="barfo0">This will NOT be red</div>
        </body>
    </html>
```

**Selects elements with the given attribute and value where the given attribute begins with the value.**

![image-20210701114010506](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701114010506.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                [class^="foo-"]{
                    color:red;
                }
            </style>
        </head>
        <body>
            <div class="foo-123">This will be red</div>
            <div class="foo-234">This will be red</div>
            <div class="bar-123">This will NOT be red</div>
        </body>
    </html>
```

Selects elements with a given attribute and value where the attribute's value can be represented as Value , VALUE ,
vAlUe or any other case-insensitive possibility.

![image-20210701114422024](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701114422024.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                [lang="EN" i]{
                    color: red;
                }
            </style>
        </head>
        <body>
            <div lang="EN">This will be red</div>
            <div lang="en">This will be red</div>
            <div lang="PT">This will NOT be red</div>
        </body>
    </html>
```

## Combinators

Descendant Combinator: selector selector
A descendant combinator, represented by at least one space character (), selects elements that are a descendant of
the deﬁned element. This combinator selects all descendants of the element (from child elements on down).

![image-20210701114718471](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701114718471.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                div p{
                    color:red;
                }
            </style>
        </head>
        <body>
           <div>
                <p>My text is red.</p>
                <section>
                    <p>My text is red</p>
                </section>
            </div>
            <p>My text is not red</p>
        </body>
    </html>
```

**Adjacent Sibling Combinator: selector + selector**

The adjacent sibling ( + ) combinator selects a sibling element that immediate follows a speciﬁed element.

![image-20210701115019906](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701115019906.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                p +     p{
                    color:red;
                }
            </style>
        </head>
        <body>
            <p>My text is not red</p>
            <p>My text is red</p>
            <p>My text is red</p>
            <hr>
            <p>My text is not red</p>
        </body>
    </html>
```

**General Sibling Combinator: selector ~ selector**

The general sibling ( ~ ) combinator selects all siblings that follow the speciﬁed element.

![image-20210701115220611](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701115220611.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                p ~ p{
                    color:red;
                }
            </style>
        </head>
        <body>
            <p>My text is not red</p>
            <p>My text is red</p>
            <hr>
            <h1>And now a title</h1>
            <p>My text is red</p>
        </body>
    </html>
```

## Pseudo-classes

Pseudo-classes are keywords which allow selection based on information that lies outside of the document tree or that cannot be expressed by other selectors or combinators. This information can be associated to a certain state
(state and dynamic pseudo-classes), to locations (structural and target pseudo-classes), to negations of the former
(negation pseudo-class) or to languages (lang pseudo-class). Examples include whether or not a link has been
followed ( :visited ), the mouse is over an element ( :hover ), a checkbox is checked ( :checked ), etc.

**Syntax**

```css
selector:pseudo-class{
	property:VALUE;
}
```

## Class Name Selectors

The class name selector select all elements with the targeted class name. For example, the class name .warning
would select the following <div> element:

```html
<div class="warning">
	<p>This would be some warning copy.</p>
</div>
```

You can also combine class names to target elements more speciﬁcally. Let's build on the example above to
showcase a more complicated class selection.

![image-20210701120046752](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701120046752.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                .important{
                    color:orange;
                }
                .warning{
                    color:blue;
                }
                .warning.important{
                    color:red;
                }
            </style>
        </head>
        <body>
            <div class="warning">
                <p>This would be some warning copy.</p>
            </div>
            <div class="important warning">
                <p class="important">This is some really important warning copy.</p>
            </div>
        </body>
    </html>
```

## Select element using its ID without the high speciﬁcity of the ID selector

This trick helps you select an element using the ID as a value for an attribute selector to avoid the high speciﬁcity of
the ID selector.
**HTML:**

```html
<div id="element">...</div>
```

**CSS**

```css
#element{...} /* High specifity will override many selectors */
[id="element"]{...}/* Low specifity, can be overridden easily */
```

## The :last-of-type selector

The :last-of-type selects the element that is the last child, of a particular type, of its parent. In the example below,
the css selects the last paragraph and the last heading h1 .

![image-20210701131541936](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701131541936.png)

```HTML
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                p:last-of-type{
                    background: #C5CAE9;
                }
                h1:last-of-type{
                    background: #CDDC39;
                }
            </style>
        </head>
        <body>
            <div class="container">
                <p>First paragraph</p>
                <p>Second paragraph</p>
                <p>Last paragraph</p>
                <h1>Heading 1</h1>
                <h2>First heading 2</h2>
                <h2>Last heading</h2>
            </div>
        </body>
    </html>
```

## CSS3 :in-range selector example

 ![image-20210701131912493](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701131912493.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                input:in-range{
                    border: 1px solid blue;
                }
            </style>
        </head>
        <body>
            <input type="number" min="10" max="20" value="15">
            <p>The border for this value will be blue</p>
        </body>
    </html>
```

## A. The :not pseudo-class example & B. :focus-within CSS pseudo-class

A. The syntax is presented above.
The following selector matches all <input> elements in an HTML document that are not disabled and don't have the
class .example :

![image-20210701132346658](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701132346658.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                input:in-range{
                    border: 1px solid blue;
                }
                input:not([disablet]):not(.example){
                    background-color: #ccc;
                }
            </style>
        </head>
        <body>
            <form>
                Phone: <input type="tel" class="example">
                E-mail: <input type="email" disabled="disabled">
                Password: <input type="password">
            </form>
        </body>
    </html>
```

See background syntax here.
B. The :focus-within CSS pseudo-class

![image-20210701132800189](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701132800189.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                div{
                    height: 80px;
                }
                input{
                    margin:30;
                }
                div:focus-within{
                    background-color:#1565c0;
                }
            </style>
        </head>
        <body>
            <h3>Background is blue if the input is focused.</h3>
            <div><input type="text"></div>
        </body>
    </html>
```

## The :only-child pseudo-class selector example

The :only-child CSS pseudo-class represents any element which is the only child of its parent.

![image-20210701133616388](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701133616388.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                p:only-child{
                    color:blue;
                }
            </style>
        </head>
        <body>
            <div>
                <p>This paragraph is the only child of the div, it will have the color blue.</p>
            </div>
            <div>
                <p>This paragraph is one of the two children of the div</p>
                <p>This paragraph is one of the two children of its parent</p>
            </div>
        </body>
    </html>
```





