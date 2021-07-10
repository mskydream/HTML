# Output Element

## Output Element Using For and Form Attributes

The following demo features an <output> element's use of the [for] and [form] attributes. Keep in mind, <output>
needs JavaScript in order to function. Inline JavaScript is commonly used in forms as this example demonstrates.
Although the <input> elements are type="number" , their value s are not numbers, they are text. So if you require
the value s to be calculated, you must convert each value into a number using methods such as: parseInt() ,
parseFloat() , Number() , etc.

![image-20210630110527591](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630110527591.png)

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
        <!-- form1 will collect the values of in1 and in2 on 'input' evet.-->
        <form id="form1" name="form1" oninput="out1.value = parseInt(in1.value, 10) + 
        parseInt(in2.value,10)">
        <fieldset>
            <legend>Output Example</legend>
            <input type="number" id="in1" name="in1" value="0"><br/>
            +
            <input type="number" id="in2" name="in2" value="0">
        </fieldset>
        </form>
        <!--[for] attribute enables out1 to display calculations for in1 and in2.-->
        <!--[form] atttibute designates form1 as the form owner of out1 even if it isn't a descentant.-->
        <output name="out1" for="in1 in2" form="form1">0</output>
    </body>
</html>
```

