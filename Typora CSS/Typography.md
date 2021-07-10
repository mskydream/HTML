# Typography

## The Font Shorthand

Whith the syntax:

```css
element{
	font:[font-style] [font-variant] [font-weight] [font-size/line-height] [font-family];
}
```

## Font Size

![image-20210702165426787](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702165426787.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            #element-one{
                font-size:30px;
            }
            #element-two{
                font-size:10px;
            }
        </style>
    </head>
    <body>
        <div id="element-one">Hello I am some text.</div>
        <div id="element-two">Hello I am some smaller text.</div>
    </body>
</html>
```

## Text Overﬂow

The text-overflow property deals with how overﬂowed content should be signaled to users. In this example, the
ellipsis represents clipped text.

![image-20210702165729395](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702165729395.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            body {
            margin: 20px;
            }

            .text {
            overflow: hidden;
            text-overflow: ellipsis;
            display: -webkit-box;
            line-height: 16px;     /* fallback */
            max-height: 32px;      /* fallback */
            -webkit-line-clamp: 2; /* number of lines to show */
            -webkit-box-orient: vertical;
            }
        </style>
    </head>
    <body>
        <div class="text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam consectetur venenatis blandit. Praesent vehicula, libero non pretium vulputate, lacus arcu facilisis lectus, sed feugiat tellus nulla eu dolor. Nulla porta bibendum lectus quis euismod. Aliquam volutpat ultricies porttitor. Cras risus nisi, accumsan vel cursus ut, sollicitudin vitae dolor. Fusce scelerisque eleifend lectus in bibendum. Suspendisse lacinia egestas felis a volutpat.
        </div>
    </body>
</html>
```

## Text Shadow

To add shadows to text, use the text-shadow property. The syntax is as follows:

```css
text-shadow: horizontal-offset vertical-offset blur color;
```

**Shadow without blur radius**

```css
h1{
	text-shadow: 2px 2px #0000ff;
}
```

This creates a blue shadow eﬀect around a heading
**Shadow with blur radius**
To add a blur eﬀect, add an option blur radius argument

```css
h1{
	text-shadow:2px 2px 10px #0000ff;
}
```

**Multiple Shadows**
To give an element multiple shadows, separate them with commas

```css
h1{
	text-shadow:0 0 3px #FF0000, 0 0 5px #0000FF;
}
```

## Text Transform

The text-transform property allows you to change the capitalization of text. Valid values are: uppercase ,
capitalize , lowercase , initial , inherit , and none

![image-20210702170517795](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702170517795.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .example1{
                text-transform: uppercase;
            }
            .example2{
                text-transform: capitalize;
            }
            .example3{
                text-transform: lowercase;
            }
        </style>
    </head>
    <body>
        <p class="example1">
            all letters in uppercase
        </p>
        <p class="example2">
            all letters in capitalize
        </p>
        <p class="example3">
            all letters in lowercase
        </p>
    </body>
</html>
```

## Letter Spacing

```css
h2{
	letter-spacing: 1px;
}
```

The letter-spacing property is used to specify the space between the characters in a text.
! letter-spacing also supports negative values:

```css
p{
	letter-spacing: -1px;
}
```

## Text Decoration

The text-decoration property is used to set or remove decorations from text.

```css
h1{text-decoration: none;}
h2{text-decoration:overline;}
h3{text-decoration:line-through;}
h4{tsxt-decoration:underline;}
```

text-decoration can be used in combination with text-decoration-style and text-decoration-color as a shorthand
property:

```css
.title{text-decoration:undeline dotted blue;}
```

This is shorthand version of

```css
.title{
	text-decoration-style:dotted;
	text-decoration-line:underline;
	text-decoration-color:blue;
}
```

##  Word Spacing

The word-spacing property speciﬁes the spacing behavior between tags and words.

![image-20210702171633352](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702171633352.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .normal{word-spacing: normal;}
            .narrow{word-spacing: -3px;}
            .extensive{word-spacing: 10px;}
        </style>
    </head>
    <body>
        <p>
            <span class="normal">This is an example, showing the effect of "word-spacing".</span><br>
            <span class="narrow">This is an esample, showing the effect of "word-spacing".</span><br>
            <span class="extensive">This is an example, showing the effect of "word-spacing".</span>
        </p>
    </body>
</html>
```

## Font Variant

Sets every letter to uppercase, but makes the lowercase letters(from original text) smaller in size than the letters
that originally uppercase.

![image-20210702172006976](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702172006976.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .smallcaps{
                font-variant: small-caps;
            }
        </style>
    </head>
    <body>
        <p class="smallcaps">
            Documentation about CSS Fonts
            <br>
            aNd ExAmpLe
        </p>
    </body>
</html>
```

Note: The font-variant property is a shorthand for the properties: font-variant-caps, font-variant-numeric, font-
variant-alternates, font-variant-ligatures, and font-variant-east-asian.

