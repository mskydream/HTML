# Cursor Styling

## Changing cursor type

```css
cursor:value;
```

![image-20210703164414819](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703164414819.png)

Value  			Description
none			 No cursor is rendered for the element
auto 			 Default. The browser sets a cursor
help 			 The cursor indicates that help is available
wait 			 The cursor indicates that the program is busy
move 		  The cursor indicates something is to be moved
pointer 		The cursor is a pointer and indicates a link

## caret-color
The caret-color CSS property speciﬁes the color of the caret, the visible indicator of the insertion point in an
element where text and other content is inserted by the user's typing or editing.

![image-20210703164724168](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703164724168.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            #example{
                caret-color:red;
            }
        </style>
    </head>
    <body>
        <input id="example">
    </body>
</html>
```

