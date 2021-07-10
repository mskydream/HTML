# Character Entities

## Character Entities in HTML

Many symbols and special characters are required while developing a web page in html, but as we know that
sometimes the use of characters directly may interfere with the actual html code which have certain characters
reserved and also certain characters being not available on keyboard. Thus, to avoid the conﬂict and at same time
to be able to use diﬀerent symbols in our code w3 org provides us with 'Character Entities'.
Character Entities are predeﬁned with 'Entity Name' - &entity_name; and 'Entity Number' - &entity_number; so we
need to use either of the two for the required symbol to be rendered on our page.
The list of few Character Entities can be found at https://dev.w3.org/html5/html-author/charref
A simple example with the use of character entity for 'magnifying glass' :

![image-20210630162217664](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630162217664.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <input type="text" placeholder="&#128269; Search">
        </body>
    </html>
```

## Common Special Characters

Some character may be reserved for HTML and cannot be used directly as it may obstruct the actual HTML codes.
For example, trying to display the left and right angle brackets ( <> ) in the source code may cause unexpected
results in the output. Similarly, white spaces as written in the source code may not display as expected in the
output HTML. Some, like ☎, are not available in the ASCII character set.
For this purpose, character entities are created. These are of the form &entity_name; or &entity_number; . The
following are some of the available HTML entities.

![image-20210630162304913](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630162304913.png)

