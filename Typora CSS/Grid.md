# Grid

Grid layout is a new and powerful CSS layout system that allows to divide a web page content into rows and columns in an easy way.

## Basic Example

![image-20210703150123819](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703150123819.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .container{
                display:grid;
                grid-columns: 50px 50px 50px;
                grid-rows: 50px 50px;
            }
            .container .item1{
                grid-column: 1;
                grid-row: 1;
            }
            .container .item2{
                grid-column: 2;
                grid-row: 1;
            }
            .container .item3{
                grid-column: 1;
                grid-row: 2;
            }
            .container .item4{
                grid-row: 2;
                grid-column: 2;
            }
        </style>
    </head>
    <body>
        <section class="container">
            <div class="item1">item1</div>
            <div class="item2">item2</div>
            <div class="item3">item</div>
            <div class="item4">item4</div>
        </section>
    </body>
</html>
```

