# Label Element

for       	Reference to the target ID Element. I.e: for="surname"

form		HTML5, [Obsolete] Reference to the form containing the Target Element. Label elements are expected
				within a <form> Element. If the form="someFormId" is provided this allows you to place the Label
				anywhere in the document.

## About Label

The <label> element is used to reference a form action element.
In the scope of User Interface it's used to ease the target / selection of elements like Type radio or checkbox .

**<label> as wrapper**

It can enclose the desired action element

```html
<label type="checkbox" name="Cats">
	I like cats
</label>
```

**<label> as reference**

Using the for attribute you don't have to place the control element as descendant of label - but the for value must
match it's ID

![image-20210630104408178](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630104408178.png)

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
        <input id="cats" type="checkbox" name="Cats">
        <label for="cats">I like Cats!</label>
    </body>
</html>
```

## Basic Use

Simple form with labels...

![image-20210630105318385](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630105318385.png)

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
        <form id="my-form" action="/login" method="POST">
            <input id="username" type="text" name="username">
            <label for="pass">Password:</label>
            <input type="pass" type="password" name="pass">

            <input type="submit" name="submit">
        </form>

        <label for="username" form="my-form">Usename:</label>
    </body>
</html>
```



