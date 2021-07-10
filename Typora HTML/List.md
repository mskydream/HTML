# List

HTML oﬀers three ways for specifying lists: ordered lists, unordered lists, and description lists. Ordered lists use
ordinal sequences to indicate the order of list elements, unordered lists use a deﬁned symbol such as a bullet to list
elements in no designated order, and description lists use indents to list elements with their children. This topic
explains the implementation and combination of these lists in HTML markup.

## Ordered List

An ordered list can be created with the <ol> tag and each list item can be created with the <li> tag as in the
example below:

![image-20210629135257688](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629135257688.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <ol>
            <li>Item</li>
            <li>Another Item</li>
            <li>Yet Another Item</li>
        </ol>
    </body>
</html>
```

### Manually changing the numbers

There are a couple of ways you can play with which numbers appear on the list items in an ordered list. The ﬁrst
way is to set a starting number, using the start attribute. The list will start at this deﬁned number, and continue
incrementing by one as usual.

![image-20210629135556265](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629135556265.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <ol start=3>
            <li>Item</li>
            <li>Some Other Item</li>
            <li>Yet Another Item</li>
        </ol>
    </body>
</html>
```

### So the example above will produce a list that follows the numbering pattern of 5, 6, 4, 5, 6 - starting again at a number lower than the previous and duplicating the number 6 in the list.

![image-20210629140010986](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629140010986.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <ol start="5">
            <li>Item</li>
            <li>Some Other Item</li>
            <li value="4">A reset Item</li>
            <li>Another Item</li>
            <li>Yet Another Item</li>
        </ol>
    </body>
</html>
```

### You can reverse the numbering by adding reversed in your ol element:

![image-20210629140400148](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629140400148.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <ol reversed>
            <li>Item</li>
            <li>Some Other Item</li>
            <li value="4">A Reset Item</li>
            <li>Another Item</li>
            <li>Yet Another Item</li>
        </ol>
    </body>
</html>
```

## Changing the type of numeral

You can easily change the type of numeral shown in the list item marker by using the type attribute

1 Default value - Decimal numbers 1,2,3,4
a Alphabetically ordered (lowercase) a,b,c,d
A Alphabetically ordered (uppercase) A,B,C,D
i Roman Numerals (lowercase) i,ii,iii,iv
I Roman Numerals (uppercase) I,II,III,IV

![image-20210629140718044](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629140718044.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <ol type="I">
            <li>Item</li>
            <li>Some Other Item</li>
            <li value="4">A Reset Item</li>
            <li>Another Item</li>
            <li>Yet Another Item</li>
        </ol>
    </body>
</html>
```

# Unordered List

An unordered list can be created with the <ul> tag and each list item can be created with the <li> tag as shown by
the example below:

![image-20210629140932381](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629140932381.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <ul>
            <li>Item</li>
            <li>Another Item</li>
            <li>Yet Another Item</li>
        </ul>
    </body>
</html>
```

# Nested lists

You can nest lists to represent sub-items of a list item.

![image-20210629141203961](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629141203961.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <ul>
            <li>item 1</li>
            <li>
                <ul>
                    <li>sub-item 2.1</li>
                    <li>sub-item 2.2</li>
                </ul>
            </li>
            <li>item 3</li>
        </ul>
    </body>
</html>
```



#  Description List

A description list (or deﬁnition list, as it was called before HTML5) can be created with the dl element. It consists of name-value groups, where the name is given in the dt element, and the value is given in the dd element.

![image-20210629141701639](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629141701639.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <dl>
            <dt>name 1</dt>
            <dd>value for 1</dd>
            <dt>name 2</dt>
            <dd>value for 2</dd>
        </dl>
    </body>
</html>
```

A name-value group can have more than one name and/or more than one value (which represent alternatives):

![image-20210629142017418](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629142017418.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Hello!</title>
    </head>
    <body>
        <dl> 
            <dt>name 1</dt>
            <dt>name 2</dt>
            <dd>value for 1 and 2</dd>
             <dt>name 3</dt>
             <dd>value for 3</dd>
             <dd>value for 3</dd>
        </dl>
    </body>
</html>
```



