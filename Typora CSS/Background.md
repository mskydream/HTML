# Background 

With CSS you can set colors, gradients, and images as the background of an element.
It is possible to specify various combinations of images, colors, and gradients, and adjust the size, positioning, and
repetition (among others) of these.

## Background Color

The background-color property sets the background color of an element using a color value or through keywords,
such as transparent , inherit or initial .
                    transparent, speciﬁes that the background color should be transparent. This is default.
                    inherit, inherits this property from its parent element.
                    initial, sets this property to its default value.
This can be applied to all elements, and ::first-letter / ::first-line pseudo-elements.
Colors in CSS can be speciﬁed by diﬀerent methods.

**Color names**

```css
div{
	background-color:red;
}
```

```html
<div>This will have a red bacground</div>
```

**Hex color codes**

Hex code is used to denote RGB components of a color in base-16 hexadecimal notation. #ﬀ0000, for example, is
bright red, where the red component of the color is 256 bits (ﬀ) and the corresponding green and blue portions of
the color is 0 (00).
If both values in each of the three RGB pairings (R, G, and B) are the same, then the color code can be shortened
into three characters (the ﬁrst digit of each pairing). #ff0000 can be shortened to #f00 , and #ffffff can be
shortened to #fff .
Hex notation is case-insensitive.

```css
body{
	background-color:#de1205;
}
.main{
	background-color:#00f;
}
```

**RGB / RGBa**

Another way to declare a color is to use RGB or RGBa.
RGB stands for Red, Green and Blue, and requires of three separate values between 0 and 255, put between
brackets, that correspond with the decimal color values for respectively red, green and blue.
RGBa allows you to add an additional alpha parameter between 0.0 and 1.0 to deﬁne opacity.

```css
header{
	background-color:rgb(0,0,0);/* black */
}
footer{
	background-color: rgba(0,0,0,0.5);/* black with 50% opacity */
}
```

**HSL / HSLa**

Another way to declare a color is to use HSL or HSLa and is similar to RGB and RGBa.
HSL stands for hue, saturation, and lightness, and is also often called HLS:
Hue is a degree on the color wheel (from 0 to 360).
Saturation is a percentage between 0% and 100%.
Lightness is also a percentage between 0% and 100%.
HSLa allows you to add an additional alpha parameter between 0.0 and 1.0 to deﬁne opacity.

```css
li a{
	background-color: hsl(120, 100%,50%);/* green */
}
#p1{
	background-color:hsla(120,100%,50%, .3); /* green with 30% opacity */
}
```

##  Background Size

The background-size property enables one to control the scaling of the background-image . It takes up to two
values, which determine the scale/size of the resulting image in vertical and and horizontal direction. If the property
is missing, its deemed auto in both width and height .
auto will keep the image's aspect ratio, if it can be determined. The height is optional and can be considered auto .
Therefore, on a 256 px × 256 px image, all the following background-size settings would yield an image with height
and width of 50 px:

```css
background-size:50px;
background-size:50px auto;
background-size: auto 50px;
background-size: 50px;

```

One can also use percentage values to scale the image with respect of the element. The following example would
yield a 200 px × 133 px drawn image:

```css
#withbackground{
	background-image:url(to/some/background.png);
	background-size: 100% 66%;
	with:200px;
	height:200px;
	padding:0;
	margin:0;
}
```

Eggsplanation for contain and cover

Contain не полное cover  полное фото

![image-20210701150217057](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701150217057.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                div > div{
                    background-image: url(http://i.stack.imgur.com/r5CAq.jpg);
                    background-repeat: no-repeat;
                    background-position: center center;
                    background-color:#ccc;
                    border: 1px solid;
                    width: 20em;
                    height: 10em;
                }
                div.contain{
                    background-size: contain;
                }
                div.cover{
                    background-size: cover;
                }

                div > div{
                    margin: 0 1ex 1ex 0;
                }
                div + div{
                    clear: both;
                    border-top: 1px dashed silver;
                    padding-top: 1ex;
                }
                div > div::after{
                    background-color: #000;
                    color: #fefefe;
                    margin: 1ex;
                    padding: 1ex;
                    opacity: 0.8;
                    display: block;
                    width: 10ex;
                    font-size: 0.7em;
                    content: attr(class);
                }
            </style>
        </head>
        <body>
            <div>
                <div class="contain"></div>
                <p>Note the grey background. The image does not cover the whole region, but it's fully 
                    <em>contined</em>.
                </p>
            </div>
            <div>
                <div class="cover"></div>
                <p>Note the ducks/geese at the bottom of the image. Most of the water is cut, as well as a part
                    of the sky. You don't see the complete image anymore, but neither do you see any background color;
                    the image <em>covers</em> all of the <code>&lt;div&gt;</code>.
                </p>
            </div>
        </body>
    </html>
```

## The background-origin property

The background-origin property speciﬁes where the background image is positioned.
Note: If the background-attachment property is set to fixed , this property has no eﬀect.
Default value: padding-box

![image-20210701161246939](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701161246939.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>CSS</title>
            <style>
                .example{
                    width: 300px;
                    border: 20px solid black;
                    padding: 50px;
                    background-repeat:no-repeat;
                }
                .example{}
                .example2{background-orgin: border-box;}
                .example3{background-origin: content-box;}
            </style>
        </head>
        <body>
            <p>No background-origin (padding-box is default):</p>
            <div class="example example1">
                <h2>Lorem Ipsum Dolor</h2>
                <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
                    euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
                </p>
                <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis
                    nisl ut aliquip ex ea commodo consequat.
                </p>
            </div>
            <p>background-origin: border-box:</p>
            <div class="example example2">
                <h2>Lorem Ipsum Dolor</h2>
                <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod
                    tincidunt ut laoreet dolore magna aliquam erat volutpat.
                </p>
                <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis
                    nisl ut aliquip ex ea commodo consequat.
                </p>
            </div>

            <p>background-origin: content-box:</p>
            <div class="example example3">
                <h2>Lorem Ipsum Dolor</h2>
                <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
                    euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
                </p>
                <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis
                    nisl ut aliquip ex ea commodo consequat.
                </p>
            </div>
        </body>
    </html>
```

## Background Clip

Deﬁnition and Usage: The background-clip property speciﬁes the painting area of the background.

![image-20210701163635977](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701163635977.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .example{
                width: 300px;
                border: 20px solid black;
                padding: 50px;
                background: url(https://static.pexels.com/photos/6440/magazines-desk-work-workspace-medium.jpg);
                background-repeat: no-repeat;
            }
        </style>
    </head>
    <body>
        <p>No background-origin (padding-box is default):</p>
        <div class="example example1">
            <h2>Lorem Ipsum Dolor</h2>
            <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
                euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
            </p>
            <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis
                nisl ut aliquip ex ea commodo consequat.
            </p>
        </div>

        <p>background-origin: border-box:</p>
        <div class="example example1">
            <h2>Lorem Ipsum Dolor</h2>
            <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
                euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
            </p>
            <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis
                nisl ut aliquip ex ea commodo consequat.
            </p>
        </div>

        <p>background-origin: content-box:</p>
        <div class="example example1">
            <h2>Lorem Ipsum Dolor</h2>
            <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh
                euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
            </p>
            <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis
                nisl ut aliquip ex ea commodo consequat.
            </p>
        </div>            
    </body>
</html>
```





