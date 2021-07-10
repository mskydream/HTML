# Aria

## role="presentation"

An element whose implicit native role semantics will not be mapped to the accessibility API.

![image-20210630162802969](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630162802969.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div style="float:left;">Some content on the left</div>
            <div style="float:right;">Some content on the right</div>
            <div role="presentation" style="clear:both;"></div><!--Only used to clear floats-->
        </body>
    </html>
```

A message with important, and usually time-sensitive, information.

![image-20210630162942009](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630162942009.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role='alert' aria-live="assertive">Your session will expire in 60 seconds.</div>
        </body>
    </html>
```

## role="alertdialog"

A type of dialog that contains an alert message, where initial focus goes to an element within the dialog.

![image-20210630163213429](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630163213429.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role="alertdialog">
                <h1>Warning</h1>
                <div role="alert">Your session will expire in 60 seconds.</div>
            </div>
        </body>
    </html>
```

## role="application"

A region declared as a web application, as opposed to a web document. In this example, the application is a simple
calculator that might add two numbers together.

![image-20210630163508192](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630163508192.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role="application">
                <h1>Calculator</h1>
                <input type="text" id="num1"> + <input type="text" id="num2">
                <span id="result"></span>
            </div>
        </body>
    </html>
```

## role="article"

A section of a page that consists of a composition that forms an independent part of a document, page, or site.

![image-20210630164000533](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630164000533.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <article>
                <h1>My first article</h1>
                <p>Lorem ipsum...</p>
            </article>
        </body>
    </html>
```

You would use role=article on non-semantic elements (not recommended, invalid)

![image-20210630164138295](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630164138295.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role="article">
                <h1>My first article</h1>
                <p>Lorem ipsum...</p>
            </div>
        </body>
    </html>
```

##  role="banner"

A region that contains mostly site-oriented content, rather than page-speciﬁc content.

![image-20210630164421817](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630164421817.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role="banner">
                <h1>My Site</h1>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/about">About</a></li>
                    <li><a href="/contact">Contact</a></li>
                </ul>
            </div>
        </body>
    </html>
```

## role="button"

An input that allows for user-triggered actions when clicked or pressed.

![image-20210630164614364](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630164614364.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <button role="button">Add</button>
        </body>
    </html>
```

## role="cell"

A cell in a tabular container.

![image-20210630164928808](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630164928808.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <table>
                <thead>
                    <!-- etc-->
                </thead>
                <tbody>
                    <td role="cell">95</td>
                    <td role="cell">14</td>
                    <td role="cell">25</td>
                </tbody>
            </table>
        </body>
    </html>
```

## role="checkbox"

A checkable input that has three possible values: true, false, or mixed.

![image-20210630165131801](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630165131801.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <p>
                <input type="checkbox" role="checkbox" aria-checked="false">
                I agree to the terms
            </p>
        </body>
    </html>
```

## role="columnheader"

A cell containing header information for a column.

![image-20210630165433035](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630165433035.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <table>
                <thead>
                    <tr>
                        <th role="columnheader">Day 1</th>
                        <th role="columnheader">Day 2</th>
                        <th role="columnheader">Day 3</th>
                    </tr>
                </thead>
                <tbody>
                    <!-- etc -->
                </tbody>
            </table>
        </body>
    </html>
```

## role="combobox"

A presentation of a select; usually similar to a textbox where users can type ahead to select an option, or type to
enter arbitrary text as a new item in the list.

![image-20210630165620096](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630165620096.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <input type="text" role="combobox" aria-expanded="false">
        </body>
    </html>
```

Typically, you would use JavaScript to build the rest of the typeahead or list select functionality.

## role="complementary"

A supporting section of the document, designed to be complementary to the main content at a similar level in the
DOM hierarchy, but remains meaningful when separated from the main content.

![image-20210630165849235](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630165849235.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role="complementary">
                <h2>More Articles</h2>

                <ul>
                    <!-- etc -->
                </ul>
            </div>
        </body>
    </html>
```

## role="contentinfo"

A large perceivable region that contains information about the parent document.

![image-20210630170108794](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630170108794.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <p role="contentinfo">
                Author: Albert Einstein<br>
                Published: August 15, 1940
            </p>
        </body>
    </html>
```

## role="deﬁnition"

A deﬁnition of a term or concept.

![image-20210630170357954](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630170357954.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <span role="term" aria-labelledby="def1">Love</span>
            <span id="def1" role="definition">an intense feeling of deep affection.</span>
        </body>
    </html>
```

## role="dialog"

A dialog is an application window that is designed to interrupt the current processing of an application in order to
prompt the user to enter information or require a response.

![image-20210630170647102](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630170647102.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role="dialog">
                <p>Are you sure?</p>
                <button role="button">Yes</button>
                <button role="button">No</button>
            </div>
        </body>
    </html>
```

## role="directory"

A list of references to members of a group, such as a static table of contents.

![image-20210630170956368](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630170956368.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <ul role="directory">
                <li><a href="/chapter-1">Chapter 1</a></li>
                <li><a href="/chapter-2">Chapter 2</a></li>
                <li><a href="/chapter-3">Chapter 3</a></li>
            </ul>
        </body>
    </html>
```

## role="document"

A region containing related information that is declared as document content, as opposed to a web application.

![image-20210630171206384](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630171206384.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role="document">
                <h1>The life of Albert Einstein</h1>
                <p>Lorem ipsum...</p>
            </div>
        </body>
    </html>
```

## role="form"

A landmark region that contains a collection of items and objects that, as a whole, combine to create a form.
Using the semantically correct HTML element <form> implies default ARIA semantics, meaning role=form is not
required as you should not apply a contrasting role to an element that is already semantic, as adding a role
overrides the native semantics of an element.

![image-20210630171920517](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630171920517.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <form action="">
                <fieldset>
                    <legend>Login form</legend>
                    <div>
                        <label for="username">Your usernmame</label>
                        <input type="text" id="username" aria-describedby="username-tip" required>
                        <div role="tooltip" id="username-tip">Your username is your email address</div>
                    </div>
                    <div>
                        <label for="password">Your password</label>
                        <input type="text" id="password" aria-describedby="password-tip" required>
                        <div role="tooltip" id="password-tip">Was emailed to you when you signed up</div>
                    </div>
                </fieldset>
            </form>
        </body>
    </html>
```

## role="grid"

A grid is an interactive control which contains cells of tabular data arranged in rows and columns, like a table.

```html
<table role="grid">
	<thead>
		<!-- etc -->
	</thead>
	<tbody>
		<!-- etc -->
	</tbody>
<table>
```

## role="gridcell"

A cell in a grid or treegrid.

![image-20210630173154754](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630173154754.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <table role="grid">
                <thead>
                    <!-- etc -->
                </thead>
                <tbody>
                    <tr>
                        <td role="gridcell">17</td>
                        <td role="gridcell">64</td>
                        <td role="gridcell">18</td>
                    </tr>
                </tbody>
            </table>
        </body>
    </html>
```

## role="group"

A set of user interface objects which are not intended to be included in a page summary or table of contents by
assistive technologies.

![image-20210630173450062](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630173450062.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <div role="group">
                <button role="button">Previous</button>
                <button role="button">Next</button>
            </div>
        </body>
    </html>
```

## role="heading"

A heading for a section of the page.

```html
<h1 role="heading">Introduction<h1>
<p>Lorem ipsum...</p>
```

## role="img"

A container for a collection of elements that form an image.

```html
<figure role="img">
	<img alt="A cute cat." src="albert.jpg">
	<figcaption>This is my cat, Albert.</figcaption>
</figure>
```

## role="list"

A group of non-interactive list items.

![image-20210630174211055](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630174211055.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <ul role="list">
                <li role="listitem">One</li>
                <li role="listitem">Two</li>
                <li role="listitem">Three</li>
            </ul>
        </body>
    </html>
```

## role="log"

A type of live region where new information is added in meaningful order and old information may disappear.

![image-20210630174621644](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630174621644.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <ul role="log">
                <li>User 1 logged in.</li>
                <li>User 2 logged in.</li>
                <li>User 1 logged out.</li>
            </ul>
        </body>
    </html>
```

## role="main"

The main content of a document.

```html
<!-- header & nav here -->
<div role="main">
<p>Lorem ipsum...</p>
</div>
<!-- footer here -->
```

## role="marquee"

A type of live region where non-essential information changes frequently.

```html
<ul role="marquee">
    <li>Dow +0.26%</li>
    <li>Nasdaq +0.54%</li>
    <li>S&amp;P +0.44%</li>
</ul>
```

## role="math"

Content that represents a mathematical expression.

```html
<img role="math" alt="y=mx+b" src="slope.png">
```

## role="menu"

A type of widget that oﬀers a list of choices to the user.

```html
<ul role="menu">
	<li role="menuitem">New</li>
	<li role="menuitem">Open</li>
	<li role="menutime">Save</li>
	<li role="menutime">Close</li>
</ul>
```

## role="menubar"

A presentation of menu that usually remains visible and is usually presented horizontally.

```html
<ul role="menubar">
	<li role="menuitem">File</li>
	<li role="menuitem">Edit</li>
	<li role="menuitem">View</li>
	<li role="menuitem">Help</li>
</ul>
```

## role="menuitem"

An option in a group of choices contained by a menu or menubar.

```html
<ul role="menubar">
	<li role="menuitem">File</li>
	<li role="menuitem">Edit</li>
	<li role="menuitem">View</li>
	<li role="menuitem">Help</li>
</ul>
```

##  role="menuitemcheckbox"

A checkable menuitem that has three possible values: true, false, or mixed.

```html
<ul role="menu">
	<li role="menuitem">Console</li>
	<li role="menuitem">Layout</li>
	<li role="menuitemcheckbox" aria-checked="true">Word wrap</li>
</ul>
```

## role="menuitemradio"

A checkable menuitem in a group of menuitemradio roles, only one of which can be checked at a time.

```html
<ul role="menu">
	<li role="menuitemradio" aria-checked="true">Left</li>
	<li role="menuitemradio" aria-checked="false">Center</li>
	<li role="menuitemradio" aria-chcked="false">Right</li>
</ul>
```

## role="navigation"

A collection of navigational elements (usually links) for navigating the document or related documents.

```html
<ul role="navigation">
	<li><a href="/">Home</a></li>
	<li><a href="/about">About</a></li>
	<li><a href="/contact">Contact</a></li>
</ul>
```

## role="note"

A section whose content is parenthetic or ancillary to the main content of the resource.

```html
<p>Lorem ipsum...</p>
<p>Lorem ipsum...</p>
<p role="note">Lorem ipsum...</p>
```

## role="option"

A selectable item in a select list.

```html
<ul role="listbox">
	<li role="option">Option 1</li>
	<li role="option">Option 2</li>
	<li role="option">Option 3</li>
</ul>
```

## role="progressbar"

An element that displays the progress status for tasks that take a long time.

```html
<progress role="progressbar" value="25" max="100">25%</progress>
```

## role="radio"

A checkable input in a group of radio roles, only one of which can be checked at a time.

```html
<div role="radiogroup">
	<input role="radio" type="radio" aria-checked="true">One<br>
	<input role="radio" type="radio" aria-checked="false">Two<br>
	<input role="radio" type="radio" aria-checked="false">Three
</div>
```

## role="region"

A large perceivable section of a web page or document, that the author feels is important enough to be included in
a page summary or table of contents, for example, an area of the page containing live sporting event statistics.

```html
<div role="region">
	Home team: 4<br>
	Away team: 2
</div>
```

## role="radiogroup"

A group of radio buttons.

```html
<div role="radiogroup">
	<input role="radio" type="radio" aria-checked="true">One<br>
	<input role="radio" type="radio" aria-checked="false">Two<br>
	<input role="radio" type="radio" aria-checked="false">Three
</div>
```

## role="row"

A row of cells in a tabular container.

```html
<table>
	<thead>
		<!-- tec -->
	<thead>
	<tbody>
		<tr role="row">
			<!-- etc -->
		</tr>
	</tbody>
</table>
```

## role="rowgroup"

A group containing one or more row elements in a grid.

```html
<table>
	<thead role="rowgroup">
		<!-- etc -->
	</thead>
	<tbody role="rowgroup">
		<!-- etc -->
	</tbody>
</table>
```

## role="rowheader"

 A cell containing header information for a row in a grid.

```html
<table role="grid">
	<thead>
		<!-- etc -->
	</thead>
	<tbody>
		<tr>
			<th role="rowheader">Day 1</th>
			<td>65</td>
		</tr>
		<tr>
			<th role="rowheader">Day 2<th>
			<td>74</td>
		</tr>
	</tbody>
</table>
```

## role="scrollbar"

A graphical object that controls the scrolling of content within a viewing area, regardless of whether the content is
fully displayed within the viewing area.

```html
<div id="content1">Lorem ipsum...</div>
<div
	role="scrollbar"
	aria-controls="content1"
	aria-orientation="vertical"
	aria-valuemax="100"
	aria-valuemin="0"
	aria-valuenow="25">
		<div class="scrollhandle"></div>
</div>
	
```

## role="search"

A landmark region that contains a collection of items and objects that, as a whole, combine to create a search
facility.

```html
<div role="search">
	<input role="searchbox" type="text">
	<button role="button">Search</button>
</div>
```

## role="searchbox"

A type of textbox intended for specifying search criteria.

```html
<div role="search">
	<input role="searchbox" type="text">
	<button role="button">Search</button>
</div>
```

## role="separator"

A divider that separates and distinguishes sections of content or groups of menuitems.

```html
<p>Lorem ipsum...</p>
<hr role="separator">
<p>Lorem ipsum...</p>
```

## role="slider"

A user input where the user selects a value from within a given range.

```html
<div
	role="slider"
	aria-valuemax="100"
	aria-valuemin="0"
	aria-valuenow="25>
		<div class="sliderhandle"></div>
</div>
```

## role="spinbutton"

A form of range that expects the user to select from among discrete choices.

```html
<input 
	role="spinbutton"
	aria-valuemax="100"
	aria-valuemin="0"
	aria-valuenow="25"
	type="number"
	value="25">
```

## role="status"

A container whose content is advisory information for the user but is not important enough to justify an alert, often
but not necessarily presented as a status bar.

```html
<div role="status">Online</div>
```

## role="switch"

A type of checkbox that represents on/oﬀ values, as opposed to checked/unchecked values.

```html
<select role="switch" aria-cheked="false">
	<option>On</option>
	<option selected>Off</option>
</select>
```

## role="tab"

A grouping label providing a mechanism for selecting the tab content that is to be rendered to the user.

```html
<ul role="tablist">
	<li role="tab">Introduction</li>
	<li role="tab">Charset 1</li>
	<li role="tab">Charset 2</li>
</ul>
```

## role="table"

A section containing data arranged in rows and columns. The table role is intended for tabular containers which are
not interactive.

```html
<table role="table">
	<thead>
		<!-- etc -->
	</thead>
	<tbody>
		<!-- etc -->
	</tbody>
</table>
```

## role="tablist"

A list of tab elements, which are references to tabpanel elements.

```html
<ul role="tablist">
	<li role="tab">Introduction</li>
	<li role="tab">Chapter 1</li>
	<li role="tab">Chapter 2</li>
</ul>
```

## role="tabpanel"

A container for the resources associated with a tab, where each tab is contained in a tablist.

```html
<ul role="tablist">
	<li role="tab">Introduction</li>
	<li role="tab">Chapter 1</li>
	<li role="tab">Chapter 2</li>
</ul>
<div role="tabpanel">
	<!-- etc -->
</div>
```

## role="textbox"

Input that allows free-form text as its value.

```html
<textarea role="textbox"></textarea>
```

 ## role="timer"

A type of live region containing a numerical counter which indicates an amount of elapsed time from a start point,
or the time remaining until an end point.

```html
<p>
	<span role="timer">60</span> seconds remaining.
</p>
```

## role="toolbar"

A collection of commonly used function buttons represented in compact visual form.

```html
<ul role="footbar">
	<li><img alt="New" src="new.png"></li>
	<li><img alt="Open" src="open.png"></li>
	<li><img alt="Save" src="save.png"></li>
	<li><img alt="Close" src="close.png"></li>
</ul>
```

## role="tooltip"

A contextual popup that displays a description for an element.

```html
<span aria-describedby="slopadesc">Slope</span>
<div role="tooltip" id="slopedesc">y=mx+b</div>
```

Typically, the tooltip would be hidden. Using JavaScript, the tooltip would be displayed after a delay when the user
hovers over the element that it describes.

## role="tree"

A type of list that may contain sub-level nested groups that can be collapsed and expanded.

![image-20210701105325755](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701105325755.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <ul role="tree">
                <li role="treeitem">
                    Part 1
                    <ul>
                        <li role="treeitem">Chapter 1</li>
                        <li role="treeitem">Chapter 2</li>
                        <li role="treeitem">Chapter 3</li>
                    </ul>
                </li>
                <li role="treeitem">
                    Part 2
                    <li role="treeitem">Chapter 4</li>
                    <li role="treeitem">Chpater 5</li>
                    <li role="treeitem">Chapter 6</li>
                </li>
                <li role="treeitem">
                    Part 3
                    <ul>
                        <li role="treeitem">Chapter 7</li>
                        <li role="treeitem">Chapter 8</li>
                        <li role="treeitem">Chapter 9</li>
                    </ul>
                </li>
            </ul>
        </body>
    </html>
```

## role="treeitem"

An option item of a tree. This is an element within a tree that may be expanded or collapsed if it contains a sub-
level group of treeitems.

![image-20210701105543929](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210701105543929.png)

```html
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>HTML</title>
        </head>
        <body>
            <ul role="tree">
                <li role="treeitem">
                Part 1
                <ul>
                <li role="treeitem">Chapter
                <li role="treeitem">Chapter
                <li role="treeitem">Chapter
                </ul>
                </li>
                <li role="treeitem">
                Part 2
                <ul>
                <li role="treeitem">Chapter
                <li role="treeitem">Chapter
                <li role="treeitem">Chapter
                </ul>
                </li>
                <li role="treeitem">
                Part 3
                <ul>
                <li role="treeitem">Chapter
                <li role="treeitem">Chapter
                <li role="treeitem">Chapter
                </ul>
                </li>
                </ul>
        </body>
    </html>
```









