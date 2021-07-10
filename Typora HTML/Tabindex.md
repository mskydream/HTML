# Tabindex

### Add an element to the tabbing order

![image-20210630160656583](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630160656583.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <div tabindex="0">Sime button</div>
    </body>
</html>
```

### Remove an element from the tabbing order

![image-20210630160831438](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630160831438.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <button tabindex="-1">This button will not be reachable by tab</button>
    </body>
</html>
```

### Deﬁne a custom tabbing order (not recommended)

![image-20210630161005929](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630161005929.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
    </head>
    <body>
        <div tabindex="2">Second</div>
        <div tabindex="1">First</div>
    </body>
</html>
```

Положительные значения вставят элемент в позицию табуляции соответствующего значения. Элементы без
предпочтение (например, tabindex = "0" или собственные элементы, такие как button и a) будут добавлены после элементов с
предпочтение.
Положительные значения не рекомендуются, поскольку они нарушают ожидаемое поведение табуляции и могут запутать людей.
кто полагается на программы чтения с экрана. Попытайтесь создать естественный порядок, изменив структуру DOM.