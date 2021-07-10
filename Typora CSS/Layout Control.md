# Layout Control

## The display property

The display CSS property is fundamental for controlling the layout and ﬂow of an HTML document. Most elements
have a default display value of either block or inline (though some elements have other default values).
**Inline**
An inline element occupies only as much width as necessary. It stacks horizontally with other elements of the
same type and may not contain other non-inline elements.

```html
<span>This is some <b>bolder</b> text!</span>
```

As demonstrated above, two inline elements, <span> and <b> , are in-line (hence the name) and do not break the
ﬂow of the text.

**Block**

A block element occupies the maximum available width of its' parent element. It starts with a new line and, in
contrast to inline elements, it does not restrict the type of elements it may contain.

```html
<div>Hello world!</div><div>This is an example!</div>
```

The div element is block-level by default, and as shown above, the two block elements are vertically stacked and,
unlike the inline elements, the ﬂow of the text breaks.

