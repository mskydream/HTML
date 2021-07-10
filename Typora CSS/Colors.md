# Colors

## currentColor

currentColor returns the computed color value of the current element.
**Use in same element**
Here currentColor evaluates to red since the color property is set to red :

```css
div{
	color: red;
	border: 5px solid currentColor;
	box-shadow: 0 0 5px currentColor
}
```

In this case, specifying currentColor for the border is most likely redundant because omitting it should produce
identical results. Only use currentColor inside the border property within the same element if it would be
overwritten otherwise due to a more speciﬁc selector.
Since it's the computed color, the border will be green in the following example due to the second rule overriding
the ﬁrst:

```css
div{
	color:blue;
	border: 3px solid currentColor;
	color: green;
}
```

## Hexadecimal Value

**Background**

CSS colors may also be represented as a hex triplet, where the members represent the red, green and blue
components of a color. Each of these values represents a number in the range of 00 to FF , or 0 to 255 in decimal
notation. Uppercase and/or lowercase Hexadecimal values may be used (i.e. #3fc = #3FC = #33ffCC ). The browser
interprets #369 as #336699 . If that is not what you intended but rather wanted #306090 , you need to specify that
explicitly.
The total number of colors that can be represented with hex notation is 256 ^ 3 or 16,777,216.

**Syntax**

```css
color: #rrggbb;
color: #rgb;
```

Value    Description
rr           00 - FF for the amount of red
gg 		00 - FF for the amount of green
bb 		00 - FF for the amount of blue

```css
.some-class{
	color:#0000FF;
}
.also-blue{
	color: #00FF;
}
```

## rgb() Notation

```css
.some-class{
	color: rgb(0,0,255);
}
.also-blue{
    color: rgb(0%, 0%, 100%);
}
```

**Syntax**
rgb(<red>, <green>, <blue>)
Value       		Description
<red> 			an integer from 0 - 255 or percentage from 0 - 100%
<green> 		an integer from 0 - 255 or percentage from 0 - 100%
<blue> 		  an integer from 0 - 255 or percentage from 0 - 100%

## rgba() Notation

Similar to rgb() notation, but with an additional alpha (opacity) value.

```css
.red{
	color:rgba(255,0,0,1);
}
.red-50p{
	color:rgba(255,0,0, .5);
}
```

**Syntax**
rgba(<red>, <green>, <blue>, <alpha>);
Value			Description
<red>  		an integer from 0 - 255 or percentage from 0 - 100%
<green> 	 an integer from 0 - 255 or percentage from 0 - 100%
<blue> 	   an integer from 0 - 255 or percentage from 0 - 100%
<alpha>      a number from 0 - 1, where 0.0 is fully transparent and 1.0 is fully opaque

## hsl() Notation

HSL stands for hue ("which color"), saturation ("how much color") and lightness ("how much white").
Hue is represented as an angle from 0° to 360° (without units), while saturation and lightness are represented as
percentages.

```css
p{
	color:hsl(240,100%,50%);
}
```

![image-20210703101846263](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703101846263.png)

**Syntax**

```css
color: hsl(<hue>, <saturation>%, <lightness>%);
```

## hsla() Notation

Similar to hsl() notation, but with an added alpha (opacity) value.

```css
hsla(240, 100%, 50%, 0)
hsla(240, 100%, 50%, 0.5)
hsla(240, 100%, 50%, 1)
```

