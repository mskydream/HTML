# Animations

## Animations with keyframes 

For multi-stage CSS animations, you can create CSS @keyframes. Keyframes allow you to define multiple animation points, called a keyframe, to define more complex animations.

## Animations with the transition property

Useful for simple animations, the CSS transition property allows number-based CSS properties to animate between states.

![image-20210703151208531](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703151208531.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .Example{
                height: 100px;
                background: #fff;
            }
            .Example:hover{
                height: 120px;
                background: #f00;
            }
        </style>
    </head>
    <body>
        <div class="Example">
            .Example DIV
        </div>
    </body>
</html>
```

