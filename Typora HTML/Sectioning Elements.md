# Sectioning Elements

## Nav Element

The <nav> element is primarily intended to be used for sections that contain main navigation blocks for the
website, this can include links to other parts of the web page (e.g. anchors for a table of contents) or other pages
entirely.

**Inline items**

The following will display an inline set of hyperlinks.

![image-20210630095514022](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630095514022.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <nav>
            <a href="https://google.com">Google</a>
            <a href="https://www.yahoo.com">Yahoo!</a>
            <a href="https://www.bing.com">Bing</a>
        </nav>
    </body>
</html>
```

### Avoid unnecessary usage

"<footer> elements may have a list of links to other parts of the site (FAQ, T&C, etc.). The footer element alone is
suﬃcient in this case, you don't need to further wrap your links with a <nav> element in the <footer> ."

![image-20210630100057262](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630100057262.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <!-- the <nav> is not required in the <footer> -->
            <footer>
                <nav>
                    <a href="#"> ... </a>
                </nav>
            </footer>
            <!-- The footer alone is sufficient -->
            <footer>
                <a href="#">...</a>
            </footer>
    </body>
</html>
```

## Article Element

The <article> element contains self-contained content like articles, blog posts, user comments or an interactive
widget that could be distributed outside the context of the page, for example by RSS.
When article elements are nested, the contents of the inner article node should be related to the outer article
element.
A blog ( section ) with multiple posts ( article ), and comments ( article ) might look something like this.

![image-20210630101542350](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630101542350.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <section>
            <!-- Each individual blog post is an <article> -->
                <article>
                    <header>
                        <h1>Blog Post</h1>
                        <time datetime="2016-03-13">13th March 2016</time>
                    </header>

                    <p>The article element represents a self contined article or document.</p>
                    <p>The section element represents a grouping of contend.</p>

                    <section>
                        <h2>Comments <small>relating to "Blog Post"</small></h2>

                        <!-- Related comment is also a self-contined article-->
                        <article id="user-comment-1">
                            <p>Excelent!</p>
                            <footer><p>...</p><time>...</time></footer>
                        </article>
                    </section>
                </article>
        </section>
        <!-- Content unrelated to the blog or posts should be outside the section.-->
        <footer>
            <p>This content should be unrelated to the blog</p>
        </footer>
 
    </body>
</html>
```

When the main content of the page (excluding headers, footers, navigation bars, etc.) is simply one group of
elements. You can omit the <article> in favour of the <main> element.

```html
<article>
	<p>This doesn't make sense, this article has no real `context`.</p>
</article>
```

## Main element

The <main> element contains the main content for your web page. This content is unique to the individual page,
and should not appear elsewhere on the site. Repeating content like headers, footers, navigation, logos, etc., is
placed outside the element.
The <main> element should only ever be used at most once on a single page.
The <main> element must not be included as a descendant of an article , aside , footer , header or nav
element.
In the following example, we're displaying a single blog post (and related information like references and
comments).

![image-20210630102121623](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630102121623.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <header>
            <nav>...</nav>

            <main>
                <h1>Individual Blog Post</h1>
                <p>An introduction for the post.</p>

                <article>
                    <h2>References</h2>
                    <p>...</p>
                </article>

                <article>
                    <h2>Comments</h2>...
                </article>
            </main>
        </header>

        <footer>...</footer>
    </body>
</html>
```

## Header Element

The <header> element represents introductory content for its nearest ancestor sectioning content or sectioning
root element. A <header> typically contains a group of introductory or navigational aids.
**Note: The header element is not sectioning content; it doesn’t introduce a new section.**

**Examples**

![image-20210630102625039](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630102625039.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <header>
            <p>Welcome to...</p>
            <h1>Voidwars!</h1>
        </header>
        <article>
            <header>
                <h1>Flexbox: The definitive guide</h1>
            </header>
            <p>The guide about Flexbox was supposed to be here, but it turned out Wes wasn't a Flexbox 
                expert either.
            </p>
        </article>
    </body>
</html>
```

## Footer Element

The <footer> element contains the footer part of the page.
Here is an example for <footer> element that contain p paragraph tag.

![image-20210630102921292](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630102921292.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <footer>
            <p>All right reversed</p>
        </footer>
    </body>
</html>
```

## Section element

The <section> element represents a generic section to thematically group content. Every section, typically, should
be able to be identiﬁed with a heading element as a child of the section .
You can use the <section> element within an <article> and vice-versa.
Every section should have a theme (a heading element identifying this region)
Don't use the <section> element as a general styling 'container'.
If you need a container to apply styling, use a <div> instead.
In the following example, we're displaying a single blog post with multiple chapters each chapter is a section (a set
of thematically grouped content, which can be identiﬁed by the heading elements in each section).

![image-20210630103229201](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630103229201.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <article>
            <header>
                <h2>Blog Post</h2>
            </header>
            <p>An introduction for the post.</p>
            <section>
                <h3>Chapter 1</h3>
                <p>...</p>
            </section>
            <section>
                <h3>Chapter 2</h3>
                <p>...</p>
            </section>
            <section>
                <h3>Comments</h3>...
            </section>
        </article>
    </body>
</html>
```

