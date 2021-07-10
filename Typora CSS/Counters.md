# Counters

## Applying roman numerals styling to the counter output

![image-20210704093625569](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704093625569.png)

```css
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            body{
                counter-reset:item-counter;
            }  
            .item{
                counter-reset: item-counter;
            }
            .item:before{
                content: counter(item-counter, upper-roman)
            }
        </style>
    </head>
    <body>
        <div class='item'>Item No: 1</div>
        <div class="item">Item No: 2</div>
        <div class="item">Item: No: 3</div>
    </body>
</html>
```

In the above example, the counter's output would be displayed as I, II, III (roman numbers) instead of the usual 1, 2,
3 as the developer has explicitly speciﬁed the counter's style.

## Section 35.2: Number each item using CSS Counter

![image-20210704094645995](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704094645995.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            body{
                counter-reset: item-counter;
            }
            .item{
                counter-increment: item-counter;
            }
            .item-header:before{
                content: counter(item-counter) ". ";
            }
            .item{
                border: 1px solid;
                height: 100px;
                margin-bottom: 10px;
            }
            .item-header{
                border-bottom: 1px solid;
                height: 40px;
                line-height: 40px;
                padding:5px;
            }
            .item-content{
                padding: 8px;
            }
        </style>
    </head>
    <body>
        <div class="item">
            <div class="item-header">Item 1 Header</div>
            <div class="item-content">Lorem Ipsum Dolor Sit Amet...</div>
        </div>
        <div class="item">
            <div class="item-header">Item 2 Header</div>
            <div class="item-content">Lorem Ipsum Dolor Sit Amet...</div>
        </div>
        <div class="item">
            <div class="item-header">Item 3 Header</div>
            <div class="item-content">Lorem Ipsum Dolor Sit Amet...</div>
        </div>
    </body>
</html>
```

## Implementing multi-level numbering using CSS counters

![image-20210704095150437](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210704095150437.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            ul{
                list-style: none;
                counter-reset: list-item-number;
            }
            li{
                counter-increment: list-item-number;
            }
            li:before{
                content: counters(list-item-number, ".") " ";
            }
        </style>
    </head>
    <body>
        <ul>
            <li>Level 1
                <ul>
                    <li>Level 1.1
                        <ul>
                            <li>Level 1.1.1</li>
                        </ul>
                    </li>
                </ul>
            </li>
            <li>Level 2
                <ul>
                    <li>Level 2.1
                        <ul>
                            <li>Level 2.1.1</li>
                            <li>Level 2.1.2</li>
                        </ul>
                    </li>
                </ul>
            </li>
        </ul>
    </body>
</html>
```



