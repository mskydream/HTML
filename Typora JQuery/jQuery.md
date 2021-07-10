# Getting started with jQuery

## Getting Started
Create a ﬁle hello.html with the following content:

![image-20210708162035250](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708162035250.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div>
            <p id="hello">Some random text</p>
        </div>
        <script src="https://code.jquery.com/jquery-2.2.4.min.js">
            $(document).ready(function(){
                $('#hello').text('Hello,World!');
            });
        </script>
    </body> 
</html>
```

# Each function

## jQuery each function

![image-20210708162430906](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708162430906.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div>
            <ul>
                <li>Mango</li>
                <li>Book</li>
            </ul>
        </div>
        <script src="https://code.jquery.com/jquery-2.2.4.min.js">
            $("li").each(function(index){
                console.log(index + ": " + $(this).text());
            });
        </script>
    </body> 
</html>
```

# Events

## Delegated Events
Let's start with example. Here is a very simple example HTML.

![image-20210708162902892](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708162902892.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <ul>
            <li>
                <a href="some_url/">Link 1</a>
            </li>
            <li>
                <a href="some_url/">Link 2</a>
            </li>
            <li>
                <a href="some_url/">Link 3</a>
            </li>
        </ul>
        <script src="https://code.jquery.com/jquery-2.2.4.min.js">
            $('ul').on('click','a',function(){
                console.log(this.href);
            });
        </script>
    </body> 
</html>
```

## Attach and Detach Event Handlers

**Attach an Event Handler**
Since version 1.7 jQuery has the event API .on() . This way any standard javascript event or custom event can be
bound on the currently selected jQuery element. There are shortcuts such as .click() , but .on() gives you more
options.

![image-20210708163233561](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708163233561.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <button id="foo">bar</button>
        <script src="https://code.jquery.com/jquery-2.2.4.min.js">
            $("#foo").on("click",function(){
                console.log($(this).text());
            });
        </script>
    </body> 
</html>
```

**Detach an Event Handler**
Naturally you have the possibility to detach events from your jQuery objects too. You do so by using .off( events
[, selector ] [, handler ] ) .

![image-20210708163458778](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708163458778.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <button id="hello">hello</button>
        <script src="https://code.jquery.com/jquery-2.2.4.min.js">
            $("#hello").on("click",function(){
                console.log('hello world!');
                $(this).off();
            });
        </script>
    </body> 
</html>
```

## Events for repeating elements without using ID's
Problem
There is a series of repeating elements in page that you need to know which one an event occurred on to do
something with that speciﬁc instance.

![image-20210708164932785](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708164932785.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div class="item-wrapper" data-item_id="346">
            <div class="item"><span class="person">Fred</span></div>
            <div class="item-toolbar">
                <button class="delete">Delete</button>
            </div>
        </div>

        <div class="item-wrapper" data-item_id="393">
            <div class="item"><span class="person">Wilma</span></div>
            <div class="item-toolbar">
                <button class="delete">Delete</button>
            </div>
        </div>

        <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.0/jquery.min.js">
            $(function(){
                $('.delete').on('click',function(){
                    var $btn = $(this);
                    var $itemWrap = $btn.closest('.item-wrapper');
                    var person = $itemWrap.find('.person').text();

                    $.post('url/string',{id:$itemWrap.data('item_id')}).done(function(response){
                        $itemWrap.remove()
                    }).fail(function(){
                        alert('Ooops, not deleted at server');
                    });
                });
            });
        </script>
    </body> 
</html>
```

## originalEvent
Sometimes there will be properties that aren't available in jQuery event. To access the underlying properties use
Event.originalEvent

````js
$(ducument).on("wheel",function(e){
	console.log(e.originalEvent.detaY)
	// Returns a value between -100 and 100 depending on the direction you are scrolling
})
````

## Document Loading Event .load()
If you want your script to wait until a certain resource was loaded, such as an image or a PDF you can use .load() ,
which is a shortcut for shortcut for .on( "load", handler) .

```html
<img src="image.jpeg" alt="image" id="image">
```

JQUERY

```js
$("#image").load(function(){
	// run script
});
```

## DOM Manipulation

## Manipulating element classes
Assuming the page includes an HTML element like:

![image-20210709095735968](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709095735968.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <p class="small-paragraph">
            This is small <a href="https://en.wikipedia.org/wiki/Paragraph">paragraph</a>
            with a <a href="http://stackexchange.com" class="trusted"></a>
        </p>

        <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.0/jquery.min.js">
            $('p').hasClass('small-paragraph'); // true
            $('p').hasClass('large-paragraph'); // false

            // Add a class to all links within paragraphs
            $('p a').addClass('untrusted-link-in-paragraph');

            // Remove the class from a.trusted
            $('a.trusted.untrusted-link-in-paragraph')
            .removeClass('untrusted-link-in-paragraph')
            .addClass('trusted-link-in-paragraph');
        </script>
    </body> 
</html>
```

**Toggle a class**
Given the example markup, we can add a class with our ﬁrst .toggleClass() :

```js
$(".small-paragraph").toggleClass("property";)
```

Now this would return true : $(".small-paragraph").hasClass("pretty")
toggleClass provides the same eﬀect with less code as:

```js
if($(".small-paragraph").hasClass("pretty")){
	$(".small-paragraph").removeClass("pretty");}
else{
	$(".small-paragraph").addClass("pretty");
}
```

toggle Two classes:

```js
$(".small-paragraph").toggleClass("pretty cool");
```

Boolean to add/remove classes:

```js
$(".small-paragraph").toggleClass("pretty",true); // cannot be truthy/falsey
$(".small-paragraph").toggleClass("pretty",false);
```

Function for class toggle(see example further down to avoid an issue)

```js
$("div.surface").toggleClass(function(){
	if($(this).parent().is(".water")){
		return "wet";
	}else{
		return "dry";
	}
});
```

Used in examples:

```js
function stringContains(myString,mySubString){
	return myString.indexOf(mySubString) !==-1;
}
function isOdd(num){return num % 2;}
var showClass = true; // we want to add the class
```

Examples:
Use the element index to toggle classes odd/even

![image-20210709102601413](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709102601413.png)

```js
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div class = "grid">
            <div class="gridrow">row</div>
            <div class="gridrow">row</div>
            <div class="gridrow">row</div>
            <div class="gridrow">row</div>
            <div class="gridrow">row</div>
            <div class="gridrow gridfooter">row but I am footer!</div>
        </div>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js">
            function isOdd(num){
                return num % 2;
            }
            function stringContains(myString,mySubString){
                return myString.indexOf(mySubString) !== -1;
            }
            var showClass = true; // we want to add the class

            $("div.gridrow").toggleClass(function(index, oldClasses, showThisClass){
                if(isOdd(index)){
                    return "odd";
                }else{
                    return "even";
                }
                return oldClasses;
            }, showClass);

            $("div.gridrow").toogleClass(function(index, oldClasses, showThisClass){
                var isFooter = stringContains(oldClasses,"gridfooter");
                if(isFooter){
                    oldClasses = oldClasses.replace('even',' ').replace('odd',' ');
                    $(this).toggleClass("even odd",false);
                }
                return oldClasses;
            }, showClass);

            $("div.gridrow").toggleClass(function(index, oldClasses,showThisClass){
                var isFooter = stringContains(oldClasses,"gridFooter");
                if(!isFooter){
                    if(!isFooter){
                        return "oddLight";
                    }else{
                        return "evenLight";
                    }
                }
                else return oldClasses;
            }, showClass);
        </script>
    </body> 
</html>
```

# DOM Traversing

Select children of element
To select the children of an element you can use the children() method.

![image-20210709110812786](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709110812786.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div class="parent">
            <h2>A headline</h2>
            <p>Lorem ipsum dolor sit amet...</p>
            <p>Praesent quis dolor turpis...</p>
        </div>
        <script src="Jquery.js">
            $('.parent').children().css("color", "green");
        </script>

    </body> 
</html>
```

## Get next element
To get the next element you can use the .next() method.

![image-20210709111300009](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709111300009.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <ul>
            <li>Mark</li>
            <li class="anna">Anna</li>
            <li>Paul</li>
        </ul>
        <script src="Jquery.js"></script>
        <script>
            $(".anna").next().css("color", "green");
        </script>

    </body> 
</html>
```

## Filter a selection
To ﬁlter a selection you can use the .filter() method.
The method is called on a selection and returns a new selection. If the ﬁlter matches an element then it is added to
the returned selection, otherwise it is ignored. If no element is matched then an empty selection is returned.

![image-20210709111637067](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709111637067.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <ul>
            <li class="zero">Zero</li>
            <li class="one">One</li>
            <li class="two">Two</li>
            <li class="three">Three</li>
        </ul>
        <script src="Jquery.js"></script>
        <script>
            $("li").filter(":even").css("color","green"); // Color even element green
            $("li").filter(".one").css("font-weight","bold"); // Make ".one" bold
        </script>

    </body> 
</html>
```

## ﬁnd() method
.ﬁnd() method allows us to search through the descendants of these elements in the DOM tree and construct a new
jQuery object from the matching elements.

![image-20210709112120630](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709112120630.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div class="parent">
            <div class="children" name="first">
                <ul>
                    <li>A1</li>
                    <li>A2</li>
                    <li>A3</li>
                </ul>
            </div>
            <div class="children" name="second">
                <ul>
                    <li>B1</li>
                    <li>B2</li>
                    <li>B3</li>
                </ul>
            </div>
        </div>

        <script src="Jquery.js"></script>
        <script>
            $('.parent').find('.children[name="second"] ul li').css('font-weight','bold');
        </script>

    </body> 
</html>
```

## Iterating over list of jQuery elements
When you need to iterate over the list of jQuery elements.
Consider this DOM structure:

![image-20210709112515613](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709112515613.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div class="container">
            <div class="red one">RED 1 Info</div>
            <div class="red two">RED 2 Info</div>
            <div class="red three">RED 3 Info</div>
        </div>

        <script src="Jquery.js"></script>
        <script>
            $(".red").each(function(key,ele){
                var text = $(ele).text();
                console.log(text);
            });
        </script>

    </body> 
</html>
```

## Selecting siblings
To select siblings of an item you can use the .siblings() method.
A typical example where you want to modify the siblings of an item is in a menu:

![image-20210709112846962](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709112846962.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <ul class="menu">
            <li class="selected">Home</li>
            <li>Blog</li>
            <li>About</li>
        </ul>

        <script src="Jquery.js"></script>
        <script>
            $(".menu").on("click","li",function(){
                $(this).addClass("selected");
                $(this).siblings().removeClass("selected");
            });
        </script>

    </body> 
</html>
```

## closest() method
Returns the ﬁrst element that matches the selector starting at the element and traversing up the DOM tree.

![image-20210709114125681](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709114125681.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div id="abc" class="row">
            <div id="xyz" class="row">
            </div>
            <p id="origin">Hello</p>
        </div>

        <script src="Jquery.js"></script>
        <script>
            var target = $('#origin').closest('.row');
            console.log("Closest row:", target.attr('id') );
            var target2 = $('#origin').closest('p');
            console.log("Closest p:", target2.attr('id') );
        </script>

    </body> 
</html>
```

**ﬁrst() method : The ﬁrst method returns the ﬁrst element from the matched set of elements.**

![image-20210709114551240](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709114551240.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div class='.firsExample'>
            <p>This is first pragraph in a div.</p>
            <p>This is second paragraph in a div.</p>
            <p>This is third paragraph in a div.</p>
            <p>This is fourh paragraph in a div.</p>
            <p>This is fifth paragraph in a div.</p>
        </div>
        <script src="Jquery.js"></script>
        <script>
            var firstParagraph = $("div p").first();
            console.log("First paragraph:",firstParagraph.text());
        </script>

    </body> 
</html>
```

# Element Visibility

## Overview

```js
$(element).hide()
$(element).show()
$(element).toggle()
$(element).is(':visible')
$('element:visible')
$('element:hidden')
$('element').fadeIn();
$('element').fadeOut();
$('element').fadeIn(1000);
$('element').fadeOut(1000);
//
//
//
//
//
//
sets display: none
sets display to original value
toggles between the two
returns true or false
matches all elements that are visible
matches all elements that are hidden
// display the element
// hide the element
// display the element using timer
// hide the element using timer
// display the element using timer and a callback function
$('element').fadeIn(1000, function(){
// code to execute
});
// hide the element using timer and a callback function
$('element').fadeOut(1000, function(){
// code to execute
});
```

# Append

## jQuery append

![image-20210709115930881](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709115930881.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <p>This is a nice</p>
        <p>I like</p>
        <ul>
            <li>List item 1</li>
            <li>List item 2</li>
            <li>List item 3</li>
        </ul>
        <button id="btn-1">Append text</button>
        <button id="btn-2">Append list item</button>
        <script src="Jquery.js"></script>
        <script>
            $("#btn-1").click(function(){
                $("p").append(" <b>Book<b/>.");
            });
            $("#btn-2").click(function(){
                $("ul").append("<li>Appened list item</li>");
            });

        </script>

    </body> 
</html>
```

# Prepend

## Prepending an element to a container

![image-20210709132512554](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709132512554.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <div id="parent">
            <span>other content</span>
        </div>
        <div id="child">

        </div>
        <script src="Jquery.js"></script>
        <script>
            $('#child').prependTo($('#parent'));
        </script>

    </body> 
</html>
```

# jQuery .animate() Method

## Animation with callback
Sometimes we need to change words position from one place to another or reduce size of the words and change
the color of words automatically to improve the attraction of our website or web apps. JQuery helps a lot with this
concept using fadeIn(), hide(), slideDown() but its functionality are limited and it only done the speciﬁc task
which assign to it.
Jquery ﬁx this problem by providing an amazing and ﬂexible method called .animate() . This method allows to set
custom animations which is used css properties that give permission to ﬂy over borders. for example if we give css
style property as width:200; and current position of the DOM element is 50, animate method reduce current
position value from given css value and animate that element to 150.But we don't need to bother about this part
because animation engine will handle it.

![image-20210709132906071](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709132906071.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>
        <button id="btn1">Animate Width</button>
        <div id="box" style="background: #98bf21;height: 100px;width: 100px;margin: 6px;"></div>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
        <script>
            $("#btn1").click(function(){
            $("#box").animate({width: "200px"});
            });
        </script>

    </body> 
</html>
```

# Ajax

## Handling HTTP Response Codes with $.ajax()
In addition to .done , .fail and .always promise callbacks, which are triggered based on whether the request was
successful or not, there is the option to trigger a function when a speciﬁc HTTP Status Code is returned from the
server. This can be done using the statusCode parameter.

```js
$.ajax({
    type: {POST or GET or PUT etc.},
    url: {server.url},
    data: {someData: true},
    statusCode: {
		404: function(responseObject, textStatus, jqXHR) {
// No content found (404)
// This code will be executed if the server returns a 404 response
		},
		503: function(responseObject, textStatus, errorThrown) {
// Service Unavailable (503)
// This code will be executed if the server returns a 503 response
		}
	}
})
.done(function(data){
	alert(data);
})
.fail(function(jqXHR, textStatus){
	alert('Something went wrong: ' + textStatus);
})
.always(function(jqXHR, textStatus) {
	alert('Ajax request was finished')
});
```

## Using Ajax to Submit a Form

Sometimes you may have a form and want to submit it using ajax.
Suppose you have this simple form -

![image-20210709134548186](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709134548186.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>  
        <form action="ajax_form" action="form_action.php">
            <label for="name">Name :</label>
            <input name="name" id="name" type="text">
            <label for="name">Email :</label>
            <input name="email" id="email" type="text">
            <input type="submit" value="Submit">
        </form>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
        <script>
            $('#ajax_form').submit(function(event){
                event.preventDefault();
                var $form = $(this);
                $.ajax({
                    type: 'POST',
                    url: $form.attr('action'),
                    data: $form.serialize(),
                });
            });
        </script>

    </body> 
</html>
```

## Ajax File Uploads
1. A Simple Complete Example
We could use this sample code to upload the ﬁles selected by the user every time a new ﬁle selection is made.

![image-20210709135532984](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709135532984.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>  
        <input type="file" id="file-input" multiple>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
        <script>
            var files;
            var fdata = new FormData();
            $("#file-input").on("change",function(e){
                files = this.files;
                $.each(files,function(i,file){
                    fdata.append("file" + i,file);
                });
                fdata.append("FullName","Jhon Doe");
                fdata.append("Gender","Male");
                fdata.append("Age","24");
                $.ajax({
                    url: "/Test/Url",
                    type: "post",
                    data: fdata, // add the FormData object to the data parameter
                    processData:false, // tell jquery not to process data
                    contentType: false, // tell jquery not to set content-type
                    success: function(response,status,jqxhr){},
                    error: function (jqxhr,status,errorMessage){
                        // handle error
                    }
                });
            });
        </script>

    </body> 
</html>
```

# Checkbox Select all with automatic check/uncheck on other checkbox change
I've used various Stackoverﬂow examples and answers to come to this really simple example on how to manage
"select all" checkbox coupled with an automatic check/uncheck if any of the group checkbox status changes.
Constraint: The "select all" id must match the input names to create the select all group. In the example, the input
select all ID is cbGroup1. The input names are also cbGroup1
Code is very short, not plenty of if statement (time and resource consuming).

## 2 select all checkboxes with corresponding group checkboxes

![image-20210709140804122](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210709140804122.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JQuery</title>
        <style>
        </style>
    </head>
    <body>  
        <p>
            <input type="checkbox" id="cbGroup1">Select all
            <input type="checkbox" name="cbGroup1" value="value1_1">Group1 value 1
            <input type="checkbox" name="cbGroup1" value="value1_2">Group1 value 2
            <input type="checkbox" name="cbGroup1" value="value1_3">Group1 value 3
        </p>
        <p>
            <input type="checkbox" id="cbGroup2">Select all
            <input type="checkbox" name="cbGroup2" value="value2_1">Group1 value 1
            <input type="checkbox" name="cbGroup2" value="value2_2">Group1 value 2
            <input type="checkbox" name="cbGroup2" value="value2_3">Group1 value 3
        </p>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
        <script>
            $("input").change(function(){
                $('input[name=\''+this.id+'\']').not(this).prop('checked',this.checked);
                $("#" + this.name).prop('checked',$('input[name=\''+this.name+'\']').length === ('input[name=\''+this.name+'\']').filter(':checked').length);
            });

        </script>

    </body> 
</html>
```

# Plugins

## Plugins - Getting Started
The jQuery API may be extended by adding to its prototype. For example, the existing API already has many
functions available such as .hide() , .fadeIn() , .hasClass() , etc.
The jQuery prototype is exposed through $.fn , the source code contains the line
jQuery.fn = jQuery.prototype
Adding functions to this prototype will allow those functions to be available to be called from any constructed
jQuery object (which is done implicitly with each call to jQuery, or each call to $ if you prefer).
A constructed jQuery object will hold an internal array of elements based on the selector passed to it. For example,
$('.active') will construct a jQuery object that holds elements with the active class, at the time of calling (as in,
this is not a live set of elements).
The this value inside of the plugin function will refer to the constructed jQuery object. As a result, this is used to
represent the matched set.

**Basic Plugin:**

```js
$.fn.highlight = function(){
	this.css({background:"yellow"});
};
// Use example:
$("span").highlight();
```

**Chainability & Reusability**
Unlike the example above, jQuery Plugins are expected to be Chainable.
What this means is the possibility to chain multiple Methods to a same Collection of Elements like
$(".warn").append("WARNING! ").css({color:"red"}) (see how we used the .css() method after the .append() ,
both methods apply on the same .warn Collection)
Allowing one to use the same plugin on diﬀerent Collections passing diﬀerent customization options plays an
important role in Customization / Reusability

```js
(function($){
	$.fn.highlight = function(custom){
        var setting = $.extend({
            color: "",
            background: "yellow"
        },custom);
        return this.css({
            color: setting.color,
            backgroundColor: setting.background
        });
    };
}(jQuery));
```

**Freedom**
The above examples are in the scope of understanding basic Plugin creation. Keep in mind to not restrict a user to a
limited set of customization options.
Say for example you want to build a .highlight() Plugin where you can pass a desired text String that will be
highlighted and allow maximal freedom regarding styles:

```js
//...
// Default settings
var settings = $.extend({
	text: "",
	class: "highlight"
}, cutom);
return this.each(function(){
	// your word highlighting logic here
});
```

