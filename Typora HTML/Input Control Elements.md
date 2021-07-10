#  Input Control Elements

## Text

The most basic input type and the default input if no type is speciﬁed. This input type deﬁnes a single-line text ﬁeld
with line-breaks automatically removed from the input value. All other characters can be entered into this. <input>
elements are used within a <form> element to declare input controls that allow users to input data.

![image-20210629165038746](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629165038746.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>

        <input type="text" size="50">
    </body>
</html>
```

## Checkbox and Radio Buttons

Checkboxes and radio buttons are written with the HTML tag <input> , and their behavior is deﬁned in the HTML
speciﬁcation.

Radio buttons usually come in groups (if it's not grouped with another radio button, you probably meant to use a
checkbox instead) identiﬁed by using the same name attribute on all buttons within that group. The selection of
radio buttons are mutually exclusive, meaning the user may only select one choice from a group of radio buttons.
When a radio button is checked, any other radio button with the same name that was previously checked becomes
unchecked.

![image-20210629165618406](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629165618406.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="radio" name="color" id="red" value="#FF0000">
        <input type="radio" name="color" id="green" value="#00FF00">
        <input type="radio" name="color" id="blue" value="#0000FF">
    </body>
</html>
```

### Accessibility

To give context to the buttons and show users what each button is for, each of them should have a label. This can
be done using a <label> element to wrap the button. Also, this makes the label clickable, so you select the
corresponding button.

![image-20210629170109865](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629170109865.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <label>
            <input type="radio" name="color" value='#ff0000'>
            Red
        </label>
    </body>
</html>
```

### Button Groups

Since each radio button aﬀects the others in the group, it is common to provide a label or context for the entire
group of radio buttons.
To provide a label for the entire group, the radio buttons should be included in a <fieldset> element with a
<legend> element within it.

![image-20210629170638577](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629170638577.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <fieldset>
            <legend>Theme color:</legend>
            <p>
                <input type="radio" name=color id="red" value="#F00">
                <label for="red">Red</label>
            </p>
            <p>
                <input type="radio" name="color" id="green" value="#0F0">
                <label for="green">Green</label>
            </p>
            <p>
                <input type="radio" name="color" id="blue" value="#00F">
                <label for="blue">Blue</label>
            </p>
        </fieldset>
    </body>
</html>
```

## Input Validation

HTML input validation is done automatically by the browser based on special attributes on the input element. It
could partially or completely replace JavaScript input validation. This kind of validation can be circumvented by the
user via specially crafted HTTP requests, so it does not replace server-side input validation. The validation only
occurs when attempting to submit the form, so all restricted inputs must be inside a form in order for validation to
occur (unless you're using JavaScript). Keep in mind that inputs which are disabled or read-only will not trigger
validation.
Some newer input types (like email , url , tel , date and many more ) are automatically validated and do not require
your own validation constraints.

### Minimum / Maximum Length

Use the minlength and maxlength attributes to indicate length requirements. Most browsers will prevent the user
from typing more than max characters into the box, preventing them from making their entry invalid even before
they attempt submission.

![image-20210629171030772](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629171030772.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input minlength="3">
        <input maxlength="15">
        <input minlength="3" maxlength="15">
    </body>
</html>
```

### Accept File Type

For input ﬁelds of type file , it is possible to accept only certain types of ﬁles, such as videos, images, audios,
speciﬁc ﬁle extensions, or certain media types. For example:

![image-20210629171554786](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629171554786.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <form>
            <input type="text" name="name" required>
            <input type="email" name="email" required>
            <input pattern="\d*" name="number" required>

            <input type="submit" value="Publish">
            <input type="submit" value="Save">
        </form>
    </body>
</html>
```

## Color

In supporting browsers, the input element with a type attribute whose value is color creates a button-like control,
with a color equal to the value of color attribute (defaults to black if value is not speciﬁed or is an invalid
hexadecimal format).

![image-20210629171838079](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629171838079.png)

````html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <form>
            <input type="color" name="favcolor" value="#ff0000">
        </form>
    </body>
</html>
````

## Password

The input element with a type attribute whose value is password creates a single-line text ﬁeld similar to the input
type=text , except that text is not displayed as the user enters it.

![image-20210629172044774](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629172044774.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="password" name="password" placeholder="Password">
    </body>
</html>
```

## File

File inputs allow users to select a ﬁle from their local ﬁlesystem for use with the current page. If used in conjunction
with a form element, they can be used to allow users to upload ﬁles to a server (for more info see Uploading Files).
The following example allows users to use the file input to select a ﬁle from their ﬁlesystem and upload that ﬁle to
a script on the server named upload_file.php .

![image-20210629172620035](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629172620035.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <form action="index.php" method="post" ectype="multiart/form-data">
            Select file to upload:
            <input type="file" name="fileSubmission" id="fileSubmission">
            <input type="submit" value="Upload your file" name="submit">
        </form>
    </body>
</html>
```

## Button

Buttons can be used for triggering actions to occur on the page, without submitting the form. You can also use the
<button> element if you require a button that can be more easily styled or contain other elements:

![image-20210629173012721](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629173012721.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <button type="button">Button Text</button>

        <input type="button" onclick="alert('hello world!')" value="Click Me">

        <button type="button" onclick="alert('Hello world!')">Click Me</button>
    </body>
</html>
```

## Submit

A submit input creates a button which submits the form it is inside when clicked.
You can also use the <button> element if you require a submit button that can be more easily styled or contain
other elements:

![image-20210629173224399](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629173224399.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <button type="submit">
            <img src="fav-icon.jpg"> Submit
        </button>
    </body>
</html>
```

## Reset

An input of type reset creates a button which, when clicked, resets all inputs in the form it is contained in to their
default state.
Text in an input ﬁeld will be reset to blank or its default value (speciﬁed using the value attribute).
Any option(s) in a selection menu will be deselected unless they have the selected attribute.
All checkboxes and radio boxes will be deselected unless they have the checked attribute.



![image-20210629173453020](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629173453020.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="reset" value="Reset">
    </body>
</html>
```

## Hidden

A hidden input won't be visible to the user, but its value will be sent to the server when the form is submitted
nonetheless.

```html
<input type="hidden" name="inputName" value="inputValue">
```

## Tel

The input element with a type attribute whose value is tel represents a one-line plain-text edit control for entering
a telephone number.

```html
<input type="tel" value="+84000000000">
```

## Email

E-mail address can be automatically validated when submitted depending on browser support.

![image-20210629174053501](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629174053501.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <form>
            <label>E-mail:</label>
            <input type="email" name="email">
        </form>
    </body>
</html>
```

## Number

```html
<input type="number" value="0" name="quantity"
```

The Input element with a type attribute whose value is number represents a precise control for setting the element’s
value to a string representing a number.
Please note that this ﬁeld does not guarantee to have a correct number. It just allows all the symbols which could
be used in any real number, for example user will be able to enter value like e1e-,0 .

## Range

```html
<input type="range" min="" max="" step="">
```

A control for entering a number whose exact value is not important.

min       Minimum value for range      0
max      Maximum value for range      100

step      Amount to increase by on each increment.     1

## Search

Input type search is used for textual search. It will add magniﬁer symbol next to space for text on most browsers

![image-20210629174643149](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629174643149.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="search" name="googlesearch">
    </body>
</html>
```

## Image

An Image. You must use the src attribute to deﬁne the source of the image and the alt attribute to deﬁne alternative text. You can use the height and width attributes to deﬁne the size of the image in pixels.

![image-20210629174941899](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629174941899.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="image" src="fav-icon.jpg" alt="img_name" height="50px" width="50px">
    </body>
</html>
```

# Week

Dependent on browser support, a control will show for entering a week-year number and a week number with no
time zone.

![image-20210629175119879](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629175119879.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="week"/>
    </body>
</html>
```

## URL

This is used for input ﬁelds that should contain a URL address.
Depending on browser support, the url ﬁeld can be automatically validated when submitted.
Some smartphones recognize the url type, and adds ".com" to the keyboard to match url input.

![image-20210629175243733](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629175243733.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="url" name="Homapage">
    </body>
</html>
```

## Date Time-Local

Dependent on browser support, a date and time picker will pop up on screen for you to choose a date and time.

![image-20210629175439578](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629175439578.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="datetime-local">
    </body>
</html>
```

## Month

Dependent on browser support, a control will show to pick the month.

![image-20210629175744073](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629175744073.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="month">
    </body>
</html>
```

## Time

The time input marks this element as accepting a string representing a time. The format is deﬁned in RFC 3339 and
should be a partial-time such as

19:04:39
08:20:39.04

Currently, all versions of Edge, Chrome, Opera, and Chrome for Android support type="time". The newer versions
of Android Browser, speciﬁcally 4.4 and up support it. Safari for iOS oﬀers partial support, not supporting min, max,
and step attributes.

![image-20210629180009663](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629180009663.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="time">
    </body>
</html>
```

## DateTime (Global)

The input element with a type attribute whose value is "datetime" represents a control for setting the element’s
value to a string representing a global date and time (with timezone information).

### Permitted attributes:

global attributes
name
disabled
form
type
autocomplete
autofocus
list
min & max
step (ﬂoat)
readonly
required value

![image-20210629180349545](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629180349545.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <fieldset>
            <p><label>Meeting time: <input type=datetime name="meeting.start"></label></p>
        </fieldset>
    </body>
</html>
```

## Date

A date picker will pop up on screen for you to choose a date. This is not supported in Firefox or Internet Explorer.

![image-20210629180517636](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629180517636.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        </style>
    </head>
    <body>
        <input type="date">
    </body>
</html>
```

