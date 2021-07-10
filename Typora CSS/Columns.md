# Columns

## Simple Example (column-count)
The CSS multi-column layout makes it easy to create multiple columns of text.

![image-20210704113630543](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704113630543.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            #multi-columns{
                -moz-column-count: 2;
                -webkit-column-count: 2;
                column-count: 2;
            }
        </style>
    </head>
    <body>
        <div id="multi-columns">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod 
            tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nosrud 
            exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in 
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in 
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nullla pariatur. Exepteur sint occaecat 
            cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum
        </div>
    </body>
</html>
```

## Column Width
The column-width property sets the minimum column width. If column-count is not deﬁned the browser will make
as many columns as ﬁt in the available width.

![image-20210704113818608](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704113818608.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            #multi-columns{
                -moz-column-width: 100px;
                -webkit-column-width: 100px;
                column-count: 100px;
            }
        </style>
    </head>
    <body>
        <div id="multi-columns">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod 
            tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nosrud 
            exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in 
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Duis aute irure dolor in 
            reprehenderit in voluptate velit esse cillum dolore eu fugiat nullla pariatur. Exepteur sint occaecat 
            cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum
        </div>
    </body>
</html>
```

