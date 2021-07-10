# Data Attributes

HTML5 data-* attributes provide a convenient way to store data in HTML elements. The stored data can be read or
modiﬁed using JavaScript

## Favicon

Use the mime-type image/png for PNG ﬁles and image/x-icon for icon ( *.ico ) ﬁles. For the diﬀerence, see this SO
question.
A ﬁle named favicon.ico at the root of your website will typically be loaded and applied automatically, without the
need for a <link> tag. If this ﬁle ever changes, browsers can be slow and stubborn about updating their cache.

![image-20210629153018534](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210629153018534.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>Table</title>
        <link rel="icon" type="image/png" href="/fav-icon.jpg">
        <link rel="shortcut icon" type="image/x-icon" href="shortcut.jpg">
    </head>
    <body>

    </body>
</html>
```

## Alternative CSS

```html
<link rel="alternate stylesheet" href="path/to/style.css" title="yourTitle">
```

Some browsers allow alternate style sheets to apply if they are oﬀered. By default they will not be applied, but
usually they can be changed through the browser settings:

## Resource Hint: dns-prefetch, prefetch, prerender

### Preconnect

The preconnect relationship is similar to dns-prefetch in that it will resolve the DNS. However, it will also make the
TCP handshake, and optional TLS negotiation. This is an experimental feature.

```html
<link rel="preconnect" href="URL">
```

### DNS-Prefetch

Informs browsers to resolve the DNS for a URL, so that all assets from that URL load faster.

```html
<link rel="dns-prefetch" href="URL">
```

### Prefetch

Informs the browsers that a given resource should be prefetched so it can be loaded more quickly.

```html
<link rel="prefetch" href="URL">
```

### Prerender 

Informs browsers to fetch and render the URL in the background, so that they can be delivered to the user
instantaneously as the user navigates to that URL. This is an experimental feature.

```html
<link rel="prerender" href="URL">
```

## Link 'media' attribute

```html
<link rel="stylesheet" href="test.css" media="print">
```

Media speciﬁes what style sheet should be used for what type of media. Using the print value would only display
that style sheet for print pages.
The value of this attribute can be any of the mediatype values (similar to a CSS media query).

## Prev and Next

When a page is part of a series of articles, for instance, one can use prev and next to point to pages that are coming
before and after.

```html
<link rel="prev" href="http://stackoverflow.com/documentation/java/topics">
```

```html
<link rel="next" href="http://stackoverflow.com/documentation/css/topics">
```

## Web Feed

Use the rel="alternate" attribute to allow discoverability of your Atom/RSS feeds.

```html
<link rel="alternate" type="application/atom+xml" href="http://example.com/feed.xml" />
```

```html
<link rel="alternate type="application/rss+xml" href="http://example.com/feed.xml">
```



 

