# Media Queries

## Terminology and Structure

Media queries allow one to apply CSS rules based on the type of device / media (e.g. screen, print or handheld)
called media type, additional aspects of the device are described with media features such as the availability of
color or viewport dimensions.

**General Structure of a Media Query**

```css
@media[...]
```

**A Media Query containing a Media Type**

```css
@media print{
}
```

**A Media Query containing a Media Type and a Media Feature**

```css
@media screen and (max-width: 600px){
}
```

**A Media Query containing a Media Feature (and an implicit Media Type of "all")**

```css
@media(orientation: portrait){
}
```

## Basic Example

```css
@media screen and(min-width:720px){
	body{
		background-color:skyblue;
	}
}
```



The above media query speciﬁes two conditions:

____The page must be viewed on a normal screen (not a printed page, projector, etc).

____The width of the user's view port must be at least 720 pixels.

If these conditions are met, the styles inside the media query will be active, and the background color of the page
will be sky blue.
Media queries are applied dynamically. If on page load the conditions speciﬁed in the media query are met, the CSS
will be applied, but will be immediately disabled should the conditions cease to be met. Conversely, if the
conditions are initially not met, the CSS will not be applied until the speciﬁed conditions are met.
In our example, if the user's view port width is initially greater than 720 pixels, but the user shrinks the browser's
width, the background color will cease to be sky blue as soon as the user has resized the view port to less than 720
pixels in width.

## mediatype

Media queries have an optional mediatype parameter. This parameter is placed directly after the @media
declaration ( @media mediatype ), for example:

```css
@media print{
	html{
		background-color:white;
	}
}
```

The above CSS code will give the DOM HTML element a white background color when being printed.
The mediatype parameter has an optional not or only preﬁx that will apply the styles to everything except the
speciﬁed mediatype or only the speciﬁed media type, respectively. For example, the following code example will
apply the style to every media type except print .

```css
@meida not print{
	html{
		background-color:green;
	}
}
```

And the same way, for just showing it only on the screen, this can be used:

```css
@media only screen{
	.fadeInEffects{
		display:block;
	}
}
```

## Media Queries for Retina and Non Retina Screens
Although this works only for WebKit based browsers, this is helpful:

```css
@media screen
	and (min-width: 1200px)
	and(max-width: 1600px)
	and (-webkit-min-deice-pixel-ratio: 1){
}
@media screen
    and(min-width: 1200px)
    and(min-width: 1600px)
    and(-webkit-min-device-pixel-ratio: 2)
    and(min-resolution: 192dpi){
}
```

**Background Information**

There are two types of pixels in the display. One is the logical pixels and the other is the physical pixels. Mostly, the
physical pixels always stay the same, because it is the same for all the display devices. The logical pixels change
based on the resolution of the devices to display higher quality pixels. The device pixel ratio is the ratio between
physical pixels and logical pixels. For instance, the MacBook Pro Retina, iPhone 4 and above report a device pixel
ratio of 2, because the physical linear resolution is double the logical resolution.
The reason why this works only with WebKit based browsers is because of:

​		The vendor preﬁx -webkit- before the rule.
​		This hasn't been implemented in engines other than WebKit and Blink.

## Using Media Queries to Target Dierent Screen Sizes

Often times, responsive web design involves media queries, which are CSS blocks that are only executed if a
condition is satisﬁed. This is useful for responsive web design because you can use media queries to specify
diﬀerent CSS styles for the mobile version of your website versus the desktop version.

```css
@media only screen and (min-width: 300px) and (max-width: 767px){
	.site-title{
		font-size:80%
	}
}
@media only screen and (min-width:768px) and (max-width: 1023){
	.site-title{
		font-size:90%;
	}
}
@media only screen and(min-width:1024px){
	.site-title{
		font-size:120%;
	}
}
```

 ## Use on link tag

```css
<link rel="stylesheet" media="min-width: 600px href="example.css">
```

This stylesheet is still downloaded but is applied only on devices with screen width larger than 600px.