# Inline-Block Layout

## Justiﬁed navigation bar
The horizontally justiﬁed navigation (menu) bar has some number of items that should be justiﬁed. The ﬁrst (left)
item has no left margin within the container, the last (right) item has no right margin within the container. The
distance between items is equal, independent on the individual item width.

![image-20210704130005671](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704130005671.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            nav{
                width: 100%;
                line-height: 1.4em;
            }
            ul{
                list-style: none;
                display: block;
                width: 100%;
                margin:0;
                padding: 0;
                text-align: justify;
                margin-bottom: -1.4em;
            }
            ul:after{
                content:"";
                display: inline-block;
                width: 100%;
            }
            li{
                display:inline-block;
            }
        </style>
    </head>
    <body>
        <nav>
            <ul>
                <li>abc</li>
                <li>abcdefghijkl</li>
                <li>abcdef</li>
            </ul>
        </nav>
    </body>
</html>
```

