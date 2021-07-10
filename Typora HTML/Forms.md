# Forms

## Submitting

### The Action Attribute

The action attribute deﬁnes the action to be performed when the form is submitted, which usually leads to a script
that collects the information submitted and works with it. if you leave it blank, it will send it to the same ﬁle

```html
<form action="action.php">
```

### The Method Attribute

The method attribute is used to deﬁne the HTTP method of the form which is either GET or POST.

```html
<form action="action.php" method="get">
<form action="action.php" method="post">
```

The GET method is mostly used to get data, for example to receive a post by its ID or name, or to submit a search
query. The GET method will append the form data to the URL speciﬁed in the action attribute.

```html
www.example.com/action.php?firstname=Mickey&lastname=Mouse
```

The POST method is used when submitting data to a script. The POST method does not append the form data to
the action URL but sends using the request body.

To submit the data from the form correctly, a name attribute name must be speciﬁed.
As an example let's send the value of the ﬁeld and set its name to lastname:

```html
<input type="text" name="lastname" value="Mouse">
```

### More attributes

```html
<form action="action.php" method="post" target="_blank" accept-charset="UTF-8"
enctype="application/x-www-form-urlendcoded" autocomplete="off" novalidate>
</form>
```

## Target attribute in form tag

The target attribute speciﬁes a name or a keyword that indicates where to display the response that is received
after submitting the form.
The target attribute deﬁnes a name of, or keyword for, a browsing context (e.g. tab, window, or inline frame).

From Tag with a target attribute:

```html
<form target="_blank">
```

_blank                 The response is displayed in a new window or tab

_self 				   The response is displayed in the same frame (this is default)

_parent               The response is displayed in the parent frame

_top 					The response is displayed in the full body of the window

framename 		The response is displayed in a named iframe

**Note:** The target attribute was deprecated in HTML 4.01. The target attribute is supported in HTML5.
Frames and framesets are not supported in HTML5, so the _parent, _top and framename values are now
mostly used with iframes.

## Uploading Files

Images and ﬁles can be uploaded/submitted to server by setting enctype attribute of form tag to multipart/form-
data . enctype speciﬁes how form data would be encoded while submitting to the server.

Example:

![image-20210630093124021](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630093124021.png)

```html
<form method="post" ectype="multipart/form-data" action="upload.php">
	<input type="file" name="pic">
	<input type="submit" value="Upload">
</form>
```

## Grouping a few input ﬁelds

While designing a form, you might like to group a few input ﬁelds into a group to help organise the form layout.
This can be done by using the tag . Here is an example for using it.
For each ﬁeldset, you can set a legend for the set using the tag LEGEND TEXT

**Example**

![image-20210630093803683](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630093803683.png)

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
            <fieldset>
                <legend>1st field set:</legend>
                Filed one:<br>
                <input type="text"><br>
                Field two:<br>
                <input type="text"><br>
            </fieldset><br>
            <fieldset>
                <legend>2nd filed set:</legend>
                Field three:<br>
                <input type="text"><br>
                Filed four:<br>
                <input type="text"><br>
            </fieldset><br>
            <input type="submit" value="Submit"><br>
        </form>>
    </body>
</html>
```

## Div Element

The div element in HTML is a container element that encapsulates other elements and can be used to group and
separate parts of a webpage. A div by itself does not inherently represent anything but is a powerful tool in web
design. This topic covers the purpose and applications of the div element.

## Basic usage

The <div> element usually has no speciﬁc semantic meaning by itself, simply representing a division, and is typically
used for grouping and encapsulating other elements within an HTML document and separating those from other
groups of content. As such, each <div> is best described by its contents.

![image-20210630094111452](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630094111452.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
            div{
                display:block;
            }
        </style>
    </head>
    <body>
        <div> 
            <p>Hello! This is a paragraph.</p>
        </div>
    </body>
</html>
```

Консорциум World Wide Web (W3C) настоятельно рекомендует рассматривать элемент div как
элемент крайней меры, когда никакой другой элемент не подходит. Использование более подходящих элементов
вместо элемента div обеспечивает лучшую доступность для читателей и упрощает сопровождение для авторов.

## Nesting

It is a common practice to place multiple <div> inside another <div> . This is usually referred to as "nesting"
elements and allows for further dividing elements into subsections or aid developers with CSS styling.

![image-20210630094611840](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630094611840.png)

The <div class="outer-div"> is used to group together two <div class="inner-div"> elements; each containing
a <p> element.

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
        <div class="outer-div">
            <div class="inner-div">
                <p>This is a paragraph</p>
            </div>
            <div class="inner-div">
                <p>This another paragraph</p>
            </div>
        </div>
    </body>
</html>
```

**Вложение встроенных и блочных элементов** При вложении элементов следует иметь в виду, что есть встроенные и
блочные элементы. в то время как элементы блока "добавляют разрыв строки в фоновом режиме", что означает, что другие вложенные элементы
автоматически отображается в следующей строке, встроенные элементы могут располагаться рядом друг с другом по умолчанию

**Avoid deep <div> nesting** 

Глубокие и часто используемые макеты вложенных контейнеров показывают плохой стиль программирования.
Скругленные углы или некоторые подобные функции часто создают такой HTML-код. Для большей части последнего поколения
браузеры есть аналоги CSS3. Старайтесь использовать как можно меньше HTML-элементов, чтобы увеличить контент для тегов.
коэффициент и уменьшить загрузку страницы, что приведет к лучшему ранжированию в поисковых системах.
div section Элемент не должен располагаться глубже 6 слоев.



