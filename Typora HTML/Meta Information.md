# Meta Information

Meta tags in HTML documents provide useful information about the document including a description, keywords,
author, dates of modiﬁcations and around 90 other ﬁelds. This topic covers the usage and purpose of these tags.

## Page Information

**application-name**

Giving the name of the Web application that the page represents.

```html
<meta name="application-name" content="OpenStreetMap">
```

If it's not a Web application, the application-name meta tag must not be used.

**author**

Set the author of the page:

```html
<meta name="author" content="Your Name">
```

Only one name can be given.
**description**
Set the description of the page:

```html
<meta name="description" content="Page Description">
```

The description meta tag can be used by various search engines while indexing your web page for searching
purpose. Usually, the description contained within the meta tag is the short summary that shows up under the
page/website's main title in the search engine results. Google usually uses only the ﬁrst 20-25 words of your
description.

**generator**

```html
<meta name="generator" content="HTML Generator 1.42">
```

Identiﬁes one of the software packages used to generate the document. Only to be used for pages where the
markup is automatically generated.
**keywords**
Set keywords for search engines (comma-separated):

```html
<meta name="keywords" content="Keyword1,Keyword2">
```

The keywords meta tag is sometimes used by search engines to know the search query which is relevant to your
web page.
As a rule of thumb, it is probably a good idea to not add too many words, as most search engines that use this meta
tag for indexing will only index the ﬁrst ~20 words. Make sure that you put the most important keywords ﬁrst.

## Social Media

Open Graph is a standard for metadata that extends the normal information contained within a site's head
markup. This enables websites such as Facebook to display deeper and richer information about a website in a
structured format. This information is then automatically displayed when users share links to websites containing OG metadata on Facebook.

### Facebook/Open Graph

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type content="website">
<meta property="og:title content="Content Title">
<meta property="og:image content="https://example.com/image.jpg">
<meta property="og:description" content="Site Name">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

## Web App

You can set up your web app or website to have an application shortcut icon added to a device's homescreen, and
have the app launch in full-screen "app mode" using Chrome for Android’s "Add to homescreen" menu item.
Below meta tag(s) will open web app in full-screen mode (without address bar).
**Android Chrome**

```html
<meta name="mobile-web-app-capable" content="yes">
```

**IOS**

```html
<meta name="apple-mobile-web-app-capable" content="yes">
```

You can also set color for status bar and address bar in meta tag.
**Android Chrome**

```html
<meta name="theme-color" content="black">
```

**IOS**

```html
<meta name="apple-mobile-web-app-status-bar-style" content="black">
```

