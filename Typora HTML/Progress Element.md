#  Progress Element

max----------------How much work the task requires in total
value--------------- How much of the work has been accomplished already
position -----------This attribute returns the current position of the <progress> element
labels ----------This attribute returns a list of <progress> element labels (if any)

## Progress

The <progress> element is new in HTML5 and is used to represent the progress of a task

```html
<progress value="22" max="100"></progress>
```

**This creates a bar filled 22%**

## HTML Fallback

For browsers that do not support the progress element, you can use this as a workaround.

![image-20210630125918246](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630125918246.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
            #videobg{
                background:url(shortcut.jpg);
                background-size: cover;
            }
        </style>
    </head>
    <body>
        <progress max="100">
            <div class = "progress-bar">
                <span style="width: 20%;">Progress: 20%</span>
            </div>
        </progress>
    </body>
</html>
```

Browsers that support the progress tag will ignore the div nested inside. Legacy browsers which cannot identify the
progress tag will render the div instead.