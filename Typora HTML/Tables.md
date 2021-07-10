# Tables

### The HTML <table> element allows web authors to display tabular data (such as text, images, links, other tables, etc.) in a two dimensional table with rows and columns of cells.

# Simple Table

This will render a <table> consisting of three total rows ( <tr> ): one row of header cells ( <th> ) and two rows of
content cells ( <td> ). <th> elements are tabular headers and <td> elements are tabular data. You can put whatever
you want inside a <td> or <th> .

![image-20210629143106567](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629143106567.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
    </head>
    <body>
        <table>
            <tr>
                <th>Heading 1/Column 1</th>
                <th>Heading 2/Column 2</th>
            </tr>
            <tr>
                <td>Row 1 Data Column 1</td>
                <td>Row 1 Data Column 2</td>
            </tr>
            <tr>
                <td>Row 2 Data Column 1</td>
                <td>Row 2 Data Column 2</td>
            </tr>
        </table>
    </body>
</html>
```

# Spanning columns or rows

Table cells can span multiple columns or rows using the colspan and rowspan attributes. These attributes can be
applied to <th> and <td> elements.

![image-20210629143750587](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629143750587.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
    </head>
    <body>
        <table>
            <tr>
                <td>row 1 col 1</td>
                <td>row 1 col 2</td>
                <td>row 1 col 3</td>
            </tr>
            <tr>
                <td colspan="3">This second row spans all three columns</td>
            </tr>
            <tr>
                <td rowspan="2">This cell spans two rows</td>
                <td>row 3 col 2</td>
                <td>row 3 col 3</td>
            </tr>
            <tr>
                <td>row 4 col2</td>
                <td>row 4 col 3</td>
            </tr>
        </table>
    </body>
</html>
```

# Table with thead, tbody, tfoot, and caption

HTML also provides the tables with the <thead> , <tbody> , <tfoot> , and <caption> elements. These additional
elements are useful for adding semantic value to your tables and for providing a place for separate CSS styling.When printing out a table that doesn't ﬁt onto one (paper) page, most browsers repeat the contents of <thead> on
every page.
There's a speciﬁc order that must be adhered to, and we should be aware that not every element falls into place as
one would expect. The following example demonstrates how our 4 elements should be placed.

![image-20210629144853850](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629144853850.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
    </head>
    <body>
        <table>
            <caption>Table Title</caption> <!--| caption is the first child of table |-->
            <thead>
                <tr>
                    <th>Header content 1</th>
                    <th>Header content 2</th>
                </tr>
            </thead>

            <tbody><!--| tbody is after thead | -->
                <tr>
                    <td>Body content 1</td>
                    <td>Body content 2</td>
                </tr>
            </tbody>

            <tfoot>
                <tr>
                    <td>Footer content 1</td>
                    <td>Footer content 2</td>
                </tr>
            </tfoot>
        </table>
    </body>
</html>
```

# Heading scope

This can be improved for accessibility by the use of the scope attribute. The above example would be amended as
follows:

![image-20210629145411585](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629145411585.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
    </head>
    <body>
        <table>
            <thead>
                <tr>
                    <td></td>
                    <th scope="col">Column Heading 1</th>
                    <th scope="col">Column Heading 2</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <th scope="row">Row Heading 1</th>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <th scope="row">Row Heading 1</th>
                    <td></td>
                    <td></td>
                </tr>
            </tbody>
        </table>
    </body>
</html>
```



