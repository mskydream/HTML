# Multiple columns
CSS allows to deﬁne that element contents wrap into multiple columns with gaps and rules between them.

## Create Multiple Columns

![image-20210704115149877](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704115149877.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            #multi-columns{
                -moz-column-count: 3;
                -webkit-column-count: 3;
                column-count: ;
            }
        </style>
    </head>
    <body>
        <div id="multi-columns">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod 
            tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nosrud 
            exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis uatem vel eum iriure dolor in 
            hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero 
            eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te 
            feugait nulla facilisi. Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming 
            id quot mazim placerat facer possim assum.
        </div>
    </body>
</html>
```

## Basic example
Consider the following HTML markup:

![image-20210704115645215](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704115645215.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            section{
                columns:3;
                column-gap: 40px;
                column-rule: 2px solid gray;
            }
        </style>
    </head>
    <body>
        <section>
            <p>Lorem ipsum dolor sit amet, consetetur adipscing elitr, sed diam nonumy eirmod tempor 
                invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam 
                et justo duo dolores et ea rebum.
            </p>
            <p>Lorem ipsum dolor sit amet, consetetur adipscing elitr, sed diam nonumy eirmod tempor 
                invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam 
                et justo duo dolores et ea rebum.
            </p>
            <p>Lorem ipsum dolor sit amet, consetetur adipscing elitr, sed diam nonumy eirmod tempor 
                invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam 
                et justo duo dolores et ea rebum.
            </p>
        </section>
    </body>
</html>
```

