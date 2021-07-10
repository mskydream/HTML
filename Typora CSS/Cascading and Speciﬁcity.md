# Cascading and Speciﬁcity

## Calculating Selector Speciﬁcity

Each individual CSS Selector has its own speciﬁcity value. Every selector in a sequence increases the sequence's
overall speciﬁcity. Selectors fall into one of three diﬀerent speciﬁcity groups: A, B and c. When multiple selector
sequences select a given element, the browser uses the styles applied by the sequence with the highest overall
speciﬁcity.

**Example 1: Speciﬁcity of various selector sequences**

```css
#foo #bar{}
#foo.bar{}
#foo {}
.bar:hover{}
div.bar{}
:hover{}
[title]{}
.bar{}
div ul + li{}
p::after{}
*::after{}
::before{}
div{}
*{}
```

## The !important declaration

The !important declaration is used to override the usual speciﬁcity in a style sheet by giving a higher priority to a
rule. Its usage is: property : value !important;

```css
#mydiv{
	font-weight: bold !important;
}
#outerdiv #mydiv{
	font-weight: normal;
}
```

Avoiding the usage of !important is strongly recommended (unless absolutely necessary), because it will disturb
the natural ﬂow of css rules which can bring uncertainty in your style sheet. Also it is important to note that when
multiple !important declarations are applied to the same rule on a certain element, the one with the higher
speciﬁcity will be the ona applied.

Here are some examples where using !important declaration can be justiﬁed:
If your rules shouldn't be overridden by any inline style of the element which is written inside style attribute
of the html element.
To give the user more control over the web accessibility, like increasing or decreasing size of the font-size, by
overriding the author style using !important .
For testing and debugging using inspect element.

## Cascading

**Example 1 - Speciﬁcity rules**

```css
.mystyle{color:blue;}
div{color:red;}
<div class="mystyle">Hello World</div>
```

## More complex speciﬁcity example

![image-20210703100328972](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703100328972.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            div{
                font-size: 7px;
                border: 3px dotted pink;
                background-color: yellow;
                color: purple;
            }
            body.mystyle > div.myotherstyle{
                font-size: 11px;
                background-color: green;
            }
            #elmnt1{
                font-size: 24px;
                border-color:red ;
            }
            .mystyle .myotherstyle{
                font-size: 16px;
                background-color: black;
                color: red;
            }
        </style>
    </head>
    <body>
        <div id="elmnt1" class="myotherstyle">
            Hello, world!
        </div>
    </body>
</html>
```

