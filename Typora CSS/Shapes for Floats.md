# Shapes for Floats

# Shape Outside with Basic Shape – circle()

With the shape-outside CSS property one can deﬁne shape values for the ﬂoat area so that the inline content
wraps around the shape instead of the ﬂoat's box.

![image-20210703170917074](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703170917074.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                img:nth-of-type(1){
                    shape-outside: circe(80px at 50% 50%);
                    float: left;
                    width: 200px;
                }
                img:nth-of-type(2){
                    shape-outside: circle(80px at 50% 50%);
                    float: right;
                    width: 200px;
                }
                p{
                    text-align: center;
                    line-height: 30px;
                }
            </style>
        </head>
        <body>
            <img src="http://images.clipartpanda.com/circle-clip-art-circlergb.jpg">
            <img src="http://images.clipartpanda.com/circle-clip-art-circlergb.jpg">
            <p>Some paragraph whose text content is required to be wrapped such that it follows the curve of
            the circle on either side. And then there is some filler text just to make the text long enough.
            Lorem Ipsum Dolor Sit Amet....</p>
        </body>
    </html>
```

​	