# Flexible Box Layout (Flexbox)

The Flexible Box module, or just 'ﬂexbox' for short, is a box model designed for user interfaces, and it allows users
to align and distribute space among items in a container such that elements behave predictably when the page
layout must accommodate diﬀerent, unknown screen sizes. A ﬂex container expands items to ﬁll available space
and shrinks them to prevent overﬂow.

## Dynamic Vertical and Horizontal Centering (align-items, justify-content)
![image-20210702172439574](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702172439574.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
                .Aligner {
                display: flex;
                align-items: center;
                justify-content: center;
                background: #4fc;
                height: 500px;
                }

                .Aligner-item {
                background: #34d;
                max-width: 50%;
                }
        </style>
    </head>
    <body>
        <div class="Aligner">
            <div class="Aligner-item Aligner-item--fixed">
              <div class="Demo">
                <h3>I'm Centered!</h3>
                <p contenteditable="true">This box is both vertically and horizontally centered. Even if the text in this box changes to make it wider or taller, the box will still be centered. Go ahead, give it a try. Just click to edit the text.</p>
              </div>
           </div>
         </div>
    </body>
</html>
```

## Sticky Variable-Height Footer

This code creates a sticky footer. When the content doesn't reach the end of the viewport, the footer sticks to the
bottom of the viewport. When the content extends past the bottom of the viewport, the footer is also pushed out of
the viewport. 

![image-20210702173931998](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702173931998.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            html, body{
                height: 100%;
            }
            body{
                display:flex;
                flex-direction: column;
            }
            .content{
                flex: 1 0 auto;
            }
            .header, .footer{
                background-color: grey;
                color:white;
                flex:none;
            }
        </style>
    </head>
    <body>
        <div class="header">
            <h2>Header</h2>
        </div>
        <div class="content">
            <h1>Content</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent libero. 
                Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet. Duis sagittis 
                ipsum. Praesent mauris. Fusce nec  tellus sed augue semper porta. Mauris massa. Vestibulum lacinia 
                arcu eget nulla. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos 
                himenaeos. Curabitur sodales ligula in libero.
            </p>
        </div>
        <div class="footer">
            <h4>Footer</h4>
        </div>
    </body>
</html>
```

## Optimally ﬁt elements to their container

One of the nicest features of ﬂexbox is to allow optimally ﬁtting containers to their parent element.

![image-20210702174457647](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702174457647.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .flex-container{
                background-color: #000;
                height: 100%;
                display: flex;
                flex-direction:row;
                flex-wrap: wrap;
                justify-content: flex-start;
                align-content: stretch;
                align-items:stretch;
            }
            .flex-item{
                background-color: #ccf;
                margin:0.1em;
                flex-grow: 1;
                flex-shrink: 0;
                flex-basis: 200px;
            }
        </style>
    </head>
    <body>
        <div class="flex-container">
            <div class="flex-item">1</div>
            <div class="flex-item">2</div>
            <div class="flex-item">3</div>
            <div class="flex-item">4</div>
            <div class="flex-item">5</div>
        </div>
    </body>
</html>
```

## Holy Grail Layout using Flexbox

Holy Grail layout is a layout with a ﬁxed height header and footer, and a center with 3 columns. The 3 columns
include a ﬁxed width sidenav, a ﬂuid center, and a column for other content like ads (the ﬂuid center appears ﬁrst in
the markup). CSS Flexbox can be used to achieve this with a very simple markup:

![image-20210702175822427](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702175822427.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
                body{
                margin: 0;
                padding: 0;
                }

                .container{
                display: flex;
                flex-direction: column;
                height: 100vh;
                color: white;
                }

                .header{
                flex: 0 0 50px;
                background: #95A5A6;
                }

                .content-body{
                flex: 1 1 auto;
                
                display: flex;
                flex-direction: row;
                }

                .content-body .content{
                flex: 1 1 auto;
                overflow: auto;
                background: #1ABC9C;
                }

                .content-body .sidenav{
                order: -1;
                flex: 0 0 100px;
                overflow: auto;
                background: #E74C3C;
                }

                .content-body .ads{
                flex: 0 0 100px;
                overflow: auto;
                background: #E67E22;
                }

                .footer{
                flex: 0 0 50px;
                background: #34495E;
                }
        </style>
    </head>
    <body>
        <div class="container">
            <header class="header">Header</header>
            <div class="content-body">
              <main class="content">Content</main>
              <nav class="sidenav">Nav</nav>
              <aside class="ads">Ads</aside>
            </div>
            <footer class="footer">Footer</footer>
        </div>
    </body>
</html>
```

## 16.5: Perfectly aligned buttons inside cards with ﬂexbox

It's a regular pattern in design these days to vertically align call to actions inside its containing cards like this:

This can be achieved using a special trick with flexbox

![image-20210702180807952](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210702180807952.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .cards{
                display:flex;
            }
            .card{
                border:1px solid #ccc;
                margin: 10px 10px;
                padding: 0 20px;
            }
            button{
                height: 40px;
                background: #fff;
                padding: 0 40px;
                border: 1px solid #000;
            }
            p:last-child{
                text-align:center;
            }
        </style>
    </head>
    <body>
        <div class="cards">
            <div class="card">
                <p>Lorem ipsum Magna proident ex anim dolor ullamco pariatur reprehenderit culpa esse enim 
                    mollit labore dolore voluptate ullamco et ut sed qui minim.
                </p>
                <p><button>Action</button></p>
            </div>
            <div class="card">
                <p>Lorem ipsum Magna proident ex anim dolor ullamco pariatur reprehenderit culpa esse enim 
                    mollit labore dolore voluptate ullamco et ut sed qui minim.
                </p>
                <p>Lorem ipsum Magna proident ex anim dolor ullamco pariatur reprehenderit culpa esse enim 
                    mollit labore dolore voluptate ullamco et ut sed qui minim.
                </p>
                <p>Lorem ipsum Magna proident ex anim dolor ullamco pariatur reprehenderit culpa esse enim 
                    mollit labore dolore voluptate ullamco et ut sed qui minim.
                </p>
                <p>Lorem ipsum Magna proident ex anim dolor ullamco pariatur reprehenderit culpa esse enim 
                    mollit labore dolore voluptate ullamco et ut sed qui minim.
                </p>
                <p><button>Action</button></p>

            </div>
        </div>
    </body>
</html>
```

## Same height on nested containers

This code makes sure that all nested containers are always the same height. This is done by assuring that all nested
elements are the same height as the containing parent div. See working example: https://jsﬁddle.net/3wwh7ewp/
This eﬀect is achieved due to the property align-items being set to stretch by default.

![image-20210703094905105](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210703094905105.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>CSS</title>
        <style>
            .container{
                display:flex;
                align-items: stretch;
            }
        </style>
    </head>
    <body>
        <div class="cantainer">
            <div style="background-color: red;">
                Some <br>
                data <br>
                to make <br>
                a height <br>
            </div>
            <div style="background-color: blue;">
                Fewer <br>
                lines  <br>
            </div>
        </div>
    </body>
</html>
```

