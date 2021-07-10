# Opacity

## Opacity Property

An element's opacity can be set using the opacity property. Values can be anywhere from 0.0 (transparent) to 1.0
(opaque).

**Example Usage**

```html
<div style="opacity:0.8;">
	This is a partially transparent element
</div>
```

Property Value 			Transparency
opacity:						 1.0; Opaque
opacity: 						0.75; 25% transparent (75% Opaque)
opacity: 						0.5; 50% transparent (50% Opaque)
opacity:						 0.25; 75% transparent (25% Opaque)
opacity:						 0.0; Transparent

## IE Compatibility for `opacity`
To use opacity in all versions of IE, the order is:

```css
.transparent-element{
	-ms-filter:"progid:DXImageTransform.Microsoft.Alpha(Opacity=60)";
	filter: alpha(opacity=60);
	opacity:0.6;
}
```



