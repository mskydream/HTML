# Structure and Formatting of a CSS Rule

## Property Lists

Some properties can take multiple values, collectively known as a property list.

```css
span{
	text-shadow:yellow 0 0 3px, green 4px 4px 10px;
}
span{
	text-shadow:
		yellow 0 0 3px,
		green 4px 4px 10px;
}
```

## Multiple Selectors

When you group CSS selectors, you apply the same styles to several diﬀerent elements without repeating the styles
in your style sheet. Use a comma to separate multiple grouped selectors.

```css
div, p{color:blue}
```

So the blue color applies to all <div> elements and all <p> elements. Without the comma only <p> elements that are
a child of a <div> would be red.
This also applies to all types of selectors.

```css
p, .blue, #first, div span{color: blue}
```

## Rules, Selectors, and Declaration Blocks

A CSS rule consists of a selector (e.g. h1 ) and declaration block ( {} ).

```css
h1{}
```



