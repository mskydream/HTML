# Using console.log()

**Introduction**
All modern web browsers, Node.js as well as almost every other JavaScript environments support writing messages
to a console using a suite of logging methods. The most common of these methods is console.log() .
In a browser environment, the console.log() function is predominantly used for debugging purposes.

**Getting Started**
Open up the JavaScript Console in your browser, type the following, and press Enter

![image-20210705085118413](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705085118413.png)

**Logging variables**

console.log() can be used to log variables of any kind; not only strings. Just pass in the variable that you want to
be displayed in the console, for example:

![image-20210705085725324](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705085725324.png)

If you want to log two or more values, simply separate them with commas. Spaces will be automatically added
between each argument during concatenation:

![image-20210705085959826](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705085959826.png)

**Placeholder**

You can use console.log() in combination with placeholders:

![image-20210705090226295](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705090226295.png)

## Using the DOM API

DOM stands for Document Object Model. It is an object-oriented representation of structured documents like XML
and HTML.
Setting the textContent property of an Element is one way to output text on a web page.
For example, consider the following HTML tag:

```html
<p id="paragraph"></p>
```

To change its textContent property, we can run the following JavaScript:

```js
document.getElementById("paragraph").textContent = "Hello, World";
```

This will select the element that with the id paragraph and set its text content to "Hello, World":

```html
<p id="paragraph">Hello, World</p>
```

You can also use JavaScript to create a new HTML element programmatically. For example, consider an HTML
document with the following body:

```html
<body>
	<h1>Adding an element</h>
</body>
```

In our JavaScript, we create a new <p> tag with a textContent property of and add it at the end of the html body:

```js
var element = document.createElement('p');
element.textContent = "Hello, World";
document.body.appendChild(element);
```

That will change your HTML body to the following:

```html
<body>
	<h1>Addingan element</h1>
	<p>Hello, World</p>
</body>
```

## Using the DOM API (with graphical text: Canvas,SVG, or image ﬁle)
### Using canvas elements
HTML provides the canvas element for building raster-based images.
First build a canvas for holding image pixel information.

```js
var canvas = document.createElement('canvas');
canvas.width = 500;
canvas.height = 250;
```

Then select a context for the canvas, in this case two-dimensional:

```js
var ctx = canvas.getContext('2d');
```

Then set properties related to the text:

```js
ctx.font = '30px Cursive';
ctx.fillText("Hello world!", 50, 50);
```

Then insert the canvas element into the page to take eﬀect:

```js
document.body.appendChild(canvas);
```

### Using SVG
SVG is for building scalable vector-based graphics and can be used within HTML.
First create an SVG element container with dimensions:

```js
var svg = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
svg.width = 500;
svg.height = 50;
```

Then build a text element with the desired positioning and font characteristics:

```js
var text = document.createElementNS('http://www.w3.org/2000/svg', 'text');
text.setAttribute('x', '0');
text.setAttribute('y', '50');
text.style.FontFamily='Times New Roman';
text.style.fontSize = '50';
```

Then add the actual text to display to the text element :

```js
text.textCOntent = 'Hello world';
```

Finally add the text element to our svg container and add the svg container element to the HTML document:

```js
svg.appendChild(text);
document.body.appendChild(svg);
```

### Image ﬁle
If you already have an image ﬁle containing the desired text and have it placed on a server, you can add the URL of
the image and then add the image to the document as follows:

```js
var img = new Image();
img.src = 'https://i.ytimg.com/vi/zecueq-mo4M/maxresdefault.jpg';
document.body.appendChild(img);
```

# JavaScript Variables

## Deﬁning a Variable

```js
var myVarible = "This is a varible!";
```

This is an example of deﬁning variables. This variable is called a "string" because it has ASCII characters ( A-Z , 0-9 ,
!@#$ , etc.)

## Using a Variable

```js
var number1 = 5;
number1 = 3;
```

Here, we deﬁned a number called "number1" which was equal to 5. However, on the second line, we changed the
value to 3. To show the value of a variable, we log it to the console or use window.alert() :

```javascript
console.log(number1);
window.alert(number1);
```

To add, substract, multiply, divide, etc., we do like so:

```js
number1 = number1 + 5;
number1 = number1 - 6;
var number2 = number1 * 10;
var number3 = number2/number1;
```

We can also add string which will concatenate them, or put them togther. For example:

```js
var myString ="I am a " + "string!";
```

## Types of Variables

```js
var myInteger = 12;
var myLong = 931014141982;
var myFloat = 5.5;
var myDouble = 9310141419482.22;

var myBoolean = true;
var myBoolean = false;

var myNotANumber = NaN;
var NaN_Example = 0/0;

var notDefined;
window.alert(aRandomVariable);
var myNull = null;
```

## Arrays and Objects

```js
var myArray = [];
```

An arrays is a set of variales. For example:

```js
var favoriteFruits = ["apple", "orange", "strawberry"];
var carsInParkingLot = ["Toyota", "Ferarri", "Lexus"];
var employees = ["Billy", "Bob", "Joe"];
var primeNumbers = [2,3,5,7,11,13,17,19,23,29,31];
var randomVariables = [2, "any type works", undefined, null, true, 2.51];

myArray = ["zero", "one", "two"];
window.alert(myArray[0]);

myArray = ["John Doe", "Billy"];
elementNumber = 1;

window.alert(myArray[elementNumber]);
```

An object is a group of values; unlike arrays, we can do something better than them:

```js
myObject = {};
john = {firstname: "Jhon", lastname: "Doe", fullname: "John Doe"};
billy = {
    firstname: "Billy",
    lastname: undefined,
    fullname: "Billy"
};
window.alert(john.fullname);
window.alert(billy.firstname);
```

Rather than making an array ["John Doe", "Billy"] and calling myArray[0] , we can just call john.fullname and
billy.fullname .

# Built-in Constants

## null
null is used for representing the intentional absence of an object value and is a primitive value. Unlike undefined ,
it is not a property of the global object.
It is equal to undefined but not identical to it.

```js
null == undefined; //true
null == inderfined; //false
```

**CAREFUL**: The typeof null is 'object' .

```js
typeof null; // 'object';
```

To properly check if a value is null , compare it with the strict equality operator

```js
var a = null;
a === null; //true
```

## Testing for NaN using isNaN()
window.isNaN()
The global function isNaN() can be used to check if a certain value or expression evaluates to NaN . This function (in
short) ﬁrst checks if the value is a number, if not tries to convert it (*), and then checks if the resulting value is NaN .
For this reason, this testing method may cause confusion.
(*) The "conversion" method is not that simple, see ECMA-262 18.2.3 for a detailed explanation of the algorithm.
These examples will help you better understand the isNaN() behavior:

```js
isNan(NaN);				//true
isNan(1); 				//false: 1 is a number
isNan(-2e-4);			//false: -2e-4 is a number (-0.0002) in scientific notation
isNan(Infinity); 		//false: Infinity is a number 
isNan(true);			//false: converted to 1, which is a number
isNan(false); 			//false: converted to 0, which is a number
isNan(null); 			//false: converted to 0, which is a number
isNan(""); 				//false: converted to 0, which is a number
isNan(" "); 			//false: converted to 0, which is a number
isNan("45.3");			//false: string representing a number, converted to 45.3
isNan("1.2e3");			//false: string representing a number, converted to 1.2e3
isNan("Infinity"); 		//false: string representing a number, converted to Infinity
isNan(new Date); 		//false: Date object, converted to millisecond since epoch
isNan("10$");			//true: conversion fails, the dollar sign is not a digit
isNan("hello"); 		//true: conversion fails, no digit at all
isNan(underfined); 		//true: converted to NaN
isNan();				//true: converted to NaN
isNan(function(){});	//true: conversion fails
isNan({});				//true: conversion fails
isNan([1,2]);			//true: converted to "1,2", which can't be converted to a number
```

This last one is a bit tricky: checking if an Array is NaN . To do this, the Number() constructor ﬁrst converts the array to a string, then to a number; this is the reason why isNaN([]) and isNaN([34]) both return false , but isNaN([1,
2]) and isNaN([true]) both return true : because they get converted to "" , "34" , "1,2" and "true" respectively. In
general, an array is considered NaN by isNaN() unless it only holds one element whose string representation
can be converted to a valid number.

```js
Number.isNan()
```

In ECMAScript 6, the Number.isNaN() function has been implemented primarily to avoid the problem of
window.isNaN() of forcefully converting the parameter to a number. Number.isNaN() , indeed, doesn't try to
convert the value to a number before testing. This also means that only values of the type number, that are
also NaN , return true (which basically means only Number.isNaN(NaN) ).

## NaN
NaN stands for "Not a Number." When a mathematical function or operation in JavaScript cannot return a speciﬁc
number, it returns the value NaN instead.

It is a property of the global object, and a reference to Number.NaN

```js
window.hasOwnProperty('Nan'); //tue
NaN; //NaN
```

Perhaps confusingly, NaN is still considered a number.

```js
tupeof NaN; //'number'
```

Don't check for NaN using the equality operator. See isNaN instead.

```js
NaN == NaN //false
NaN === NaN//false
```

## undeﬁned and null
At ﬁrst glance it may appear that null and undefined are basically the same, however there are subtle but
important diﬀerences.
undefined is the absence of a value in the compiler, because where it should be a value, there hasn't been put one,
like the case of an unassigned variable.
			undefined is a global value that represents the absence of an assigned value.
									typeof undefined === 'undefined'
			null is an object that indicates that a variable has been explicitly assigned "no value".
									typeof null === 'object'
Setting a variable to undefined means the variable eﬀectively does not exist. Some processes, such as JSON
serialization, may strip undefined properties from objects. In contrast, null properties indicate will be preserved so
you can explicitly convey the concept of an "empty" property.
The following evaluate to undefined :

A variable when it is declared but not assigned a value (i.e. deﬁned)

```js
let foo;
console.log('is undefined?', foo === underfined);
```

Accessing the value of a property that doesn't exist

```js
let foo = {a: 'a'};
console.log('is undefined?', foo.b === underfined);
```

The return value of a function that doesn't return a value

```js
function foo(){return;}
console.log('is undefined?', foo() === undefined);
```

The value of a function argument that is declared but has been omitted from the function call

```js
function foo(param){
	console.log('is indefined?', param === underfined);
}
foo('a');
foo();
```

undefined is also a property of the global window object.

```js
console.log(window.undefined);
window.hasOwnProperty('undefined');
```

## Inﬁnity and -Inﬁnity

```js
1/0;//Infinity
//Whait! WHAAAT?
```

Infinity is a property of the global object (therefore a global variable) that represents mathematical inﬁnity. It is a
reference to Number.POSITIVE_INFINITY
It is greater than any other value, and you can get it by dividing by 0 or by evaluating the expression of a number
that's so big that overﬂows. This actually means there is no division by 0 errors in JavaScript, there is Inﬁnity!
There is also -Infinity which is mathematical negative inﬁnity, and it's lower than any other value.
To get -Infinity you negate Infinity , or get a reference to it in Number.NEGATIVE_INFINITY .

```js
-(Infinity); //-Infinity
```

Now let's have some fun with examples:

```js
Infinity > 1231922310293; //true
-Infinity  < -123192310293; //true
1/0; //Infinity
Math.pow(123123123,9123192391023); //Infinity
Number.MAX_VALUE * 2; //Infinity
23 / Infinity; //0
-Infinity; //-Infinity
-Infinity === Number.NEGATIVE_INFINITY;
-0; //-0, yes there is a negative 0 in the language
0 === -0 //true
1 / -0 // -Infinity
1/0 === 1 / -0; //false
Infinity + Infinity; //Infinity
var a = 0, b = -0;
a === b; //true
1/a === 1/b; //false
```

## Number constants

The Number constructor has some built in constants that can be useful

```js
Number.MAX_VALUE; //1.930838933838238938e+308
Number.MAX_SAFE_INTEGER; //90398329
Number.MIN_VALUE; //5e-324
Number.MIN_SAFE_INTEGER; //-900243432435848
Number.EPSILON; //0.00000000000000032423542242332234321
Number.POSITIVE_INFINITY; //Infinity
Number.NEGATIVE_INFINITY; //-Infinity
Number.NaN; //NaN
```

In many cases the various operators in JavaScript will break with values outside the range of
( Number.MIN_SAFE_INTEGER , Number.MAX_SAFE_INTEGER )
Note that Number.EPSILON represents the diﬀerent between one and the smallest Number greater than one, and
thus the smallest possible diﬀerence between two diﬀerent Number values. One reason to use this is due to the
nature of how numbers are stored by JavaScript see Check the equality of two numbers

## Operations that return NaN
Mathematical operations on values other than numbers return NaN.

```js
"b" * 3
"cde" - "e"
[1,2,3] * 2
```

An exception: Single-number arrays.

```js
[2] * [3] //Return 6
```

Also, remember that the + operator concatenates strings.

```js
"a" + "b" //Return "ab"
```

Dividing zero by zero returns NaN .

```js
0/0 //NaN
```

## Math library functions that return NaN
Generally, Math functions that are given non-numeric arguments will return NaN.

```js
Math.floor("a")
```

#  Comments

## Using Comments
To add annotations, hints, or exclude some code from being executed JavaScript provides two ways of commenting
code lines

### Single line Comment //

Everything after the // until the end of the line is excluded from execution.

```js
function elementAt(event){
	return document.elementFromPoint(event.clientX, event.clientY);
}
```

### Multi-line Comment /**/
Everything between the opening /* and the closing */ is excluded from execution, even if the opening and closing
are on diﬀerent lines.

```js
/* Gets the element from Event coordinates.
   Use like:
   var clikedE1 = someE1.addEventListener("click", elementAt, false);
*/
```

# Console

## Opening the Console
In most current browsers, the JavaScript Console has been integrated as a tab within Developer Tools. The shortcut
keys listed below will open Developer Tools, it might be necessary to switch to the right tab after that.

### Compatibility
When using or emulating Internet Explorer 8 or earlier versions (e.g. through Compatibility View / Enterprise Mode)
the console will only be deﬁned when the Developer Tools are active, so console.log() statements can cause an
exception and prevent code from executing. To mitigate this, you can check to see if the console is available before
you log:

````js
if(typeof window.console !== 'underfined'){
	console.log("Hello World");
}
````

## Measuring time - console.time()
console.time() can be used to measure how long a task in your code takes to run.
Calling console.time([label]) starts a new timer. When console.timeEnd([label]) is called, the elapsed time, in
milliseconds, since the original .time() call is calculated and logged. Because of this behavior, you can call
.timeEnd() multiple times with the same label to log the elapsed time since the original .time() call was made.

**Example 1:**

```js
console.time('response in');
alert('Click to continue');
console.timeEnd('response in');
alert('One more time');
console.timeEnd('response in');
```

wil outup:

````js
response in: 774.967ms
response in: 1402.199ms
````

**Example 2:**

![image-20210705110057797](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705110057797.png)

## Formatting console output
Many of the console's print methods can also handle C-like string formatting, using % tokens:

```js
console.log('%s has %d points','Sam', 100);
```

**Advanced styling**

When the CSS format speciﬁer ( %c ) is placed at the left side of the string, the print method will accept a second
parameter with CSS rules which allow ﬁne-grained control over the formatting of that string:

![image-20210705110505891](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705110505891.png)

****

**Other print methods**

In addition to the log method, modern browsers also support similar methods:
				console.info – small informative icon (ⓘ) appears on the left side of the printed string(s) or object(s).
				console.warn – small warning icon (!) appears on the left side. In some browsers, the background of the log
				is yellow.
				console.error – small times icon (⊗) appears on the left side. In some browsers, the background of the log is
				red.
				console.timeStamp – outputs the current time and a speciﬁed string, but is non-standard:
				console.timeStamp('msg');
				Displays:
				00:00:00.001 msg
				console.trace – outputs the current stack trace or displays the same output as the log method if invoked in
				the global scope.

## Including a stack trace when logging -console.trace()
![image-20210705110935356](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705110935356.png)

## Tabulating values - console.table()
In most environments, console.table() can be used to display objects and arrays in a tabular format.

**For example**

![image-20210705111119965](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705111119965.png)

Second Example:

![image-20210705111344851](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705111344851.png)

Third Example:

![image-20210705112440774](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705112440774.png)

## Counting - console.count()
console.count([obj]) places a counter on the object's value provided as argument. Each time this method is
invoked, the counter is increased (with the exception of the empty string '' ). A label together with a number is
displayed in the debugging console according to the following format:

```js
[label]: X
```

label represents the value of the object passed as argument and X represents the counter's value.
An object's value is always considered, even if variables are provided as arguments:

![image-20210705112843416](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705112843416.png)

Strings with numbers are converted to Number objects:

![image-20210705113114657](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705113114657.png)

Functions point always to the global Function object:

![image-20210705113552969](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705113552969.png)

Certain objects get speciﬁc counters associated to the type of object they refer to:

input:

![image-20210705114758701](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705114758701.png)

output:

![image-20210705114821379](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705114821379.png)

# Datatypes in JavaScript

## typeof
typeof is the 'oﬃcial' function that one uses to get the type in JavaScript, however in certain cases it might yield
some unexpected results ...

## Finding an object's class
To ﬁnd whether an object was constructed by a certain constructor or one inheriting from it, you can use the
instanceof command:

![image-20210705115603911](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705115603911.png)

Every value in JavaScript besides null and undefined also has a constructor property storing the function that was
used to construct it. This even works with primitives.

![image-20210705130325021](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705130325021.png)

# String

## Basic Info and String Concatenation
Strings in JavaScript can be enclosed in Single quotes 'hello' , Double quotes "Hello" and (from ES2015, ES6) in
Template Literals (backticks) `hello` .

```js
var hello = "Hello";
var world = 'world';
var helloW =  `Hello Wordl`;
```

Strings can be created from other types using the String() function.

```js
var intString = String(32); //"32"
var booleanString = String(true);
var nullString = String(null);
```

Or, toString() can be used to convert Numbers, Booleans or Objects to Strings.

```js
var intString = (5232).toString(); //"5232"
var booleanString = (false).toString(); //false
var objString = ({}).toString();//"[object Object]"
```

Strings also can be created by using String.fromCharCode method.

```js
String.fromCharCode(104,101,108,108,111)//hello
```

Creating a String object using new keyword is allowed, but is not recommended as it behaves like Objects unlike
primitive strings.

````js
var objectString = new String("Yes, I am a String object");
typeof objectString; //"object"
typeof objectString.valueOf();//"string"
````

**Concatenating Strings**
String concatenation can be done with the + concatenation operator, or with the built-in concat() method on the
String object prototype.

```js
var foo = "Foo";
var bar = "Bar";
console.log(foo + bar); //=> "Foo Bar"
console.log(foo + " " + bar); // => "Foo Bar"
foo.contact(bar) 			// => "FooBar"
"a".contact("b", " ", "d") // => "ab d"
```

Strings can be concatenated with non-string variables but will type-convert the non-string variables into strings.

```js
var string = "string";
var number = 32;
var boolean = true;
console.log(string + number + boolean); //"string32true"
```

With template literals, you can do string interpolation using ${variable} inside template literals:

```js
var place = `World`;
var greet = `Hello ${place}!`;
console.log(greet);//"Hello World!" only `...`
```

## Reverse String
The most "popular" way of reversing a string in JavaScript is the following code fragment, which is quite common:

```js
function reverseString(str){
	return str.split('').reverse().join('');
}
reverseString('string');  //"gnits"
```

**Using spread operator**

```js
function reverseString(str){
	return[...String(str)].reverse().join('');
}
console.log(reverseString('stackoverflow'));	//"wolfrevokcats"
console.log(reverseString(1337));				//"7331"
console.log(reverseString([1, 2, 3]));			//"3,2,1"
```

**Custom reverse() function**

![image-20210705133548946](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705133548946.png)

## Comparing Strings Lexicographically

To compare strings alphabetically, use localeCompare() . This returns a negative value if the reference string is
lexicographically (alphabetically) before the compared string (the parameter), a positive value if it comes
afterwards, and a value of 0 if they are equal.

![image-20210705134310354](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705134310354.png)

The > and < operators can also be used to compare strings lexicographically, but they cannot return a value of zero
(this can be tested with the == equality operator). As a result, a form of the localeCompare() function can be
written like so:

![image-20210705134826721](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705134826721.png)

This is especially useful when using a sorting function that compares based on the sign of the return value (such as
sort ).

![image-20210705135050095](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705135050095.png)

## Access character at index in string

Use charAt() to get a character at the speciﬁed index in the string.

```js
var string = "Hello, World!";
console.log(string.charAt(4));//"o"
```

Alternatively, because strings can be treated like arrays, use the index via bracket notation.

```js
var string = "Hello, World!";
console.log(string[4]);//o
```

To get the character code of the character at a speciﬁed index, use charCodeAt() .

```js
var string ="Hello, World!";
console.log(string.charCodeAt(4)); //111
```

## Escaping quotes

If your string is enclosed (i.e.) in single quotes you need to escape the inner literal quote with backslash \

```js
var text = 'L\'albero means tree in Italian';
console.log(text); \\"L'albero means tree in Italian"
```

Same goes for double quotes:

```js
var text = "I feel \"high\"";
```

Special attention must be given to escaping quotes if you're storing HTML representations within a String, since
HTML strings make large use of quotations i.e. in attributes:

```js
var content = "<p class=\"special\">Hello World!</p>"; //valid String
var hello = '<p class = "special">I\'d like to say "Hi"</p>'; //valid String
```

Quotes in HTML strings can also be represented using &apos; (or &#39; ) as a single quote and &quot; ( or &#34; ) as
double quotes.

```js
var hi = "<p class='special'>I'd like to say &quot;Hi&quot;</p>"; //valid String
var hello = '<p class="special">I&apos;d like to say "Hi"</p>'
```

## Word Counter
Say you have a <textarea> and you want to retrieve info about the number of:
			Characters (total)
			Characters (no spaces)
			Words
			Lines

```js
function wordCount(val){
	var wom = val.match(/\ S+g);
	return{
		charactersNoSpaces : val.replace(/\s+/g,'').lenght,
		characters 		   : val.lenght,
		words			   : wom ? wom.length : 0,
		lines			   : val.split(/\r*\n/).length
	};
}
wordCount(someMultilineText).words; //(Number of words)
```

## Trim whitespace
To trim whitespace from the edges of a string, use String.prototype.trim :

```js
" 	some whitespaced string 	".trim(); //"some whitespaced string"
```

Many JavaScript engines, but not Internet Explorer, have implemented non-standard trimLeft and trimRight
methods. There is a proposal, currently at Stage 1 of the process, for standardised trimStart and trimEnd
methods, aliased to trimLeft and trimRight for compatibility.

```js
//Stage 1 proposal
"		this is me		".trimStart(); //"this is me		"
"		this is me		".trimEnd(); //"		this is me"
//Non-standard methods, but currently implemented by most engines
"		this is me		".trimLeft(); //"this is me		"
"		this is me		".trimRight(); //"		this is me"
```

## Splitting a string into an array
Use .split to go from strings to an array of the split substrings:

```js
var s = "one, two, three, four, five"
s.split(". "); //["one", "two", "three", "four", "five"]
```

Use the array method .join to go back to a string:

```js
s.split(", ").join("--"); //"one--two--three--four--five"
```

## Strings are unicode
**All JavaScript strings are unicode!**

````js
var s = "some ∆≈ƒ unicode ¡™£¢¢¢";
s.charCodeAt(5); //8710
````

## Substrings with slice

Use .slice() to extract substrings given two indices:

````js
var s = "0123456789abcdefg";
s.slice(0, 5); //"01234"
s.slice(5, 6); //"5"
````

Given one index, it will take from that index to the end of the string:

```js
s.slice(10); //"abcdefg"
```

## String Find and Replace Functions
To search for a string inside a string, there are several functions:
indexOf( searchString ) and lastIndexOf( searchString )
indexOf() will return the index of the ﬁrst occurrence of searchString in the string. If searchString is not found,
then -1 is returned.

```js
var string = "Hello, World!";
console.log(string.indexOf("o")); //4
console.log(string.indexOf("foo")); //-1
```

Similarly, lastIndexOf() will return the index of the last occurrence of searchstring or -1 if not found.

```js
var string = "Hello, World!";
console.log(string.lastIndexOf("o"));  //8
console.log(string.lastIndexOf("foo")); //-1
```

includes() will return a boolean that tells whether searchString exists in the string, starting from index start
(defaults to 0). This is better than indexOf() if you simply need to test for existence of a substring.

```js
var string = "Hello, World!";
console.log(string.includes("Hello")); //true
console.log(string.includes("foo")); //false
```

replace() will return a string that has all occurrences of substrings matching the RegExp regexp or string
substring with a string replacement or the returned value of replaceFunction .
Note that this does not modify the string in place, but returns the string with replacements.

```js
var string = "Hello, World!";
string = string.replace("Hello", "Bye");
console.log(string); //"Bye, World!"

string = string.replace(/W.{3}d/g, "Universe");
console.log(string); //"Bye, Universe!"
```

Note that all parameters are optional.

```js
var string = "heLlo, woRlD!";
string = string.replace(/(a-zA-Z)([a-zA-Z]+)/g, function(match, g1, g2){
	return g.toUpperCase() + g2.toLowerCase();
});
console.log(string); //"Hello, World!"
```

## String to Upper Case

```js
console.log('qwerty'.toUpperCase()); //'QWERTY'
```

## String to Lower Case

String.prototype.toLowerCase()

```js
console.log('QWERTY'.toLowerCase()); //'qwerty'
```

## Repeat a String

This can be done using the .repeat() method:

```js
"abc".repeat(3); //Returns "abcabcabc"
"abc".repeat(0); //Returns ""
"abc".repeat(-1); //Throws a RangeError
```

In the general case, this should be done using a correct polyﬁll for the ES6 String.prototype.repeat() method.
Otherwise, the idiom new Array(n + 1).join(myString) can repeat n times the string myString :

````js
var myString = "abc";
var n = 3;
new Array(n + 1).join(myString); //Returns "abcabcabc"
````

# Create a new Date object
To create a new Date object use the Date() constructor:
**with no arguments**
			Date() creates a Date instance containing the current time (up to milliseconds) and date.
**with one integer argument**
			Date(m) creates a Date instance containing the time and date corresponding to the Epoch time (1 January,
			1970 UTC) plus m milliseconds. Example: new Date(749019369738) gives the date Sun, 26 Sep 1993 04:56:09
			GMT.
**with a string argument**
			Date(dateString) returns the Date object that results after parsing dateString with Date.parse .
**with two or more integer arguments**
			Date(i1, i2, i3, i4, i5, i6) reads the arguments as year, month, day, hours, minutes, seconds,
			milliseconds and instantiates the corresponding Date object. Note that the month is 0-indexed in JavaScript,
			so 0 means January and 11 means December. Example: new Date(2017, 5, 1) gives June 1st, 2017.

```js
// Creates a Date object with the current date and time from the
// user's browser
var now = new Date();
now.toString() === 'Mon Apr 11 2016 16:10:41 GMT-0500 (Central Daylight Time)'
// true
// well, at the time of this writing, anyway
// Creates a Date object at the Unix Epoch (i.e., '1970-01-01T00:00:00.000Z')
var epoch = new Date(0);
epoch.toISOString() === '1970-01-01T00:00:00.000Z' // true
// Creates a Date object with the date and time 2,012 milliseconds
// after the Unix Epoch (i.e., '1970-01-01T00:00:02.012Z').
var ms = new Date(2012);
date2012.toISOString() === '1970-01-01T00:00:02.012Z' // true
// Creates a Date object with the first day of February of the year 2012
// in the local timezone.
var one = new Date(2012, 1);
one.toString() === 'Wed Feb 01 2012 00:00:00 GMT-0600 (Central Standard Time)'
// true
// Creates a Date object with the first day of the year 2012 in the local
// timezone.
// (Months are zero-based)
var zero = new Date(2012, 0);
zero.toString() === 'Sun Jan 01 2012 00:00:00 GMT-0600 (Central Standard Time)'
// true
// Creates a Date object with the first day of the year 2012, in UTC.
var utc = new Date(Date.UTC(2012, 0));
utc.toString() === 'Sat Dec 31 2011 18:00:00 GMT-0600 (Central Standard Time)'
// true
utc.toISOString() === '2012-01-01T00:00:00.000Z'
// true
// Parses a string into a Date object (ISO 8601 format added in ECMAScript 5.1)
// Implementations should assumed UTC because of ISO 8601 format and Z designation
var iso = new Date('2012-01-01T00:00:00.000Z');
iso.toISOString() === '2012-01-01T00:00:00.000Z' // true
// Parses a string into a Date object (RFC in JavaScript 1.0)
var local = new Date('Sun, 01 Jan 2012 00:00:00 -0600');
local.toString() === 'Sun Jan 01 2012 00:00:00 GMT-0600 (Central Standard Time)'
// true
// Parses a string in no particular format, most of the time. Note that parsing
// logic in these cases is very implementation-dependent, and therefore can vary
// across browsers and versions.
var anything = new Date('11/12/2012');
anything.toString() === 'Mon Nov 12 2012 00:00:00 GMT-0600 (Central Standard Time)'
// true, in Chrome 49 64-bit on Windows 10 in the en-US locale. Other versions in
// other locales may get a different result.
// Rolls values outside of a specified range to the next value.
var rollover = new Date(2012, 12, 32, 25, 62, 62, 1023);
rollover.toString() === 'Sat Feb 02 2013 02:03:03 GMT-0600 (Central Standard Time)'
// true; note that the month rolled over to Feb; first the month rolled over to
// Jan based on the month 12 (11 being December), then again because of the day 32
// (January having 31 days).
// Special dates for years in the range 0-99
var special1 = new Date(12, 0);
special1.toString() === 'Mon Jan 01 1912 00:00:00 GMT-0600 (Central Standard Time)`
// true
// If you actually wanted to set the year to the year 12 CE, you'd need to use the
// setFullYear() method:
special1.setFullYear(12);
special1.toString() === 'Sun Jan 01
12 00:00:00 GMT-0600 (Central Standard Time)`
// true
```

## Convert to a string format

**Convert to String**

![image-20210705145610799](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705145610799.png)

**Convert to Time String**

![image-20210705145711219](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705145711219.png)

**Convert to Date String**

![image-20210705145816041](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705145816041.png)

**Convert to UTC String**

![image-20210705145917161](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705145917161.png)

**Convert to ISO String**

![image-20210705150016565](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705150016565.png)

**Convert to GMT String**

![image-20210705150110901](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705150110901.png)

**Convert to Locale Date String**

![image-20210705150212352](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705150212352.png)

## Creating a Date from UTC
By default, a Date object is created as local time. This is not always desirable, for example when communicating a
date between a server and a client that do not reside in the same timezone. In this scenario, one doesn't want to
worry about timezones at all until the date needs to be displayed in local time, if that is even required at all.
**The problem**
In this problem we want to communicate a speciﬁc date (day, month, year) with someone in a diﬀerent timezone.
The ﬁrst implementation naively uses local times, which results in wrong results. The second implementation uses
UTC dates to avoid timezones where they are not needed.
**Naive approach with WRONG results**

![image-20210705151625223](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705151625223.png)

**Changing a Date object**

All Date object modiﬁers, such as setDate(...) and setFullYear(...) have an equivalent takes an argument in
UTC time rather than in local time.

![image-20210705151933576](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705151933576.png)

## Formatting a JavaScript date
Formatting a JavaScript date in modern browsers
In modern browsers (*), Date.prototype.toLocaleDateString() allows you to deﬁne the formatting of a Date in a
convenient manner.
It requires the following format :
dateObj.toLocaleDateString([locales [, options]])
The locales parameter should be a string with a BCP 47 language tag, or an array of such strings.
The options parameter should be an object with some or all of the following properties:

**localeMatcher** : possible values are "lookup" and "best fit" ; the default is "best fit"
**timeZone** : the only value implementations must recognize is "UTC" ; the default is the runtime's default time zone

**hour12** :possible values are true and false ; the default is locale dependent
**formatMatcher** : possible values are "basic" and "best fit" ; the default is "best fit"
**weekday** : possible values are "narrow" , "short" & "long"
**era** : possible values are "narrow" , "short" & "long"
**year** : possible values are "numeric" & "2-digit"
**month** : possible values are "numeric" , "2-digit" , "narrow" , "short" & "long"
**day** : possible values are "numeric" & "2-digit"
**hour** : possible values are "numeric" & "2-digit"
**minute** : possible values are "numeric" & "2-digit"
**second** : possible values are "numeric" & "2-digit"
**timeZoneName** : possible values are "short" & "long"

**Going custom**
If Date.prototype.toLocaleDateString() isn't ﬂexible enough to fulﬁll whatever need you may have, you might
want to consider creating a custom Date object that looks like this:

```js
var DateObject = (function(){
	var monthNames = [
		"January","February","March",
		"April","May","June","July",
		"August", "September", "October",
		"November","December"
	];
	var date = function(str){
		this.set(str);
	};
	date.prototype = {
		set:funtion(str){
			var dateDef = str ? new Date(str) : new Date();
			this.day = dateDef.getDate();
			this.dayPadded = (this.day < 10) ? ("0" + this.day) : "" +this.day;
			this.month = dateDef.getMonth() + 1;
			this.monthPadded = (this.month < 10) ? ("0" + this.month) : "" + this.month;
			this.monthName = monthNames[this.month - 1];
			this.year = dateDef.getFullYear();
		},
		get : function(properties, separator){
			var separator = separator ? separator : '-' ret = [];
			for(var i in properties){
				ret.push(this[properties[i]]);
			}
			return ret.join(separator);
		}
	};
	return date;
})();
```

## Get the number of milliseconds elapsed since 1 January 1970 00:00:00 UTC

The static method Date.now returns the number of milliseconds that have elapsed since 1 January 1970 00:00:00
UTC. To get the number of milliseconds that have elapsed since that time using an instance of a Date object, use its
getTime method.

![image-20210705154925189](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705154925189.png)

## Get the current time and date
Use new Date() to generate a new Date object containing the current date and time.
Note that Date() called without arguments is equivalent to new Date(Date.now()) .
Once you have a date object, you can apply any of the several available methods to extract its properties (e.g.
getFullYear() to get the 4-digits year).
Below are some common date methods.
**Get the current year**

![image-20210705155541432](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705155541432.png)

**Get the current month**

![image-20210705155702369](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705155702369.png)

Please note that 0 = January. This is because months range from 0 to 11, so it is often desirable to add +1 to the
index.
**Get the current day**

![image-20210705155830326](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705155830326.png)

**Get the current hour**

![image-20210705155951707](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705155951707.png)

**Get the current minutes**

![image-20210705160109727](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705160109727.png)

**Get the current milliseconds**
To get the milliseconds (ranging from 0 to 999) of an instance of a Date object, use its getMilliseconds method.

![image-20210705161057962](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705161057962.png)

**Convert the current time and date to a human-readable string**

![image-20210705161319084](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705161319084.png)

## Increment a Date Object
To increment date objects in JavaScript, we can usually do this:

![image-20210705161452019](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705161452019.png)

**Adding Work Days**

If you wish to add work days (in this case I am assuming Monday - Friday) you can use the setDate function
although you need a little extra logic to account for the weekends (obviously this will not take account of national
holidays) -

# Date Comparison

## Comparing Date values
To check the equality of Date values:

![image-20210705161832580](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705161832580.png)

Note that you must use valueOf() or getTime() to compare the values of Date objects because the equality
operator will compare if two object references are the same. For example:

![image-20210705161946182](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705161946182.png)

Whereas if the variables point to the same object:

![image-20210705162118093](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705162118093.png)

However, the other comparison operators will work as usual and you can use < and > to compare that one date is
earlier or later than the other. For example:

![image-20210705162259939](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705162259939.png)

It works even if the operator includes equality:

![image-20210705162430487](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705162430487.png)

## Date Difference Calculation
To compare the diﬀerence of two dates, we can do the comparison based on the timestamp.

![image-20210705162759170](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705162759170.png)

# Comparison Operations

## Abstract equality / inequality and type conversion

**The Problem**

The abstract equality and inequality operators ( == and != ) convert their operands if the operand types do not
match. This type coercion is a common source of confusion about the results of these operators, in particular, these
operators aren't always transitive as one would expect.

```js
"" == 0; //true A
0 == "0"; //true A
"" == "0"; //false B
false == 0; //true
false == "0" // true

"" != 0; //false A
0 != "0"; //false A
"" != "0"; // true B
false != 0; //false
false != "0"; //false
```

The results start to make sense if you consider how JavaScript converts empty strings to numbers.

```js
Number(""); // 0
Number("0"); // 0
Number(false); // 0
```

**The Solution**

In the statement false B , both the operands are strings ( "" and "0" ), hence there will be no type conversion and
since "" and "0" are not the same value, "" == "0" is false as expected.
One way to eliminate unexpected behavior here is making sure that you always compare operands of the same
type. For example, if you want the results of numerical comparison use explicit conversion:

```js
var test = (a,b) => Number(a) == Number(b);
test("", 0); //true;
test("0", 0); //true
test("", "0"); //true;
test("abc", "abc"); //false as operands are not numbers
```

Or, if you want string comparison:

```js
var test = (a,b) => String(a) == String(b);
test("", 0); //false;
test("0", 0); //true
test("", "0"); //false
```

## NaN Property of the Global Object
NaN ("Not a Number") is a special value deﬁned by the IEEE Standard for Floating-Point Arithmetic, which is used when
a non-numeric value is provided but a number is expected ( 1 * "two" ), or when a calculation doesn't have a valid
number result ( Math.sqrt(-1) ).
Any equality or relational comparisons with NaN returns false , even comparing it with itself. Because, NaN is
supposed to denote the result of a nonsensical computation, and as such, it isn’t equal to the result of any other
nonsensical computations.

```js
(1* "two") === NaN //false
NaN === 0;			//false
NaN === NaN;		//false
Number.NaN ===		//false

NaN < 0;			//false
NaN > 0;			//false
NaN >= NaN;			//false
NaN >= 'two';		//false
```

Non-equal comparisons will always return true :

```js
NaN !== 0; //true
NaN !== NaN //true
```

## Short-circuiting in boolean operators
The and-operator ( && ) and the or-operator ( || ) employ short-circuiting to prevent unnecessary work if the outcome
of the operation does not change with the extra work.
In x && y , y will not be evaluated if x evaluates to false , because the whole expression is guaranteed to be false .
In x || y , y will not be evaluated if x evaluated to true , because the whole expression is guaranteed to be true .

**Example with functions**

```js
function T(){
	console.log("T");
	return true;
}
function F(){
	console.log("F");
	return false;
}
```

## Null and Undeﬁned
The diﬀerences between null and undefined
null and undefined share abstract equality == but not strict equality === ,

```js
null === undefined //true
null === undefined //false
```

The similarities between null and undefined
null and undefined are both falsy.

```js
if(null) console.log("won't be logged");
if(undefined) console.log("won't be logged");
```

Neither null or undefined equal false (see this question).

```js
false == undefined //false
false == null 		//false
false === undefined	//false
false === null		//false
```

## Abstract Equality (==)

**Examples:**

```js
1 == 1;						//true
1 == true;					//true
1 == '1';					//true
1 == '1.00';				//true
1 == '1.000000001';			//false
0 == false;					//true
0 == undefined;				//false
0 == "";					//false
```

## Automatic Type Conversions
Beware that numbers can accidentally be converted to strings or NaN (Not a Number).
JavaScript is loosely typed. A variable can contain diﬀerent data types, and a variable can change its data type:

```js
var x = 5+7; 					//is 12
var x = 5+"7";					//is 57
var x = 5 - 7;					// is -2
var x = 5 - "7";				// is -2
var x = "5" - 7;				// is -2
var x = 5 - "x";				// is NaN		
```

## Logic Operators with Non-boolean values
(boolean coercion)
Logical OR ( || ), reading left to right, will evaluate to the ﬁrst truthy value. If no truthy value is found, the last value is
returned.

```js
var a = 'hello' || '';				// a = 'hello'
var b = '' || [];					// b = []
var c = '' || undefined;			// c = undefined
var d = 1 || 5;						// d = 1
var e = 0 || {};					// e = {}
var f = 0 || '' || 5;				// f = 5
var g = '' || 'yay' || 'boo';		// g = 'yay'
```

Logical AND ( && ), reading left to right, will evaluate to the ﬁrst falsy value. If no falsey value is found, the last value is
returned.

```js
var a = 'hello' && '';				//a = ''
var b = '' && [];					//b = ''
var c = undefined && 0;				//c = undefined
var d = 1 && 5;						//d = 5
var e = 0 && {};					// e = 0
var f = 'hi' && [] && 'done';		//f = 'done'
var g = 'bye' && undefined && 'adios';	//g = undefined
```

This trick can be used, for example, to set a default value to a function argument (prior to ES6).

![image-20210705171435163](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210705171435163.png)

## Equality comparison operations
JavaScript has four diﬀerent equality comparison operations.
SameValue
It returns true if both operands belong to the same Type and are the same value.
Note: the value of an object is a reference.
You can use this comparison algorithm via Object.is (ECMAScript 6).

```js
Object.is(1,1);					//true
Object.is(+0,-0);				//false
Object.is(NaN, NaN);			//true
Object.is(true, "true");		//false
Object.is(false, 0);			//false
Object.is(null,undefined);		//false
Object.is(1,"1");				//false
Object.is([],[]);				//false
```

You can use this comparison algorithm via Array.prototype.includes (ECMAScript 7).

```js
[1].includes(1);			//true
[+0].includes(-0);			//true
[NaN].includes(NaN);		//true
[true].includes("true")		//false
[false].includes(0);		//false
[1].includes("1");			//false
[null].includes(undefined);	//false
[[]].includes([]);			//false
```

## Grouping multiple logic statements
You can group multiple boolean logic statements within parenthesis in order to create a more complex logic
evaluation, especially useful in if statements.

## Bit ﬁelds to optimise comparison of multi state data
A bit ﬁeld is a variable that holds various boolean states as individual bits. A bit on would represent true, and oﬀ
would be false. In the past bit ﬁelds were routinely used as they saved memory and reduced processing load.
Though the need to use bit ﬁeld is no longer so important they do oﬀer some beneﬁts that can simplify many
processing tasks.
For example user input. When getting input from a keyboard's direction keys up, down, left, right you can encode
the various keys into a single variable with each direction assigned a bit.
Example reading keyboard via bitﬁeld

```js
var bitField = 0;
const KEY_BITS = [4,1,8,2];
const KEY_MASKS = [0b1011,0b1110,0b0111,0b1101];
window.onkeydown = window.onkeyup = function(e){
    if(e.keyCode >= 37 && e.keyCode < 41){
        if(e.type === "keydown"){
            bitField |= KEY_BITS[e.keyCode - 37];
        }else{
            bitField &= KEY_MASKS[e.keyCode -37];
        }
    }
}
```

Example reading as an array

```js
var directionState = [false,false,false,false];
window.onkeydown = window.onkeyup =function(e){
	if(e.keyCode >= 37 && e.keyCode < 41){
		directionState[e.keyCode - 37] = e.type === "keydown";
	}
}
```

To turn on a bit use bitwise or | and the value corresponding to the bit. So if you wish to set the 2nd bit bitField
|= 0b10 will turn it on. If you wish to turn a bit oﬀ use bitwise and & with a value that has all by the required bit on.
Using 4 bits and turning the 2nd bit oﬀ bitfield &= 0b1101;
You may say the above example seems a lot more complex than assigning the various key states to an array. Yes, it
is a little more complex to set but the advantage comes when interrogating the state.
If you want to test if all keys are up.

```js
if(!bitfield)
if(!(directionState[0] && directionState[1] && directionState[2] && directionState[3]))
```

You can set some constants to make things easier

```js
const KEY_U = 1;
const KEY_D = 2;
const KEY_L = 4;
const KEY_R = 8;
const KEY_UL = KEY_U + KEY_L; //up left
const KEY_UR = KEY_U + KEY_R; //up right
const KEY_DL = KEY_D + KEY_L; //down left
const KEY_DR = KEY_D + KEY_R; //down right
```

You can then quickly test for many various keyboard states

```js
if((bitfield & KEY_UL) === KEY_UL)				//is UP and LEFT only down
if(bitfield & KEY_UL)							//is UP left down
if((bitfield & KEY_U) === KEY_U)				//is UP only down
if(bitfield & KEY_U)							//is UP down (any other key may be down)
if(!(bitfield & KEY_U))							//is UP up (any other key may be down)
if(!bitfield)									//no keys are down 
if(bitfield)									//any one or more keys are down
```

The keyboard input is just one example. Bitﬁelds are useful when you have various states that must in combination
be acted on. JavaScript can use up to 32 bits for a bit ﬁeld. Using them can oﬀer signiﬁcant performance increases.
They are worth being familiar with.

# Conditions
Conditional expressions, involving keywords such as if and else, provide JavaScript programs with the ability to
perform diﬀerent actions depending on a Boolean condition: true or false. This section covers the use of JavaScript
conditionals, Boolean logic, and ternary statements.

## Ternary operators
Can be used to shorten if/else operations. This comes in handy for returning a value quickly (i.e. in order to assign it
to another variable).

Ex:

````js
var animal = 'kitty';
var result = (animal === 'kitty') ? 'cute' : 'still nice';
````

In this case, result gets the 'cute' value, because the value of animal is 'kitty'. If animal had another value, result
would get the 'still nice' value.
Compare this to what the code would like with if/else conditions.

```js
var animal = 'kitty';
var result = '';
if(animal === 'kitty'){
	result = 'cute';
}else{
	result = 'still nice';
}
```

The if or else conditions may have several operations. In this case the operator returns the result of the last
expression.

```js
var a = 0;
var str = 'not a';
var b = '';
b = a === 0 ? (a = 1, str += ' test') : (a = 2)''
```

Because a was equal to 0, it becomes 1 , and str becomes 'not a test'. The operation which involved str was the
last, so b receives the result of the operation, which is the value contained in str , i.e. 'not a test'.
Ternary operators always expect else conditions, otherwise you'll get a syntax error. As a workaround you could
return a zero something similar in the else branch - this doesn't matter if you aren't using the return value but just
shortening (or attempting to shorten) the operation.

```js
var a = 1;
a === 1 ? alert('Hey, it is 1!') : 0;
```

As you see, if (a === 1) alert('Hey, it is 1!'); would do the same thing. It would be just a char longer, since
it doesn't need an obligatory else condition. If an else condition was involved, the ternary method would be much
cleaner.

```js
a === 1 ? alert('Hey, it is 1!') : alert('Weird, what could it be?');
if(a === 1) alert('Hey, it is 1!') else alert('Weird, what could it be?')
```

Ternaries can be nested to encapsulate additional logic. For example

```js
foo ? bar ? 1 : 2 : 3
//To be clear, this is evaluated left to right
// and can be more explicity expressed as:
foo ? (bar ? 1 : 2) : 3
```

This is the same as the following if/else

```JS
if(foo){
	if(bar){
		1
	} else{
		2
	}
}else{
	3
}
```

Stylistically this should only be used with short variable names, as multi-line ternaries can drastically decrease
readability.
The only statements which cannot be used in ternaries are control statements. For example, you cannot use return
or break with ternaries. The following expression will be invalid.

```js
var animal = 'kitty';
for(var i = 0; i < 5; ++i){
	(animal === 'kitty') ? break:console.log(i);
}
```

For return statements, the following would also be invalid:

```js
var animal = 'kitty';
(animal === 'kitty') ? return 'meow' : return 'woof';
```

To do the above properly, you would return the ternary as follows:

```js
var animal = 'kitty';
return(animal === 'kitty') ? 'meow' : 'woof';
```

## Switch statement
Switch statements compare the value of an expression against 1 or more values and executes diﬀerent sections of
code based on that comparison.

```js
var value = 1;
switch(value){
	case 1:
		console.log('I will always run');
		break;
	case 2:
		console.log('I will never run');
		break;
}
```

The break statement "breaks" out of the switch statement and ensures no more code within the switch statement
is executed. This is how sections are deﬁned and allows the user to make "fall through" cases.

```js
switch(value){
	case 1:
		console.log('I will only run if value === 1');
	case 2:
		console.log('I will run if value === 1 or value === 2');
		break;
	case 3:
		console.log('I will only run if value === 3');
		break;
}
```

The last case is the default case. This one will run if no other matches were made.

```js
var animal = 'Lion';
switch(animal){
	case 'Dog':
		console.log('I will not run since animal !== "Dog"');
		break;
	case 'Cat':
		console.log('I will not run since animal !== "Cat"');
		break;
	default:
		console.log('I will run since animal does not match any other case');
}
```

It should be noted that a case expression can be any kind of expression. This means you can use comparisons,
function calls, etc. as case values.

````js
function john(){
	return 'John';
}
function jacob(){
	return 'Jacob';
}
switch(name){
	case john():
		console.log('I will run if name === "John"');
		break;
	case 'Ja' + 'ne'://Concatenate the strings together then compare (name === "Jane")
		console.log('I will run if name === "Jane"');
		break;
	case john() + ' ' + jacob() + ' Jingleheimer Schmidt':
		console.log('His name is equal to name too!');
		break;
}
````

Multiple Inclusive Criteria for Cases
Since cases "fall through" without a break or return statement, you can use this to create multiple inclusive criteria:

```js
var x = "c"
switch(x){
	case "a":
	case "b":
	case "c":
		console.log("Either a,b, or c was selected.");
		break;
	case "d":
		console.log("Only d was selected.");
		break;
	default: 
		console.log("No case was matched.");
		break; // precautionary break if case order changes
}
```

## If / Else If / Else Control
In its most simple form, an if condition can be used like this:

```js
var i = 0;
if(i < 1){
	console.log("i is smaller than 1");
}
```

The condition i < 1 is evaluated, and if it evaluates to true the block that follows is executed. If it evaluates to
false , the block is skipped.
An if condition can be expanded with an else block. The condition is checked once as above, and if it evaluates to
false a secondary block will be executed (which would be skipped if the condition were true ). An example:

```js
if(i < 1){
	console.log("i is smaller than 1");
}else{
	console.log("i was not smaller than 1")
}
```

Supposing the else block contains nothing but another if block (with optionally an else block) like this:

```js
if(i < 1){
	console.log("i is smaller than 1");
}else{
	if(i < 2){
		console.log("i is smaller than 2");
	}else{
		console.log("non of the previous conditions was true");
	}
}
```

Then there is also a diﬀerent way to write this which reduces nesting:

```js
if(i < 1){
	console.log("i is smaller than 1");
}else if (i < 2){
	console.log("i is smaller than 2");
}else{
	console.log("none of the previous conditions was true");
}
```

## Strategy
A strategy pattern can be used in JavaScript in many cases to replace a switch statement. It is especially helpful
when the number of conditions is dynamic or very large. It allows the code for each condition to be independent
and separately testable.
Strategy object is simple an object with multiple functions, representing each separate condition. Example:

```js
const AnimalSays = {
	dog(){
		reurn 'woof';
	},
	cat(){
		return 'meow';
	},
	lion(){
		return 'roar';
	},
	default(){
		return 'moo';
	}
};
```

The above object can be used as follows:

```js
function makeAnimalSpeak(animal){
	const speak = AnimalSays[animal] || AnimalSays.default;
	console.log(animal + ' says' + speak());
}
```

Result:

```js
makeAnimalSpeak('dog') // 'dog says woof'
makeAnimalSpeak('cat') // 'cat says meow'
makeAnimalSpeak('lion') // 'lion says roar'
makeAnimalSpeak('snake') // 'snake says moo'
```

## Section 11.5: Using || and && short circuiting
The Boolean operators || and && will "short circuit" and not evaluate the second parameter if the ﬁrst is true or
false respectively. This can be used to write short conditionals like:

```js
var x = 0 
x == 10 && alert("x is 10")
x == 10 || alert("x is not 10")
```

# Arrays

## Converting Array-like Objects to Arrays
What are Array-like Objects?
JavaScript has "Array-like Objects", which are Object representations of Arrays with a length property. For example:

```js
var realArray = ['a','b','c'];
var arrayLike = {
	0: 'a',
	1: 'b',
	2: 'c',
	length: 3
};
```

Common examples of Array-like Objects are the arguments object in functions and HTMLCollection or NodeList
objects returned from methods like document.getElementsByTagName or document.querySelectorAll .
However, one key diﬀerence between Arrays and Array-like Objects is that Array-like objects inherit from
Object.prototype instead of Array.prototype . This means that Array-like Objects can't access common Array
prototype methods like forEach() , push() , map() , filter() , and slice() :

```js
var parent = document.getElementById('myDropDown');
var desiredOption = parent.querySelector('option[value = "desired"]');
var domList = parent.children;

domList.indexOf(desiredOption);
domList.forEach(function(){
	arguments.map(/* Stuff here */)
});
```

## Mapping values
It is often necessary to generate a new array based on the values of an existing array.
For example, to generate an array of string lengths from an array of strings:

```js
['one','two','three','four'].map(function(value,index,arr){
	return value.lenght;
});
// => [3,3,5,4]
['one','two','three','four'].map(value => value.lenght);
```

## Filtering Object Arrays
The filter() method accepts a test function, and returns a new array containing only the elements of the original
array that pass the test provided.

```js
var numbers = [5,32,43,4];
var odd = numbers.filter(function(n){
	return n % 2 !== 0;
});

let odd = numbers.filter(n => n % 2 !== 0);//can be shortened to (n => n % 2)
```

## Sorting Arrays
The .sort() method sorts the elements of an array. The default method will sort the array according to string
Unicode code points. To sort an array numerically the .sort() method needs to have a compareFunction passed to
it.

**Default Sort**
Sorts the array in UNICODE order.

```js
['s', 't', 'a', 34, 'K', 'o', 'v', 'E', 'r', '2', '4', 'o', 'W', -1, '-4'].sort();
```

Results in:

```js
[-1, '-4', '2', 34, '4', 'E', 'K', 'W', 'a', 'l', 'o', 'o', 'r', 's', 't', 'v']
```

**Alphabetical Sort**

```js
['s', 't', 'a', 'c', 'K', 'o', 'v', 'E', 'r', 'f', 'l', 'W', '2', '1'].sort((a, b) => {
return a.localeCompare(b);
});
```

Results in:

```js
['1', '2', 'a', 'c', 'E', 'f', 'K', 'l', 'o', 'r', 's', 't', 'v', 'W']
```

**String sorting by length (longest ﬁrst)**

```js
[["zebras", "dogs", "elephants", "penguins"].sort(function(a, b) {
return b.length - a.length;
});]
```

Results in

```js
["elephants", "penguins", "zebras", "dogs"];
```

**String sorting by length (shortest ﬁrst)**

```js
["zebras", "dogs", "elephants", "penguins"].sort(function(a, b) {
return a.length - b.length;
});
```

Result in

```js
["dogs","zebras","penguins", "elephants"];
```

**Numerical Sort (ascending)**

```js
[100,1000,10,10000,1].sort(function(a,b){
	return a - b;
});
```

Results in:

```js
[1,10,100,1000,10000]
```

**Numerical Sort (descending)**

```js
[100,1000,10,10000,1].sort(function(a,b){
	return b -a;
});
```

Results in:

```js
[10000,1000,100,10,1]
```

**Sorting array by even and odd numbers**

```js
[10,21,4,15,7,99,0,12].sort(function(a,b){
	return(a & 1) - (b & 1) || a - b;
});
```

Results in:

```js
[0,4,10,12,7,15,21,99]
```

**Date Sort (descending)**

```js
var dates = [
	new Date(2007,11,10),
	new Date(2014,2,21),
	new Date(2009,6,11),
	new Date(2016,7,23)
];
dates.sort(function(a,b){
	if(a > b) return -1;
	if(a < b) return 1;
	return 0;
});
dates.sort(function(a,b){
	return b-a;
});
```

Results in:

![image-20210706103729819](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210706103729819.png)

## Destructuring an array

An array can be destructured when being assigned to a new variable.

```js
const triangle = [3,4,5];
const [length,height,hypotenuse] = triangle;
length === 3;			// true
height === 4;			//true
hypotneuse === 5;		//true
```

## Array comparison
For simple array comparison you can use JSON stringify and compare the output strings:

```js
JSON.stringify(array1) === JSON.stringify(array2)
```

You can use a recursive function to compare arrays.

```js
function compareArrays(array1, array2){
	var i, isA1,isA2;
	isA1 = Array.isArray(array1);
	isA2 = Array.isArray(array2);
	
	if(isA1 !== isA2){
		return false;
	}
	if(!(isA1 && isA2)){
		return array1 === array2;
	}
	if(array1.lenght !== array2.lenght){
		return false;
	}
	for(i = 0; i < array1.length; i += 1){
		if(!compareArrays(array1[i], array2[i])){
			return false;
		}
	}
	return true;
}
```

**WARNING**: Using the above function is dangerous and should be wrapped in a try catch if you suspect there is a
chance the array has cyclic references (a reference to an array that contains a reference to itself)

```js
a = [0];
a[1] = a;
b = [0, a];
```

## Reversing arrays
.reverse is used to reverse the order of items inside an array.

Example for .reverse:

```js
[1,2,3,4].reverse();
```

Result in:

```js
[4,3,2,1]
```

You can also reverse an array 'deeply' by:

```js
function deepReverse(arr){
	arr.reverse().forEach(elem => {
		if(Array.isArray(elem)){
			deepReverse(elem);
		}
	});
	return arr;
}
var arr = [1, 2, 3, [1, 2, 3, ['a', 'b', 'c']]];
deepReverse(arr);

OUTPUT:
[[['c','b','a'],3,2,1],3,2,1]
```

## Shallow cloning an array
Sometimes, you need to work with an array while ensuring you don't modify the original. Instead of a clone
method, arrays have a slice method that lets you perform a shallow copy of any part of an array. Keep in mind
that this only clones the ﬁrst level. This works well with primitive types, like numbers and strings, but not objects.
To shallow-clone an array (i.e. have a new array instance but with the same elements), you can use the following
one-liner:

````js
var clone = arrayToClone.slice();
````

This calls the built-in JavaScript Array.prototype.slice method. If you pass arguments to slice , you can get more
complicated behaviors that create shallow clones of only part of an array, but for our purposes just calling slice()
will create a shallow copy of the entire array.
All method used to convert array like objects to array are applicable to clone an array:

```js
arrayToClone = [1,2,3,4,5];
clone1 = Array.from(arrayToClone);
clone2 = Array.of(...arrayToClone);
clone2 = [...arrayToClone]
```

```js
arrayToClone = [1,2,3,4,5];
clone1 = Array.prototype.slice.call(arrayToClone);
clone2 = [].slice.call(arrayToClone);
```

## Concatenating Arrays

**Two Arrays**

```js
var array1 = [1,2];
var array2 = [3,4,5];
var array3 = array1.concat(array2);
OUTPUT:
[1,2,3,4,5]
```

**Multiple Arrays**

```js
var array1 = ["a","b"],
	array2 = ["c","d"],
	array3 = ["e","f"],
	array4 = ["g","h"];
var arrConc  = array1.concat(array2,array3,array4);
```

**Without Copying the First Array**

```js
var longArray = [1,2,3,4,5,6,7,8],
	shortArray = [9,10];
```

**Array and non-array values**

```js
var arr1 = ["a","b"];
var arr2 = ["e","f"];
var arrConc = arr1.concat("c","d",arr2);
OUTPUT:
["a","b","c","d","e","f"]
```

## Merge two array as key value pair
When we have two separate array and we want to make key value pair from that two array, we can use array's
reduce function like below:

```js
var columns = ["Date","Number","Size","Location","Age"];
var rows = ["2001","5","Big","Sydney","25"];
var result = rows.reduce(function(result,field,index){
	result[columns[index]] = field;
	return;
},{})
console.log(result);
OUTPUT:
{
	Date: "2001",
	Number: "5",
	Size: "Big",
	Location: "Sydney",
	Age: "25"
}
```

## Filtering values

The filter() method creates an array ﬁlled with all array elements that pass a test provided as a function.

```js
[1,2,3,4,5].filter(function(value,index,arr){
	return value > 2;
});
[1,2,3,4,5].filter(value => value > 2);
OUTPUT:
[3,4,5]
```

This example utilises the same concept of passing a function that takes one argument

```js
function startsWithLetterA(str){
	if(str && str[0].toLowerCase() == 'a'){
		return true
	}
	return false;
}
var str = 'Since Boolean is a native javascript function/constructor that takes [one optional parameter] and the filter method also takes a function and passes it the current array item as a parameter, you could read it like the following';
var strArray = str.split(" ");
var wordsStartsWhithA = strArray.filter(startsWithLetterA);
OUTPUT:
["a","and","also","a","and","array","as"]
```

## Convert a String to an Array
The .split() method splits a string into an array of substrings. By default .split() will break the string into
substrings on spaces ( " " ), which is equivalent to calling .split(" ") .
The parameter passed to .split() speciﬁes the character, or the regular expression, to use for splitting the string.
To split a string into an array call .split with an empty string ( "" ). Important Note: This only works if all of your
characters ﬁt in the Unicode lower range characters, which covers most English and most European languages. For
languages that require 3 and 4 byte Unicode characters, slice("") will separate them.

```js
var strArray = "StackOverflow".split("");
OUTPUT
strArray = ["S", "t", "a", "c", "k", "O", "v", "e", "r", "f", "l", "o", "w"]
```

Using the spread operator ( ... ), to convert a string into an array .

```js
var strArray = [..."sky is blue"];
// strArray = ["s","k","y"," ","i","s"," ","b","l","u","e"]
```

## Removing items from an array

**Shift**

Use .shift to remove the ﬁrst item of an array.
For example:

```js
var array = [1,2,3,4];
array.shift();
OUTPUT:
[2,3,4]
```

**Pop**

Further .pop is used to remove the last item from an array.
For example:

```js
var array = [1,2,3];
array.pop();
OUTPUT:
[1,2]
```

**Splice**

Use .splice() to remove a series of elements from an array. .splice() accepts two parameters, the starting
index, and an optional number of elements to delete. If the second parameter is left out .splice() will remove all
elements from the starting index through the end of the array.
For example:

```js
var array = [1,2,3,4];
array.splice(1,2);
```

OUTPUT:
![image-20210706113900168](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210706113900168.png)

**Delete**

Use delete to remove item from array without changing the length of array:

```js
var array = [1,2,3,4,5];
console.log(array.length);//5
delete array[2];
console.log(array); //[1,2,undefined,4,5]
console.log(array.legth);
```

**Array.prototype.length**

Assigning value to length of array changes the length to given value. If new value is less than array length items will
be removed from the end of value.

```js
array = [1,2,3,4,5];
array.length = 2;
console.log(array); //[1,2]
```

## Removing all elements

Care must be taken as this does not remove any items from the original array. The array may have been closed
over when passed to a function. The array will remain in memory for the life of the function though you may not be
aware of this. This is a common source of memory leaks.
Example of a memory leak resulting from bad array clearing:

```js
var count = 0;
function addListener(arr){ // arr is closed over
	 var b = document.body.querySelector("#foo" + (count++));
	 b.addEventListener("click",function(e){ // this function reference keeps
	 	// the closure current while the 
	 	// event is active 
	 	// do something but does not need arr
	 });
}
arr = ["big data"];
var i = 100;
while(i > 0){
	addListener(arr); // the array is passed to the function
	arr = [];
	array.push("some large data"); // more memory allocated
	i--;
}
// there are now 100 arrays closed over, each referencing a different array
// no a single item has been deleted
```

To prevent the risk of a memory leak use the one of the following 2 methods to empty the array in the above
example's while loop.

**Method 2**

Setting the length property deletes all array element from the new array length to the old array length. It is the
most eﬃcient way to remove and dereference all items in the array. Keeps the reference to the original array

```js
arr.length = 0;
```

**Method 3**

Similar to method 2 but returns a new array containing the removed items. If you do not need the items this
method is ineﬃcient as the new array is still created only to be immediately dereferenced.

```js
arr.splice(0); //should not use if you don't want the removed items
//only use this method if you do the following 
var keepArr = arr.splice(0);//empties the array and creates a new array containing the
							// removed items
```

## Finding the minimum or maximum element
If your array or array-like object is numeric, that is, if all its elements are numbers, then you can use Math.min.apply
or Math.max.apply by passing null as the ﬁrst argument, and your array as the second.

```js
var myArray = [1,2,3,4];
Math.min.apply(null,myArray);//1
Math.max.apply(null,myArray);//4
```

In ES6 you can use the ... operator to spread an array and take the minimum or maximum element.

```js
var myArray = [1,2,3,4,99,20];
var maxValue = Math.max(...myArray); // 99
var minValue = Math.min(...myArray); // 1
```

The following example uses a for loop:

```js
var maxValue = myArray[0];
for(var i = 1; i < myArray.length; i++){
	var currentValue = myArray[i];
	if(currentValue > maxValue){
		maxValue = currentValue;
	}
}
```

The following example uses Array.prototype.reduce() to ﬁnd the minimum or maximum:

```js
var myArray = [1,2,3,4];
myArray.reduce(function(a,b){
	return Math.min(a,b);
});// 1
myArray.reduce(function(a,b){
	return Math.max(a,b);
});// 4
```

or using arrow functions:

```js
myArray.reduce((a,b) => Math.min(a,b)); //1
myArray.reduce((a,b) => Math.max(a,b)); //4
```

To generalize the reduce version we'd have to pass in an initial value to cover the empty list case:

```js
function myMax(array){
	return array.reduce(function(maxSoFar, element){
		return Math.max(maxSoFar, element);
	}, -Infinity);
}
myMax([3,5]);				// 5
myMax([]);					//-Infinity					
Math.max.apply(null, []);	// -Infinity
```

## Joining array elements in a string

To join all of an array's elements into a string, you can use the join method:

```js
console.log(["Hello," ","world"].join("")); // "Hello world"
console.log([1,800,555,1234].join("-"));  //"1-800-555-1234"
```

## Removing/Adding elements using splice()
The splice() method can be used to remove elements from an array. In this example, we remove the ﬁrst 3 from
the array.

```js
var values = [1,2,3,4,5,3];
var i = values.indexOf(3);
if(i >= 0){
	values.splice(i,1);
}
// [1,2,4,5,3]
```

The splice() method can also be used to add elements to an array. In this example, we will insert the numbers 6,
7, and 8 to the end of the array.

```js
var values = [1,2,4,5,3];
var i = values.length + 1;
values.splice(i,0,6,7,8);
//[1,2,4,5,3,6,7,8]
```

## The entries() method
The entries() method returns a new Array Iterator object that contains the key/value pairs for each index in the
array.

```js
var letters = ['a','b','c'];
for(const[index,element] of letters.entries()){
	console.log(index,element);
}
OUTPUT:
0 "a"
1 "b"
2 "c"
```

## Append / Prepend items to Array

**Unshift**

Use .unshift to add one or more items in the beginning of an array.
For example:

```js
var array = [3,4,5,6];
array.unshift(1,2);
OUTPUT:
[1,2,3,4,5,6]
```

**Push**

Further .push is used to add items after the last currently existent item.
For example:

```js
var array = [1,2,3];
array.push(4,5,6);
OUTPUT:
[1,2,3,4,5,6]
```

## Object keys and values to array

```js
var object = {
	key1: 10,
	key2: 3,
	key3: 40,
	key4: 20
};
var array = [];
for(var people on object){
	array.push([people,object[people]]);
}
OUTPUT:
[
	["key1", 10],
	["key2", 3],
	["key3", 40],
	["key4", 20]
]
```

## Logical connective of values

.some and .every allow a logical connective of Array values.
While .some combines the return values with OR , .every combines them with AND .
Examples for .some

```js
[false,false].some(function(value){
	return value;
});
// result: false
[false, true].some(function(value){
	return value;
});
//result: true
[true,true].some(funtion(value){
	result value;
});
//result: true;
And examples for .every
[false,false].every(function(value){
	return value;
});
// result false
[false, true].every(function(value){
	return value;
});
// Result false
[true,true].every(function(value){
	return value;
});
// Result: true
```

## Section 12.30: Checking if an object is an Array
Array.isArray(obj) returns true if the object is an Array , otherwise false .

```js
Array.isArray([])				// true
Array.isArray([1,2,3])			// true
Array.isArray({})				// false
Array.isArray(1)				// false
```

## Insert an item into an array at a speciﬁc index
Simple item insertion can be done with Array.prototype.splice method:

```js
arr.splice(index, 0, item);
```

More advanced variant with multiple arguments and chaining support:

```js
Array.prototype.insert = function(index){
	this.splice.apply(this, [index, 0].concat(Array.prototype.slice.call(arguments,1)));
	return this;
};
["a","b","c","d"].insert(2,"X","Y","Z").slice(1,6);		//["b","X","Y","Z","c"]
```

## Sorting multidimensional array

```js
var array = [
	["key1", 10],
	["key2", 3],
	["key3", 40],
	["key4",20]
];
array.sort(funcion(a,b){
	return a[1] - b[1];
})
array.sort((a,b) => a[1] - b[1]);
OUTPUT:
[
	["key2", 3]
	["key1", 10]
	["key4", 20]
	["key3", 40]
]
```

## Test all array items for equality
The .every method tests if all array elements pass a provided predicate test.
To test all objects for equality, you can use the following code snippets.

```js
[1,2,1].every(function(item, i, list){return item === list[0];}); //false
[1,1,1].every(function(item,i,list){return item === list[0];}); //true
[1,1,1].every((item,i,list) => item === list[0]); //true
```

## Copy part of an Array

The slice() method returns a copy of a portion of an array.
It takes two parameters, arr.slice([begin[, end]]) :
begin
Zero-based index which is the beginning of extraction.
end
Zero-based index which is the end of extraction, slicing up to this index but it's not included.
If the end is a negative number, end = arr.length + end .

**Example 1**

```js
var arr = ["a","b","c","d" ...];
var newArr = arr.slice(0,2); // newArr === ["a","b"]
```

**Example 2**

```js
var arr = [0,1,2,3,4,5,6,7,8,9...];
// I want to slice this Array starting from
// number 5 to its end
var newArr = arr.slice(4); // newArr === [5,6,7,8,9...]
```

# Objects

## Shallow cloning

If you need to support older versions of JavaScript, the most-compatible way to clone an Object is by manually
iterating over its properties and ﬁltering out inherited ones using .hasOwnProperty() .

```js
var existing = {a: 1,b: 2,c: 3};
var clone = {};
for(var prop in existing){
	if(existing.hasOwnProperty(prop)){
		clone[prop] = existing[prop];
	}
}
```

## Object.freeze

Object.freeze makes an object immutable by preventing the addition of new properties, the removal of existing
properties, and the modiﬁcation of the enumerability, conﬁgurability, and writability of existing properties. It also
prevents the value of existing properties from being changed. However, it does not work recursively which means
that child objects are not automatically frozen and are subject to change.

```js
var obj = {
	foo: 'foo',
	bar: [1,2,3],
	bar: {
		foo: 'nested-foo'
	}
};
Object.freeze(obj);
obj.newProperty = true;
obj.foo = 'not foo';
Object.defineProperty(obj, 'foo',{
    writable: true;
});
delete obj.foo;
obj.bar.push(4);
obj.baz.foo = 'new foo';
```

## Object cloning
When you want a complete copy of an object (i.e. the object properties and the values inside those properties,
etc...), that is called deep cloning.
Version ≥ 5.1
If an object can be serialized to JSON, then you can create a deep clone of it with a combination of JSON.parse and
JSON.stringify :

```js
var existing  = {a: 1, b: {c: 2}};
var copy = JSON.parse(JSON.stringify(existing));
existing.b.c = 3; //copy.b.c will not change
```

Assuming that you have a "nice" object whose properties only contain primitive values, dates, arrays, or other "nice"
objects, then the following function can be used for making deep clones. It is a recursive function that can detect
objects with a cyclic structure and will throw an error in such cases.

```js
function deepClone(obj){
	function clone(obj, traverseObjects){
		var copy;
		if(obj === null || typeof obj !== "object"){
		throw new Error("Cannot clone circular object.");
		}
	
        if(obj instanceof Date){
            copy = new Date();
            copy.setTime(obj.getTime());
            return copy;
        }
        if(obj instanceof Array){
            copy = [];
            for(var i = 0; i < obj.length; i++){
                copy.push(clone(obj[i],traversedObjects.concat(obj)));
            }
            return copy;
        }
        // simple objects
        if(obj instanceof Object){
            copy = {};
            for(var key in obj){
                if(obj.hasOwnProperty(key)){
                    copy[key] = clone(obj[key], traversedObjects.concat(obj));
                }
            }
            return copy;
        }
        throw new Error("Not a cloneable object.");
    }
    return clone(obj,[]);
}
```

## Object.assign
The Object.assign() method is used to copy the values of all enumerable own properties from one or more source
objects to a target object. It will return the target object.
Use it to assign values to an existing object:

```js
var user = {
	firstName: "Jhon"
};
Object.assign(user, {lastName: "Doe", age:39});
console.log(user);//Logs: {firstName: "John",lastName: "Doe", age: 39}
```

Or merge many properties from multiple objects to one:

![image-20210706142806572](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210706142806572.png)

## Accesor properties (get and set)
Version ≥ 5
Treat a property as a combination of two functions, one to get the value from it, and another one to set the value in
it.
The get property of the property descriptor is a function that will be called to retrieve the value from the property.
The set property is also a function, it will be called when the property has been assigned a value, and the new value
will be passed as an argument.
You cannot assign a value or writable to a descriptor that has get or set

```js
var person = {name: "John", surname: "Doe"};
Object.defineProperty(person,fullName,{
	get: function(){
		return this.name + " " + this.surname;
	},
	set: function(value){
		[this.name, this.surname] = value.split(" ");
	}
});
console.log(person.fullName); // "Jhon Doe"

person.surname = "Hill";
console.log(person.fillName); // "Jhon Hill"

person.fullName = "Mary Jones";
console.log(person.name) // "Mary"
```

## Dynamic / variable property names
Sometimes the property name needs to be stored into a variable. In this example, we ask the user what word needs
to be looked up, and then provide the result from an object I've named dictionary .

```js
var dictionary = {
	lettuce: 'a veggie',
	banana: 'a fruit',
	tomato: 'it depends on who you ask',
	apple: 'a fruit',
	Apple: 'Steve Jobs rocks' // properties are case-sensitive
}
var word = prompt('What word would you like to look up today?')
var definition = dictionary[word]
alert(word + '\n\n'+ definition)
```

## Convert object's values to array

Given this object

```js
var obj = {
	a: "hello",
	b: "this is",
	c: "javascript!"
};
var array = Object.keys(obj)
	.map(function(key){
		return obj[key];
});
console.log(array); // ["hello", "this is", "javascript!"]
```

## Retrieving properties from an object
Characteristics of properties :
Properties that can be retrieved from an object could have the following characteristics,
			Enumerable
			Non - Enumerable
			own
While creating the properties using Object.deﬁneProperty(ies), we could set its characteristics except "own".
Properties which are available in the direct level not in the prototype level ( __proto__ ) of an object are called as own
properties.
And the properties that are added into an object without using Object.defindProperty(ies) will don't have its
enumerable characteristic. That means it be considered as true.

**Methods of retrieving properties :**
Properties from an object could be retrieved by the following methods,

1. for..in loop
    This loop is very useful in retrieving enumerable properties from an object. Additionally this loop will retrieve
    enumerable own properties as well as it will do the same retrieval by traversing through the prototype chain
    until it sees the prototype as null.

  ```js
  var x = {a : 10, b : 3}, pros = [];
  for(prop in x){
  	prop.push(prop);
  }
  console.log(props); //["a","b"]
  //Ex 2: Data with enumerable properties in prototype chain
  var x = {a : 10, __proto__: {b : 10}}, props = [];
  for(prop in x){
  	props.push(prop);
  }
  console.log(props); //["a","b"]
  // Ex 3: Data with non enumerable roperties
  var x = {a : 10}, props = [];
  Object.defineProperty(x,"b",{value:5, enumerable:false});
  for(prop in x){
  	props.push(prop);
  }
  console.log(props) //["a"]
  ```

  ## Read-Only property

  Using property descriptors we can make a property read only, and any attempt to change its value will fail silently,
  the value will not be changed and no error will be thrown.
  The writable property in a property descriptor indicates whether that property can be changed or not.

  ![image-20210706150320338](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210706150320338.png)

  

## Non enumerable property

We can avoid a property from showing up in for (... in ...) loops
The enumerable property of the property descriptor tells whether that property will be enumerated while looping
through the object's properties.

![image-20210706150742485](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210706150742485.png)

## Descriptors and Named Properties
Properties are members of an object. Each named property is a pair of (name, descriptor). The name is a string that
allows access (using the dot notation object.propertyName or the square brackets notation
object['propertyName'] ). The descriptor is a record of ﬁelds deﬁning the bevahiour of the property when it is
accessed (what happens to the property and what is the value returned from accessing it). By and large, a property
associates a name to a behavior (we can think of the behavior as a black box).

Example:

```js
var obj = {propertyName1: 1};
Object.defineProperty(obj,'propertyName2',{get:function() {
	console.log('this will be logged every time propertyName2 is accessed to get its value');},
	set: function(){
		console.log('and this will be logged every time property Name2\'s value is tried to be set')
}});
obj.propertyName1 = 3;
console.log(obj.propertyName1); //3
obj.propertyName2 = 3;
console.log(obj.propertyName2);
```

## Object.keys

Object.keys(obj) returns an array of a given object's keys.

```js
var obj = {
	a: "hello",
	b: "this",
	c: "javascript!"
};
var keys = Object.keys(obj);
console.log(keys);//["a","b","c"]
```

## Creating an Iterable object

```js
var myIterableObject = {};
myIterableObject[Symbol.iterator] = function(){
	return{
		next: function(){
			if(!this.iterated){
				this.iterated = true;
				return{
					done: false,
					value: 'One'
				};
			}
			return{
				done: true
			};
		},
		iterated: false
	};
};
for(var c of myIterableObject){
	console.log(c);
}
```

## Object.values()

The Object.values() method returns an array of a given object's own enumerable property values, in the same
order as that provided by a for...in loop (the diﬀerence being that a for-in loop enumerates properties in the
prototype chain as well).

```js
var obj = {0: 'a',1: 'b',2: 'c'};
console.log(Object.values(obj));// ['a','b','c']
```

# Arithmetic (Math)

## Remainder / Modulus (%)
The remainder / modulus operator ( % ) returns the remainder after (integer) division.

```js
console.log(42 % 10);  // 2
console.log(42 % -10); // 2
console.log(-42 % 10);  // -2
console.log(-42 % -10);  // -2
console.log(-40 % 10);  // -0
console.log(40 % 10);  // 0
```

## Rounding
**Rounding**
Math.round() will round the value to the closest integer using half round up to break ties.

```js
var a = Math.round(2.3);		// a is now 2
var b = Math.round(2.7);		// b is now 3
var c = Math.round(2.5);		// c is now 3
var d = Math.round(-2.7);		// d is now -3
var e = Math.roun(-2.5);		// e is now -2
```

**Rounding up**
Math.ceil() will round the value up.

```js
var a = Math.ceil(2.3);		// a is now 3
var b = Math.ceil(2.7);		// b is now 3
var c = Math.ceil(-1.1);	// c is now 1
```

**Rounding down**
Math.floor() will round the value down.

```js
var a = Math.floor(2.3);		// a is now 2
var b = Math.floor(2.7);		// b is now 2
var c = Math.floor(-1.1);		// c is now -1
```

**Truncating**
Caveat: using bitwise operators (except >>> ) only applies to numbers between -2147483649 and 2147483648 .

```js
Math.trunc(2.3);			//2(floor)
Math.trunc(-2.3);			//-2 (ceil)
Math.trunc(2147483648.1);	// 2147483648 (floor)
Math.trunc(-2147483649.1);	// 2147483649 (ceil)
Math.trunc(NaN);
```

## Incrementing (++)
The Increment operator ( ++ ) increments its operand by one.
If used as a postﬁx, then it returns the value before incrementing.
If used as a preﬁx, then it returns the value after incrementing.

```js
// postfix
var a = 5,		//5
	b = a++		//5
	c = a		//6
```

In this case, a is incremented after setting b . So, b will be 5, and c will be 6.

```js
// prefix
var a = 5,		// 5
	b = ++a		// 6
	c = a		// 6
```

## Little / Big endian for typed arrays when using bitwise operators
Example where Endian type is important

```js
var canvas = document.createElement("canvas");
var ctx = canvas.getContext("2D");
var imgData = ctx.getImageData(0,0,canvas.width,canvas.height);

var buf32 = new Uint32Array(imgData.data.buffer);
var mask = 0x00ff00ff;
if(isLittleEndian){
	mask = 0xff00ff00;
}
var len = buf32.length;
var i = 0;
while(i < len){
	buf32[i] &= mask;
}
ctx.putImageData(imgData);
```

## Get Random Between Two Numbers

Examples:

```js
// random between (0,10)
Math.floor(Math.random() * 11);
// random between (1,10)
Math.floor(Math.random() * 10) + 1;
//random beetwen(5,20);
Math.floor(Math.random()* 16) +5;
// random between (-10,-2)
Math.floor(Math.random() * 9) - 10;
```

## Simulating events with different probabilities
Sometimes you may only need to simulate an event with two outcomes, maybe with diﬀerent probabilities, but you
may ﬁnd yourself in a situation that calls for many possible outcomes with diﬀerent probabilities. Let's imagine you
want to simulate an event that has six equally probable outcomes. This is quite simple.

```js
function simulateEvent(numEvents){
	var event = Math.floor(numEvents*Math.random());
	return event;
}
console.log("Rolled a " + (simulateEvent(6)+1)); //Rolled a 2
```

However, you may not want equally probable outcomes. Say you had a list of three outcomes represented as an
array of probabilities in percents or multiples of likelihood. Such an example might be a weighted die. You could
rewrite the previous function to simulate such an event.

```js
function simulateEvent(changes){
	var sum = 0;
	chances.forEach(function(chase){
		sum+=chance;
	});
	var rand = Math.random();
	var chance = 0;
	for(var i=0; i<chances.length; i++){
		chance+=chances[i]/sum;
		if(rand<chance){
			return i;
		}
	}
	return -1;
}
console.log("Rolled a " + (simulateEvent([1,1,1,1,1,2]) + 1)); // Rolled a 1
console.log("Rolled a" + (simulateEvent([1/7,1/7,1/7,1/7,1/7,2/7]) + 1)); //Rolled a 6


```

## Ceiling and Floor
**ceil()**
The ceil() method rounds a number upwards to the nearest integer, and returns the result.
**Syntax:**

```js
Math.ceil(n);
```

**Example:**

```js
console.log(Math.ceil(0.60));	// 1
console.log(Math.ceil(0.40));	// 1
console.log(Math.ceil(5.1));	// 6
console.log(Math.ceil(-5.1));	// -5
console.log(Math.ceil(-5.9));	// -5
```

**floor()**
The floor() method rounds a number downwards to the nearest integer, and returns the result.

**Example:**

```js
console.log(Math.floor(0.60));	// 0
console.log(Math.floor(0.40));	// 0
console.log(Math.floor(5.1));	// 5
console.log(Math.floor(-5.1));	// -6
console.log(Math.floor(-5.9));	// -6
```

# Bitwise operators

## Bitwise operators
Bitwise operators perform operations on bit values of data. These operators convert operands to signed 32-bit
integers in two's complement.

**Conversion to 32-bit integers**

Numbers with more than 32 bits discard their most signiﬁcant bits. For example, the following integer with more
than 32 bits is converted to a 32-bit integer:

```
Before: 10100110111110100000000010000011110001000001
After:				10100000000010000011110001000001
```

**Real world example: Number's Parity Check**
Instead of this "masterpiece" (unfortunately too often seen in many real code parts):

```js
function isEven(n){
	return n % 2 == 0;
}
function isOdd(n){
	if(isEven(n)){
		return false;
	}else{
		return true;
	}
}
```

# Declarations and Assignments

## Modifying constants
Declaring a variable const only prevents its value from being replaced by a new value. const does not put any
restrictions on the internal state of an object. The following example shows that a value of a property of a const
object can be changed, and even new properties can be added, because the object that is assigned to person is
modiﬁed, but not replaced.

```js
const person = {
	name: "John"
};
console.log('The name of the person is', person.name);

person.name = "Steve";
console.log('The name of the person is',person.name);

person.surname = "Fox";
console.log('The name of the person is', person.name,'and the surname is',person.surname);
OUTPUT:
The name of the person is Jhon
The name of the person Steve
The name of the person is Steve and the surname is Fox
```

# Loops

**Standard usage**

```js
for(var i = 0; i < 100; i++){
	console.log(i);
}
OUTPUT:
1
2
3
...
99
```

**Multiple declarations**
Commonly used to cache the length of an array.

```js
var array = ['a','b','c'];
for(var i = 0; i < array.length;i++){
	console.log(array[i]);
}
OUTPUT:
'a'
'b'
'c'
```

**Changing the increment**

```js
for(var i = 0; i < 100; i += 2){
	console.log(i);
}
OUTPUT:
0
2
4
...
98
```

**Decremented loop**

```js
for(var i = 100; i >= 0; i--){
	console.log(i);
}
OUTPUT:
100
99
98
...
0
```

## "for ... of" loop

```js
const iterable = [0,1,2];
for(let i of iterable){
	console.log(i);
}
OUTPUT:
0
1
2
```

**Support of for...of in other collections**
**Strings**
for...of will treat a string as a sequence of Unicode characters:

```js
const string = "abc";
for(let chr of string){
	console.log(chr);
}
OUTPUT:
a b c
```

**Maps**
You can also use for...of loops to iterate over Maps. This works similarly to arrays and sets, except the iteration
variable stores both a key and a value.

```js
const map = new Map()
	.set('abc', 1)
	.set('def', 2)
for(const iteration of map){
	console.log(iteration)
}
OUTPUT:
["abc", 1]
["def", 2]
```

**Objects**
for...of loops do not work directly on plain Objects; but, it is possible to iterate over an object’s properties by
switching to a for...in loop, or using Object.keys() :

```js
const someObject = {name: 'Mike'};
for(let key of Object.keys(someObject)){
	console.(key + ": " + someObject[key]);
}
OUTPUT:
name: Mike
```

## "for ... in" loop

```js
var object = {"a":"foo","b":"bar","c":"baz"};
Object.defineProperty(object, 'a',{
	enumerable: false,
});
for(var key in object){
	if(object.hasOwnProperty(key)){
		console.log('object.' + key + ', ' + object[key]);
	}
}
OUTPUT:
object.b, bar
object.c, baz
```

## "while" Loops

**Standard While Loop**
A standard while loop will execute until the condition given is false:

```js
var i = 0;
while(i < 100){
	console.log(i);
	i++;
}
OUTPUT:
0
1
...
99
```

**Decremented loop**

```js
var i = 100;
while(i > 0){
	console.log(i);
	i--;
}
OUTPUT:
100
99
98
...
1
```

**Do...while Loop**
A do...while loop will always execute at least once, regardless of whether the condition is true or false:

```js
var i = 101;
do{
	console.log(i);
}while(i < 100);
OUTPUT:
101
```

## "continue" a loop

**Continuing a "for" Loop**

When you put the continue keyword in a for loop, execution jumps to the update expression ( i++ in the example):

```js
for(var i = 0;i < 3; i++){
	if(i === 1){
		continue;
	}
	console.log(i);
}
OUTPUT:
0
2
```

**Continuing a While Loop**
When you continue in a while loop, execution jumps to the condition ( i < 3 in the example):

```js
var i = 0;
while(i < 3){
	if(i === 1){
		i = 2;
		continue;
	}
	console.log(i);
	i++;
}
OUTPUT:
0
2
```

## Break speciﬁc nested loops
We can name our loops and break the speciﬁc one when necessary.

```js
outerloop:
for(var i = 0; i < 3;i++){
	innerloop:
	for(var j = 0; j < 3; j++){
		console.log(i);
		console.log(j);
		if(j == 1){
			break outerloop;
		}
	}
}
OUTPUT:
0
0
0
1
```

# Functions
Functions in JavaScript provide organized, reusable code to perform a set of actions. Functions simplify the coding
process, prevent redundant logic, and make code easier to follow. This topic describes the declaration and
utilization of functions, arguments, parameters, return statements and scope in JavaScript.

## Function Scoping
When you deﬁne a function, it creates a scope.
Everything deﬁned within the function is not accessible by code outside the function. Only code within this scope
can see the entities deﬁned inside the scope.

```js
function foo(){
	var a = 'hello';
	console.log(a); // 'hello'
}
console.log(a); //reference error
```

Nested functions are possible in JavaScript and the same rules apply.

```js
function foo(){
	var a = 'hello';
	function bar(){
        var b = 'world';
        console.log(a);	//'hello'
        console.log(b);	//'world'
	}
	console.log(a);		//'hello'
	console.log(b);		// reference error
}
console.log(a);		//reference error
console.log(b);		//reference error
```

## Named Functions
Functions can either be named or unnamed (anonymous functions):

```js
var namedSum = function sum (a,b){
	return a + b;
}
var anonSum = function(a,b){
	return a + b;
}
namedSum(1,3);
anonSum(1,3);
OUTPUT:
4
4
```

**Named Functions in a recursive scenario**

A recursive function can be deﬁned as:

```js
var say = function(times){
	if(times > 0){
		console.log('Hello!');
		say(times - 1);
	}
}
var sayHelloTimes = say;
sayHelloTimes(2);
OUTPUT:
Hello!
Hello!
```

What if somewhere in your code the original function binding gets redeﬁned?

```js
var say = function(times){
	if(times > 0){
		console.log('Hello!');
		say(times - 1);
	}
}
var sayHelloTimes = say;
say = "oops";
sayHelloTimes(2);
OUTPUT:
Hello!
Uncaught TypeError: say is not a function
```

This can be solved using a named function

```js
var say = function say(times){
	if(times > 0){
		console.log('Hello!');
		say(times - 1);
	}
}
var sayHelloTimes = say;
say = "oops";
sayHelloTimes(2);
OUTPUT:
Hello!
Hello!
```

And as bonus, the named function can't be set to undefined , even from inside:

```js
var say = function say (times){
	// this does nothing
	say = undefined;
	if(times > 0){
		console.log('Hello!');
		say(times - 1);
	}
}
var sayHelloTimes = say;
say = "oops";
sayHelloTimes(2);
Output:
Hello!
Hello!
```

## Binding `this` and arguments

When you take a reference to a method (a property which is a function) in JavaScript, it usually doesn't remember
the object it was originally attached to. If the method needs to refer to that object as this it won't be able to, and
calling it will probably cause a crash.
You can use the .bind() method on a function to create a wrapper that includes the value of this and any number
of leading arguments.

```js
var monitor = {
	treshold: 5,
	chek: function(value){
		if(value > this.treshold){
			this.display("Value is too high!");
		}
	},
	display(message){
		alert(message);
	}
};
monitor.chek(7);
var badChek = monitor.chek;
badChek(15);

var chek = monitor.chek.bind(monitor);
chek(15);

var chek8 = monitor.chek.bind(monitor, 8);
chek8();
```

**Bind Operator**
The double colon bind operator can be used as a shortened syntax for the concept explained above:

```js
var log = console.log.bind(console); // long version
const log = ::console.log; // short version

foo.bar.call(foo); // long version
foo::bar(); // short version

foo.bar.call(foo,arg1,arg2,arg3); // long verion
foo::bar(arg1,arg2,arg3); // short version

foo.bar.apply(foo,args); // long version
foo::bar(...args); // short version
```

This syntax allows you to write normally, without worrying about binding this everywhere.

**Binding console functions to variables**

**Usage:**

````js
log('one','2',3,[4],{5:5});
````

**Output:**

```js
one 2 3 [4] Object{5:5}
```

**Why would you do that?**
One use case can be when you have custom logger and you want to decide on runtime which one to use.

```js
var logged = require('appLoger');
var log = logToServer ? logger.log : console.log.bind(console);
```

## Functions with an Unknown Number of Arguments (variadic functions)
To create a function which accepts an undetermined number of arguments, there are two methods depending on
your environment.

Whenever a function is called, it has an Array-like arguments object in its scope, containing all the arguments
passed to the function. Indexing into or iterating over this will give access to the arguments, for example

```js
function logSomeThings(){
	for(var i = 0;i < arguments.length; ++i){
		console.log(arguments[i]);
	}
}
logSomeThings('hello','world');
```

From ES6, the function can be declared with its last parameter using the rest operator ( ... ). This creates an Array
which holds the arguments from that point onwards

```js
function personLogsSomeThings(person, ...msg){
	msg.forEach(arg => {
		console.log(person,'says',arg);
	});
}
personLogsSomeThinks('John','hello','world');
// logs "John says hello"
// logs "John says world"
```

This syntax can be used to insert arbitrary number of arguments to any position, and can be used with any
iterable( apply accepts only array-like objects).

```js
const logArguments = (...args) => console.log(args)
function* generateNumbers(){
	yield 6
	yield 5
	yield 4
}
```

## Anonymous Function

**Deﬁning an Anonymous Function**

When a function is deﬁned, you often give it a name and then invoke it using that name, like so:

```js
foo();
function foo(){
	//...
}
```

**Assigning an Anonymous Function to a Variable**
A very common use of anonymous functions is to assign them to a variable:

```js
var foo = function(){/*...*/};
foo();
```

**Returning an Anonymous Function From Another Function**
Sometimes it's useful to return a function as the result of another function. For example:

```js
var hash = getHashFunction('sha1');
var hashValue = hash('Secret Value');
function getHashFunction(algorithm){
	if(algorithm === 'sha1') return function(value){/*...*/};
	else if(algortihm === 'md5') return function(value){/*...*/};
}
```

**Immediately Invoking an Anonymous Function**
Unlike many other languages, scoping in JavaScript is function-level, not block-level. (See Function Scoping ). In
some cases, however, it's necessary to create a new scope. For example, it's common to create a new scope when
adding code via a <script> tag, rather than allowing variable names to be deﬁned in the global scope (which runs
the risk of other scripts colliding with your variable names). A common method to handle this situation is to deﬁne
a new anonymous function and then immediately invoke it, safely hiding you variables within the scope of the
anonymous function and without making your code accessible to third-parties via a leaked function name. For
example:

```js
<!-- My Script -->
<script>
function initalize(){
	// foo is safely hidden within initialize, but...
	var foo = '';
}
// ...my initialize function is now accesible from global scope.
// There is a risk someone could call it again, probably by accident.
initialize();
</script>
<script>
// Using an anonymous function, and then immediately
// invoking it, hides my foo variable and guarantees
// no one else can call it a second time.
(function(){
	var foo = '';
}())// <== the parentheses invokes the function immediately
</script>
```

**Self-Referential Anonymous Functions**
Sometimes it's useful for an anonymous function to be able to refer to itself. For example, the function may need to
recursively call itself or add properties to itself. If the function is anonymous, though, this can be very diﬃcult as it
requires knowledge of the variable that the function has been assigned to. This is the less than ideal solution:

```js
var foo = function(callAgain){
	console.log('Whassup?');
	if(callAgain === true) foo(false);
};
foo(true);
// Console Output:
// Whassup?
// Whassup?
// Assingn bar to the original function, and assign foo to another function.
var bar = foo;
foo = function(){
	console.log('Bad.')
};
bar(true);
```

The intent here was for the anonymous function to recursively call itself, but when the value of foo changes, you
end up with a potentially diﬃcult to trace bug.
Instead, we can give the anonymous function a reference to itself by giving it a private name, like so:

```js
var foo = function myself(callAgain){
	console.log('Whassup?');
	if(callAgain === true) myself(false);
};
foo(true);
// Console Output:
// Whassup?
// Whassup?
var bar = foo;
foo = function(){
	console.log('Bad.')
};
bar(true);
// Console Output:
// Whassup?
// Whassup?
```

## Default parameters
Before ECMAScript 2015 (ES6), a parameter's default value could be assigned in the following way:

```js
function printMsg(msg){
	msg = typeof msg !== 'undefined' ? // if a value was provided
		msg: 'Default value for msg.';
	console.log(msg);
}
```

ES6 provided a new syntax where the condition and reassignment depicted above is no longer necessary:

```js
function printMsg(msg = 'Default value for msg.'){
	console.log(msg);
}
printMsg(); // "Default value for msg."
printMsg(undefined); //"Default value for msg."
printMsg('Now my msg in different!'); // "Now my msg in different!"
```

## Call and apply
Functions have two built-in methods that allow the programmer to supply arguments and the this variable
diﬀerently: call and apply .
This is useful, because functions that operate on one object (the object that they are a property of) can be
repurposed to operate on another, compatible object. Additionally, arguments can be given in one shot as arrays,
similar to the spread ( ... ) operator in ES6.

```js
let obj = {
	a: 1,
	b: 2,
	set: function(a,b){
		this.a = a;
		this.b = b;;
	}
};
obj.set(3,7); // normal syntax
obj.set.call(obj,3,7); // equivalent to the above
obj.set.apply(obj,[3,7]); // equivalent to the above; note that an array is used

console.log(obj); // prints{a: 3,b: 5}
let myObj = {};
myObj.set(5,4); // fails; myObj has no `set` property

obj.set.call(myObj, 5,4); // success; `this` in set() is re-routed to myObj instead of obj
obj.set.apply(myObj,[5,4]); // same as above; note the array

console.log(myObj); // pritns{a: 3, b: 5}
```

ECMAScript 5 introduced another method called bind() in addition to call() and apply() to explicitly set this
value of the function to speciﬁc object.
It behaves quite diﬀerently than the other two. The ﬁrst argument to bind() is the this value for the new function.
All other arguments represent named parameters that should be permanently set in the new function.

```js
function showName(label){
	console.log(label + ":" + this.name);
}
var student1 = {
	name: "Ravi"
};
var student2 = {
	name: "Vinod"
};
var showNameStudent1 = showName.bind(student1);
showNameStudent1("student1");
var showNameStudent2 = showName.bind(student2, "student2");
showNameStudent2();

student2.sayName = showNameStudent1;
student2.sayName("student2");
```

## Partial Application

Similar to currying, partial application is used to reduce the number of arguments passed to a function. Unlike
currying, the number need not go down by one.
Example:
This function ...

```js
function reversedMultiplyThenAdd(c,b,a){
	return a * b + c;
}
function factory(b,c){
	return reversedMultiplyThenAdd.bind(null,c,b);
}
var mutiplyTwoThenAddTen = factory(2,10);
multiplyTwoThenAddTen(10); // 30
```

## Passing arguments by reference or value
In JavaScript all arguments are passed by value. When a function assigns a new value to an argument variable, that
change will not be visible to the caller:

```js
var obj = {a: 2};
function myfunc(arg){
	arg = {a: 5};
}
myfunc(obj);
console.log(obj.a); // 2
```

However, changes made to (nested) properties of such arguments, will be visible to the caller:

```js
var obj = {a: 2};
function myfunc(arg){
	arg.a = 5; // assigment to a property of the argument
}
myfunc(obj);
console.log(obj.a); // 5
```

This can be seen as a call by reference: although a function cannot change the caller's object by assigning a new
value to it, it could mutate the caller's object.
As primitive valued arguments, like numbers or strings, are immutable, there is no way for a function to mutate
them:

```js
var s = 'say';
function myfunc(arg){
	arg += ' hello';
}
myfunc(s);
console.log(s); // say
```

## Function Arguments, "arguments" object, rest
and spread parameters
Functions can take inputs in form of variables that can be used and assigned inside their own scope. The following
function takes two numeric values and returns their sum:

```js
fucntion addition (argument1, argument2){
	return argument1 + argument2;
}
console.log(addition(2,3)); // 5
```

# Functional JavaScript

## Higher-Order Functions
In general, functions that operate on other functions, either by taking them as arguments or by returning them (or
both), are called higher-order functions.
A higher-order function is a function that can take another function as an argument. You are using higher-order
functions when passing callbacks.

```js
function iAmCallbackFunction(){
	console.log("callback has been invoked");
}
function iAmJustFunction(callbackFn){
	// do some stuff ...
	// invoke the callback function.
	callbackFn();
}
```

## Identity Monad
This is an example of an implementation of the identity monad in JavaScript, and could serve as a starting point to
create other monads.
Based on the conference by Douglas Crockford on monads and gonads
Using this approach reusing your functions will be easier because of the ﬂexibility this monad provides, and
composition nightmares:

```js
identityMonad(value)
	.bind(k)
	.bind(j,j1,j2)
	.bind(i,i2)
	.bind(h,h1,h2)
	.bind(g,g1,g2)
	.bind(f,f1,f2)
function identityMonad(value){
	var monad = Object.create(null);
	
	monad.bind = function(func,...args){
		return func(value,...args);
	};
	monad.call = function(func, ...args){
		func(value, ...args);
		return identityMonad(value);
	};
	monad.apply = function(func, ...args){
		return identityMonad(func(value,...args));
	};
	monad.value = function(){
		return value; 
	};
	return monad;
};
```

## Pure Functions
A basic principle of functional programming is that it avoids changing the application state (statelessness) and
variables outside its scope (immutability).
Pure functions are functions that:
				with a given input, always return the same output
				they do not rely on any variable outside their scope
				they do not modify the state of the application (no side eﬀects)
Let's take a look at some examples:

**Impure function**

```js
let obj = {a: 0}
const impure = (input) => {
	input.a = input.a + 1;
	return input.a;
}
let b = impure(obj)
console.log(obj)	//Logs{"a": 1}
console.log(b)		//Logs 1
```

**Pure function**

```js
let obj = {a: 0}
const pure = (input) => {
	let output = input.a + 1;
	return output;
}
let b = pure(obj)
console.log(obj) // Logs{"a":0}
console.log(b) //Logs 1
```

**Impure function**

```js
let a = 1;
let impure = (input) => {
	let output = input * a;
	return output;
}
console.log(impure(2)) // Logs 2
a++;	// a becomes equal to 2
console.log(impure(2)) // Logs 4
```

**Pure function**

```js
let pure = (input) => {
	let a = 1;
	let output = input * a;
	return output;
}
console.log(pure(2)) // Logs 2
```

## Accepting Functions as Arguments

```js
function trasforms(fn,arr){
	let result = [];
	for(let el of arr){
		result.push(fn(el));
	}
	return result;
}
console.log(transform(x => x * 2,[1,2,3,4])); // [2,4,6,8]
```

As you can see, our transform function accepts two parameters, a function and a collection. It will then iterate the
collection, and push values onto the result, calling fn on each of them.
Looks familiar? This is very similar to how Array.prototype.map() works!

```js
console.log([1,2,3,4].map(x => x * 2)); //[2,4,6,8]
```

# Prototypes, objects
In the conventional JS there are no class instead we have prototypes. Like the class, prototype inherits the
properties including the methods and the variables declared in the class. We can create the new instance of the
object whenever it is necessary by, Object.create(PrototypeName); (we can give the value for the constructor as
well)

## Creation and initialising Prototype

```js
var Human = function(){
	this.canWalk = true;
	this.canSpeak = true;
};
Person.prototype.greet = function(){
	if(this.canSpeak){
		this.name = "Steve"
		console.log('Hi, I am ' + this.name);
	}else{
		console.log('Sorry i can not speak');
	}
};
```

The prototype can be instantiated like this

```js
obj = Object.create(Person.prototype);
ob.greet();
```

We can pass value for the constructor and make the boolean true and false based on the requirement.
Detailed Explanation

```js
var Human = function(){
	this.canSpeak = true;
};
Human.prototype.greet = function(){
	if(this.canSpeak){
		console.log('Hi, I am ' + this.name);
	}
};
var Student = function(name,title){
	Human.call(this);
	this.name = name;
	this.title = title;
};
Student.prototype = Object.create(Human.prototype);
Student.prototype.constructor = Student;

Student.prototype.greet = function(){
	if(this.canSpeak){
		console.log('Hi, I am ' + this.name + ', the' + this.title);
	}
};
var Customer = function(name){
	Human.call(this);
	this.name = name;
};
Customer.prototype = Object.create(Human.prototype);
Customer.prototype.constructor = Customer;

var bill = new Student('Billy', 'Teacher');
var carter = new Customer('Carter');
var andy = new Student('Andy','Bill');
var virat = new Customer('Virat');

bill.greet();
// Hi, I am Bob, the Teacher
carter.greet()
// Hi, I am Carter
andy.greet();
// Hi, I am Andy, the Bill
virat.greet();
```

# Classes

## Class Constructor
The fundamental part of most classes is its constructor, which sets up each instance's initial state and handles any
parameters that were passed when calling new .
It's deﬁned in a class block as though you're deﬁning a method named constructor , though it's actually handled
as a special case.

```js
class MyClass{
	constructor(option){
		console.log(`Creating instance using ${option} option.`);
	}
}
const foo = new MyClass('speedy'); // logs: "Creating instance using speedy option"
```

## Class Inheritance
Inheritance works just like it does in other object-oriented languages: methods deﬁned on the superclass are
accessible in the extending subclass.
If the subclass declares its own constructor then it must invoke the parents constructor via super() before it can
access this .

```js
class SuperClass{
	constructor(){
		this.logger = console.log;
	}
	log(){
		this.logger(`Hello ${this.name}`);
	}
}
class SubClass extends SuperClass{
	constructor(){
		super();
		this.name = 'subclass';
	}
}
const subClass = new SubClass();
subClass.log(); // logs: "Hello suclass"
```

## Static Methods
Static methods and properties are deﬁned on the class/constructor itself, not on instance objects. These are speciﬁed
in a class deﬁnition by using the static keyword.

```js
class MyClass{
	static myStaticMethod(){
		return 'Hello';
	}
	static get myStaticProperty(){
		return 'Goodbye';
	}
}
console.log(MyClass.myStaticMethod()); // logs: "Hello"
console.log(MyClass.myStaticProperty); // logs: "Goodbye"
```

## Getters and Setters
Getters and setters allow you to deﬁne custom behaviour for reading and writing a given property on your class. To
the user, they appear the same as any typical property. However, internally a custom function you provide is used
to determine the value when the property is accessed (the getter), and to perform any necessary changes when the
property is assigned (the setter).
In a class deﬁnition, a getter is written like a no-argument method preﬁxed by the get keyword. A setter is similar,
except that it accepts one argument (the new value being assigned) and the set keyword is used instead.
Here's an example class which provides a getter and setter for its .name property. Each time it's assigned, we'll
record the new name in an internal .names_ array. Each time it's accessed, we'll return the latest name.

```js
class MyClass{
	constructor(){
		this.names_ = [];
	}
	set name(value){
		this.names_.push(value);
	}
	get name(){
		return this.names_[this.names_.length - 1];
	}
}
const myClassInstance = new MyClass();
myClassInstance.name = 'Joe';
myClassInstance.name = 'Bob'

console.log(myClassInstence.name); // logs: "Bob"
console.log(myClassInstance.names_); // logs: ["Joe","Bob"]
```

## Private Members
JavaScript does not technically support private members as a language feature. Privacy - described by Douglas
Crockford - gets emulated instead via closures (preserved function scope) that will be generated each with every
instantiation call of a constructor function.
The Queue example demonstrates how, with constructor functions, local state can be preserved and made
accessible too via privileged methods.

```js
class Queue{
	constructor(){			// does generate a closure with each instantiation
		const list = [];	// local state ("private member").
		this.enqueue = function (type){		//privileged public method
			list.push(type);				//accesing the local state
            return type;					// "writing" alike
		};
		this.dequeue = function(){			// privileged public method 
			return list.shift();			// acessing the local state
		};									// "reading / writing" alike
	}
}
var q = new Queue;

q.enqueue(9);
q.enqueue(8);
q.enqueue(7);

console.log(q.dequeue());					// 9 ... first out.
console.log(q.dequeue());					// 8
console.log(q.dequeue());					// 7
console.log(q);								// {}
console.log(Object.keys(q));				// ["enqueue","dequeue"]
```



With every instantiation of a Queue type the constructor generates a closure.
Thus both of a Queue type's own methods enqueue and dequeue (see Object.keys(q) ) still do have access to list
that continues to live in its enclosing scope that, at construction time, has been preserved.
Making use of this pattern - emulating private members via privileged public methods - one should keep in mind
that, with every instance, additional memory will be consumed for every own property method (for it is code that
can't be shared/reused). The same is true for the amount/size of state that is going to be stored within such a
closure.

## Methods
Methods can be deﬁned in classes to perform a function and optionally return a result.
They can receive arguments from the caller.

```js
class Something{
	constructor(data){
		this.data = data
	}
	doSomething(text){
		return{
			data: this.data,
			text
		}
	}
}
var s = new Something({})
s.doSomething("hi")			// returns: {data: {},text: "hi"}
```

## Dynamic Method Names
There is also the ability to evaluate expressions when naming methods similar to how you can access an objects'
properties with [] . This can be useful for having dynamic property names, however is often used in conjunction
with Symbols.

```js
let METADATA = Symbol('metadata');
class Car{
	constructor(make,model){
		this.make = make;
		this.model = model;
	}
	[METADATA](){
		return {
			make: this.make,
			model: this.model
		};
	}
	["add"](a,b){
		return a + b;
	}
	[1 + 2](){
		return "three";
	}
}
let MazdaMPV = new Car("Mazda","MPV");
MazdaMPV.add(4,5);//9
MazdaMPV[3](); // "three"
MazdaMPV[METADATA](); // {make: "Mazda", model: "MPV"}
```

## Managing Private Data with Classes
One of the most common obstacles using classes is ﬁnding the proper approach to handle private states. There are
4 common solutions for handling private states:

When using symbol as a property key, it is not enumerable.
As such, they won't be revealed using for var in or Object.keys .
Thus we can use symbols to store private data.

```js
const topSecret = Symbol('topSecret');		//our private key;
export class SecretAgent{
	consturctor(secret){
		this[topSecret] = secret; // we have acces to the symbol key (closure)
		this.coverStory = 'just a simple gardner';
		this.doMission = () => {
			figureWhatToDo(topSecret[topSecret]); // we have access to topSecret
		};
	}
}
```

**Using WeakMaps**
WeakMap is a new type of object that have been added for es6.

The idea is to use the WeakMap, as a static map for the whole class, to hold each instance as key and keep the
private data as a value for that instance key.
Thus only inside the class will we have access to the WeakMap collection.
Let's give our agent a try, with WeakMap :

````js
const topSecret = new WeakMap(); // will hold all private data of instances
export class SecretAgent{
	constructor(secret){
		topSecret.set(this.secret); // we use this, as the key, to set it inour insatance privat data
		this.coverStory = 'just a simple gardner';
		this.doMission = () =>{
			figureWhatToDo(topSecret.get(this)); // we have access to topSecret
		};
	}
}
````

**Deﬁne all methods inside the constructor**
The idea here is simply to deﬁne all our methods and members inside the constructor and use the closure to access
private members without assigning them to this .

```js
export class SecretAgent{
	constructor(secret){
		const topSecret = secret;
		this.coverStory = 'just a simple gardner';
		this.doMission = () => {
			figureWhatToDo(topSecret); // we have access to topSecret
		};
	}
}
```

**Using naming conventions**
We will decide that any property who is private will be preﬁxed with _ .
Note that for this approach the data isn't really private.

```js
export class SecretAgent{
	constructor(secret){
		this._topSecret = secret; // it private by convention
		this.coverStory = 'just a simple gardner';
		this.doMission = () => {
			figureWhatToDo(this_topSecret);
		};
	}
}
```

## Class Name binding
ClassDeclaration's Name is bound in diﬀerent ways in diﬀerent scopes -

The scope in which the class is deﬁned - let binding

The scope of the class itself - within { and } in class {} - const binding

```js
class Foo{
	// Foo inside this block is a const binding
}
// Foo here is a let binding
```

For example,

```js
class A{
	foo(){
		A = null; // will throw at runtime as A inside the class is a `const` binding
	}
}
A = null; // will NOT throw as A here is a `let` binding
```

This is not the same for a Function

```js
function A(){
	A = null; // works
}
A.prototype.foo = function foo(){
	A = null; // works
}
A = null; // works
```

# Context (this)

## this with simple objects

```js
var person = {
	name: 'John Doe',
	age: 42,
	gender: 'male',
	bio: function(){
		console.log('My name is ' + this.name);
	}
};
person.bio(); // logs "My name is Jhon Doe"
var bio = person.bio;
bio(); // logs "My name is undefined"
```

In the above code, person.bio makes use of the context ( this ). When the function is called as person.bio() , the
context gets passed automatically, and so it correctly logs "My name is John Doe". When assigning the function to a
variable though, it loses its context.
In non-strict mode, the default context is the global object ( window ). In strict mode it is undefined .

## Binding function context

Every function has a bind method, which will create a wrapped function that will call it with the correct context. See
here for more information

```js
var monitor = {
	treshold: 5,
	check: function(value){
		if(value > this.treshold){
			this.display("Value is too high!");
		}
	},
	display(message){
		alert(message);
	}
},
monitor.check(7);

var badCheck = monitor.check;
badChek(15);
var check = monitor.check.bind(monitor);
check(15);
var check8 = monitor.check.bind(monitor,8);
check8();
```

**Hard binding**
The object of hard binding is to "hard" link a reference to this .
Advantage: It's useful when you want to protect particular objects from being lost.
Example:

```js
function Person(){
	console.log("I'm " + this.name);
}
var person0 = {name: "Stackoverflow"}
var person1 = {name: "Jhone"}
var person2 = {name: "Doe"}
var person3 = {name: "Ala Eddine JEBALI"};

var origin = Person;
Person = function(){
	origin.call(person0);
}

Person();
// outputs: I'm Stackoverflow

Person.call(person1);
// outputs: I'm Stackoverflow

Person.apply(person2);
// outputs: I'm Stackoverflow

Person.call(person3);
// outputs: I'm Stackoverflow
```

## this in constructor functions
When using a function as a constructor, it has a special this binding, which refers to the newly created object:

```js
function Cat(name){
	this.name = name;
	this.sound = "Weow";
}
var cat = new Cat("Tom"); // is a Cat Object
cat.sound; // Returns "Meow"

var cat2 = Cat("Tom"); // is a Cat object
cat.sound; // Returns "Meow"

var cat2 = Cat("Tom"); // is undefined
window.name; // "Tom"
cat2.name; // error! cannot access property of undefined
```

# Setters and Getters

Setters and getters are object properties that call a function when they are set/gotten.

## Deﬁning getters and setters in ES6 class

```js
class Person{
	constructor(firstname, lastname){
		this._firstname = firstname;
        this._lastname = lastname;
	}
    get firstname(){
        return this._firstname;
    }
    set firstname(name){
        this._firstname = name;
    }
    get lastname(){
        return this._lastname;
	}
    set lastname(name){
        this._lastname = name;
	}
}
let person = new Person('Jhon', 'Doe');
console.log(person.firstname,person.lastname); // John Doe
person.firsname = 'Foo';
person.lastname = 'Bar';

console.log(person.firstname, person.lastname); // Foo Bar
```

# Method Chaining

## Chainable object design and chaining
Chaining and Chainable is a design methodology used to design object behaviors so that calls to object functions
return references to self, or another object, providing access to additional function calls allowing the calling
statement to chain together many calls without the need to reference the variable holding the object/s.
Objects that can be chained are said to be chainable. If you call an object chainable, you should ensure that all
returned objects / primitives are of the correct type. It only takes one time for your chainable object to not return
the correct reference (easy to forget to add return this ) and the person using your API will lose trust and avoid
chaining. Chainable objects should be all or nothing (not a chainable object even if parts are). An object should not
be called chainable if only some of its functions are.

**Object designed to be chainable**

```js
function Vec(x = 0, y = 0){
	this.x = x;
	this.y = y;
}
Vec.prototype = {
	add : function(vec){
		this.x += vec.x;
		this.y += vec.y;
		return this; //return reference to self to allow chaining of function calls
	}, 
	scale : function(val){
		this.x *= val;
		this.y *= val;
		return this; // return reference to self to allow chaining of function calls
	},
	log :function(val){
		onsole.log(this.x + ' : ' + this.y);
		return this;
	},
	clone : function(){
		return new Vec(this.x, this.y);
	}
}
var vec = new Vec();
vec.add({x: 10,y : 10})
	.add({x:10,y:10})
	.log()						// console output "20 : 20"
	.add({x:10,y:10})
	.scale(1/30)
	.log()						// console output "1 : 1"
	.clone()					// returns a new instance of the object 
	.scale(2)					// from which you can continue chaining
	.log()
```

## Method Chaining
Method chaining is a programming strategy that simpliﬁes your code and beautiﬁes it. Method chaining is done by
ensuring that each method on an object returns the entire object, instead of returning a single element of that
object. For example:

```js
function Door(){
	this.height = '';
	this.width = '';
	this.status = 'closed';
}
Door.prototype.open = function(){
	this.status = 'opened';
	return this;
}
Door.prototype.close = function(){
	this.status = 'closed';
	return this;
}
Door.prototype.setParams = function(width,height){
	this.width = width;
	this.height = height;
	return this;
}
Door.prototype.doorStatus = function(){
	console.log('The',this.width,'x',this.height,'Door is',this.status);
	return this;
}
var smallDoor = new Door();
smallDoor.setParams(20,100).open().doorStatus().close().doorStatus();
OUTPUT:
// The 20 x 100 Door is opened
// The 20 x 100 Door is closed
// Door {height: 100, width: 20, status: "closed"}
```

# Callbacks

## Error handling and control-ﬂow branching
Callbacks are often used to provide error handling. This is a form of control ﬂow branching, where some
instructions are executed only when an error occurs:

```js
const expected = true;
function compare(actual,success, failure){
	if(actual === expected){
		success();
	}else{
		failure();
	}
}
function onSuccess(){
	console.log('Value was expected');
}
function onFailure(){
	console.log('Value was unexpected/exeptional');
}
compare(true, onSuccess, onFailure);
compare(false, onSucess, onFailure);
// Outputs:
// "Value was expected"
// "Value was unexpected/exceptional"
```

Code execution in compare() above has two possible branches: success when the expected and actual values are
the same, and error when they are diﬀerent. This is especially useful when control ﬂow should branch after some
asynchronous instruction:

```js
function compareAsync(actual,success,failure){
	setTimeout(function(){
		compare(actual,success,failure)
	}, 1000);
}
compareAsync(true, onSuccess, onFailure);
compareAsync(false, onSuccess,onFailure);
console.log('Doing something else');
// Outputs:
// "Doing something else"
// "Value was expected"
// "Value was unexpected/exceptional"
```

# Intervals and Timeouts

## Recursive setTimeout
To repeat a function indeﬁnitely, setTimeout can be called recursively:

```js
functionrepeatingFunc(){
	console.log("It's been 5 seconds. Execute the function again.");
	setTimeout(repeatingFunc, 5000);
}
setTimeout(repeatingFunc, 5000);
```

## Intervals

````js
function waitFunc(){
	console.log("This will be logged every 5 seconds");
}
window.setInterval(waitFunc,5000);
````

## Removing intervals
window.setInterval() returns an IntervalID , which can be used to stop that interval from continuing to run. To
do this, store the return value of window.setInterval() in a variable and call clearInterval() with that variable as
the only argument:

```js
function waitFunc(){
	console.log("This will be logged every 5 seconds");
}
var interval = window.setInterval(waitFunc,5000);
window.setTimeout(function(){
	clearInterval(interval);
},32000);
```

## Removing timeouts
window.setTimout() returns a TimeoutID , which can be used to stop that timeout from running. To do this, store
the return value of window.setTimeout() in a variable and call clearTimeout() with that variable as the only
argument:

```js
function waitFunc(){
	console.log("This will not be logged after 5 seconds");
}
function stopFunc(){
	clearTimeout(timeout);
}
var timeout = window.setTimeout(waitFunc,5000);
window.setTimeout(stopFunc,3000);
```

# Cookies

## Test if cookies are enabled

If you want to make sure cookies are enabled before using them, you can use navigator.cookieEnabled :

```js
if(navigator.cookieEnabled === false){
	alert("Error: cookie not enabled!");
}
```

## Adding and Setting Cookies
The following variables set up the below example:

```JS
var COOKIE_NAME = "Example Cookie";
var COOKIE_VALUE = "Hello, world!";
var COOKIE_PATH = "/foo/bar";
var COOKIE_EXPIRES;
COOKIE_EXPIRES = (new Date(Date.now() + 60000)).toUTCString();
doucument.cookie += COOKIE_NAME + "=" + COOKIE_VALUE + "; expires" + COOKIE_EXPIRES + "; path=" + COOKIE_PATH;
```

# Web Storage

## Simpler way of handling Storage
localStorage , sessionStorage are JavaScript Objects and you can treat them as such.
Instead of using Storage Methods like .getItem() , .setItem() , etc… here's a simpler alternative:

```js
localStorage.hello = "Hello";
localStorage.year = 2017;

var user = {name:"John",surname:"Doe",books:["A","B"]};
localStorage.user = JSON.stringify(user);
console.log(typeof localStorage.year);

var someYear = localStorage.year;

var userData = JSON.parse(localStorage.user);
var userName = userData.name;

delete localStorage.year;
localStorage.clear();
// OUTPUT:
// String
```

## Remove Storage Item
To remove a speciﬁc item from the browser Storage (the opposite of setItem ) use removeItem

```js
localStorage.setItem("greet","hi");
localStorage.removeItem("greet");
console.log(localStorage.getItem("greet")); // null
```

# Data attributes

## Accessing data attributes
**Using the dataset property**
The new dataset property allows access (for both reading and writing) to all data attributes data-* on any element.

![image-20210707152826890](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210707152826890.png)

# JSON

## Parsing with a reviver function
A reviver function can be used to ﬁlter or transform the value being parsed.

```js
var jsonString = '[{"name":"Jhon","score":51},{"name":"Jack","score":17}]';

var data = JSON.parse(jsonString,function reviver(key,value){
	return key === 'name' ? value.toUpperCase() : value;
});
const jsonString = '[{"name":"John","score":51},{"name":{"Jack","score":17}}]';
const data = JSON.parse(jsonString,(key,value) =>
	key === 'name' ? value.toUpperCase() : value;
);
```

## Serializing and restoring class instances
You can use a custom toJSON method and reviver function to transmit instances of your own class in JSON. If an
object has a toJSON method, its result will be serialized instead of the object itself.

```js
function Car(color,speed){
	this.color = color;
	this.speed = speed;
}
Car.prototype.toJSON = function(){
	return{
		$type: 'com.example.Car',
		color: this.color,
		speed: this.speed
	};
};
Car.fromJSON = function(data){
	return new Car(data.color,data.speed);
};
class Car{
	constructor(color,speed){
		this.color = color;
		this.speed = speed;
		this.id_ = Math.random();
	}
	toJSON(){
		return{
			$type: 'com.example.Car',
			color: this.color,
			speed: this.speed
		};
	}
	static fromJSON(data){
		return new Car(data.color, data.speed);
	}
}
var userJson = JSON.stringify({
	name: "John",
	car: new Car('red','fast')
});
```

This produces the a string with the following content:

```js
{"name":"John","car":{"$type":"com.example.Car","color":"red","speed":"fast"}}
var userObject = JSON.parse(userJson, function reviver(key,value){
	return (value && value.$type === 'com.example.Car') ? Car.fromJSON(value) : value;
});
```

This produces the following object:

```js
{
	name: "John",
	car: Car{
		color: "red",
		speed: "fast",
		id_: 0.19349242527065402
	}
}
```

## Cyclic object values
Not all objects can be converted to a JSON string. When an object has cyclic self-references, the conversion will fail.
This is typically the case for hierarchical data structures where parent and child both reference each other:

```js
const world = {
	name: 'World',
	regions: []
};
world.regions.push({
	name: 'North America',
	parent: 'America'
});
console.log(JSON.stringify(world));
world.regions.push({
	name: 'Asia',
	parent: world
});
console.log(JSON.stringify(world));
```

# Enumerations

## Printing an enum variable

After deﬁning an enum using any of the above ways and setting a variable, you can print both the variable's value
as well as the corresponding name from the enum for the value. Here's an example:

```js
var ColorsEnum = {WHITE: 0, GRAY: 1, BLACK: 2}
Object.freeze(ColorsEnum);
var color = ColorEnum.BLACK;
if(color == ColorsEnum.BLACK){
	console.log(color);		// This will print "2"
	var ce = ColorEnum;
	for(var name in ce){
		if(ce[name] == ce.BLACK)
			console.log(name);		// This will print "BLACK"
	}
}
```

## Automatic Enumeration Value

This Example demonstrates how to automatically assign a value to each entry in an enum list. This will prevent two
enums from having the same value by mistake. NOTE: Object.freeze browser support

```js
var testEnum = fumction(){
	var enumList = [
		"One",
		"Two",
		"Three"
	];
	enumObj = {};
	enumList.forEach((item,index) => enumObj[item] = index + 1);
	Object.freeze(enumObj);
	return enumObj;
}();
console.log(testEnum.One); // 1 will be logged
var x = testEnum.Two;
switch(x){
	case testEnum.One:
		console.log("111");
		break;
	case testEnum.Two:
		console.log("222"); // 222 will be logged
		break;
}
```

# Generators
Generator functions (deﬁned by the function* keyword) run as coroutines, generating a series of values as they're
requested through an iterator.

## Generator Functions
A generator function is created with a function* declaration. When it is called, its body is not immediately executed.
Instead, it returns a generator object, which can be used to "step through" the function's execution.
A yield expression inside the function body deﬁnes a point at which execution can suspend and resume.

```js
function* nums(){
	console.log('starting'); //A
	yield 1;				//B
	console.log('yielded 1'); //C
	yield 2;					// D
	console.log('yielded 2'); // E
	yield 3;
	console.log('yielded 3');	// G
}
var generator = nums();
generator.next();
generator.next();
generator.next();
generator.next();

```

## Sending Values to Generator
It is possible to send a value to the generator by passing it to the next() method.

```js
function* summer(){
	let sum = 0, value;
	while(true){
		value = yield;
		if(value === null) break;
		sum += value;
	}
	return sum;
}
let generator = summer();

generator.next(1);
generator.next(10);
generator.next(100);

let sum = generator.next(null).value();
```

# Promises

## Waiting for the ﬁrst of multiple concurrent promises

The Promise.race() static method accepts an iterable of Promises and returns a new Promise which resolves or
rejects as soon as the ﬁrst of the promises in the iterable has resolved or rejected.

```js
function resolve(value,millisecond){
	return new Promise(resolve => setTimeout(() => resolve(value),milliseconds));
}
function reject(reason, milliseconds){
	return new Promise((_,reject) => setTimeout(() => reject(reason),millisecond));
}
Promise.race([
	resolve(1,5000),
	resolve(2,3000),
	resolve(3,1000)
])
.then(vale => console.log(value));
Promise.race([
	reject(new Error('bad thinks!'),1000),
	resolve(2,2000)
])
.then(value => console.log(value)) // does not output anything
.catch(error => console.log(error.message)); // outputs "bad thinks!" after 1 second
```

**Return a rejected promise with the error**

```js
function foo(arg){
	if(arg === 'unexepectedValue'){
		return Promise.reject(new Error('UnexpectedValue'))
	}
	return new Promise(resolve => 
	setTimeout(()=> resolve(arg),1000)
}
```

**Wrap your function into a promise chain**
Your throw statement will be properly caught when it is already inside a promise chain:

```js
function foo(arg){
	return Promise.resolve()
		.then(() => {
			if(arg === 'unexpectedValue'){
				throw new Error('UnexpectedValue')
			}
			return new Promise(resolve => 
				setTimeout(() => resolve(arg), 1000)
			)
		})
}
```

# Modals - Prompts

 ## Persistent Prompt Modal
When using prompt a user can always click Cancel and no value will be returned.
To prevent empty values and make it more persistent:

![image-20210707171346871](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210707171346871.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JS</title>
        <style>

        </style>
    </head>
    <body>
        <h2>Welcome <span id="name"></span></h2>
        <script>
            var userName;
            while(!userName){
                userName = prompt("Enter your name","");
                if(!userName){
                    alert("Please, we need your name!");
                }else{
                    document.getElementById("name").innerHTML = userName;
                }
            }
        </script>
    </body> 
</html>
```

## Conﬁrm to Delete element
A way to use confirm() is when some UI action does some destructive changes to the page and is better
accompanied by a notiﬁcation and a user conﬁrmation - like i.e. before deleting a post message:

![image-20210707172339535](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210707172339535.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JS</title>
        <style>
        </style>
    </head>
    <body>
        <div id = "post-102">
            <p>I like Confirm modals.</p>
            <a data-deletepost="post-102">Delete post</a>
        </div>
        <div id="post-103">
            <p>That's way too cool1</p>
            <a data-deletepost="post-103">Delete post</a>
        </div>
        <script>
            var deleteBtn = document.querySelectorAll("[data-deletepost");
            function deleteParentPost(event){
                event.preventDefault();
                if(confirm("Really Delete this post?")){
                    var post = document.getElementById(this.dataset.deletepost);
                }
            }
            [].forEach.call(deleteBtn,function(btn){
                btn.addEventListener("click",deleteParentPost,false);
            });
        </script>
    </body> 
</html>
```

## Usage of alert()

![image-20210707172520813](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210707172520813.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JS</title>
        <style>
        </style>
    </head>
    <body>

        <script>
            alert("Hello world!");
            window.alert("Hello world!");
        </script>
    </body> 
</html>
```

# execCommand and contenteditable
**Quick Start Example:**

![image-20210708091540167](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708091540167.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JS</title>
        <style>
        </style>
    </head>
    <body>
        <button data-edit="bold"><b>B</b></button>
        <button data-edit="italic"><i>I</i></button>
        <button data-edit="formatBlock:p">P</button>
        <button data-edit="formatBlock:H1">H1</button>
        <button data-edit="insertUnorderedList">UL</button>
        <button data-edit="justifyLeft">&#8676;</button>
        <button data-edit="justifyRight">&#8677;</button>
        <button data-edit="removeFormat">&times;</button>
        <div contenteditable><p>Edit me!</p></div>
        <script>
            [].forEach.call(document.querySelectorAll("[data-edit]"),function(btn){
                btn.addEventListener("click",edit,false);
            });
            function edit(event){
                event.preventDefault();
                var cmd_val = this.dataset.edit.split(":");
                document.execCommand(cmd_val[0],false,cmd_val[1]);
            }
        </script>
    </body> 
</html>
```

## Copy to clipboard from textarea using execCommand("copy")

![image-20210708092126650](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708092126650.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JS</title>
        <style>
        </style>
    </head>
    <body>
        <textarea id="content"></textarea>
        <input type="button" id="cpoyID" value="Copy">
        <script>
            var button = document.getElementById("copyID"),
                input = document.getElementById("content");
            button.addEventListener("click",function(event){
                event.preventDefault();
                input.select();
                document.execCommand("copy");
            });
        </script>
    </body> 
</html>
```

# Navigator Object

## Get some basic browser data and return it as a JSON object

The following function can be used to get some basic information about the current browser and return it in JSON
format.

```js
function getBrowserInfo(){
	var 
		json = "[{",
		info = [
			navigator.userAgent, // Get the User-agent
			navigator.cookieEnabled, // Checks whether cookies are enbled in browser
			navigator.appName, // Get the Name of Browser
			navigator.language, // Get the Language of Browser
			navigator.appVersion, // Get the Version of Browser
			navigator.platform // Get the platform for which browser is compiled
		],
		/* The array containing the browser info names */
		infoNames = [
			"userAgent",
			"cookiesEnabled",
			"browserName",
			"browserLang",
			"browserVersion",
			"browserPlatform"
		];
	for(var i = 0; i < info.length; i++){
		if(i === info.length - 1){
			json += '"' + infoNames[i] + '": "' + info[i] + '"';
		}else{
			json += '"' + infoNames[i] + '": "' + info[i] + '",'
		}
	};
	return json + "}]";
}
```

# BOM (Browser Object Model)

## Introduction
The BOM (Browser Object Model) contains objects that represent the current browser window and components;
objects that model things like history, device's screen, etc
The topmost object in BOM is the window object, which represents the current browser window or tab.

![image-20210708094528521](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708094528521.png)

# Strict mode

## Changes to properties

Strict mode also prevents you from deleting undeletable properties.

```js
"use strict";
delete Object.prototype; // throw a TypeError
```

The above statement would simply be ignored if you don't use strict mode, however now you know why it does not
execute as expected.
It also prevents you from extending a non-extensible property.

```js
var myObject = {name: "My Name"}
Object.preventExtensions(myObject);
function setAge(){
	myObject.age = 25; // No errors
}
function setAge(){
	"use strict";
	myObject.age = 25; // TypeError: can't define property "age" : Object is not extensible
}
```

## Behaviour of a function's arguments list
arguments object behave diﬀerent in strict and non strict mode. In non-strict mode, the argument object will reﬂect
the changes in the value of the parameters which are present, however in strict mode any changes to the value of
the parameter will not be reﬂected in the argument object.

```js
function add(a,b){
	console.log(arguments[0],arguents[1]); // Prints: 1,2
	a = 5, b = 10;
	console.log(arguments[0],arguments[1]); // Prints: 5,10
}
add(1,2);
```

# Custom Elements

## Extending Native Elements
It's possible to extent native elements, but their descendants don't get to have their own tag names. Instead, the is
attribute is used to specify which subclass an element is supposed to use. For example, here's an extension of the
<img> element which logs a message to the console when it's loaded.

```html
const prototype = Object.create(HTMLImageElement.prototype);
prototype.createdCallback = function(){
	this.addEventListener('load', event => {
		console.log("Image loaded successfully.");
	});
};
document.refisterElement('ex-image',{extends: 'img',prototype: prototype});
<img is="ex-image" src = "http://cdn.sstatic.net/Sites/stackoverflow/img/apple-touch-icon.png">
```

## Registering New Elements
Deﬁnes an <initially-hidden> custom element which hides its contents until a speciﬁed number of seconds have
elapsed.

```js
const InitiallyHiddenElement = document.registerElement('initially-hidden',class extends
HTMLElement{
	createdCallback(){
		this.revealTimeoutId = null;
	}		
	attachedCallback(){
		const seconds = Number(this.getAttribute('for'));
		this.style.display = 'none';
		this.revealTimeoutId = setTimeout(() => {
			this.style.display = 'block';
		}, seconds * 1000);
	}
	detachedCallback(){
		if(this.revealTimeoutId){
			clearTimeout(this.revealTimeoutId);
			this.revealTimeoutId = null;
		}
	}
});
```

```html
<initially-hidden for = "2">Hello</initially-hidden>
<initially-hidden for = "5">World></initially-hidden>
```

# Binary Data

## Getting binary representation of an image ﬁle

This example is inspired by this question.
We'll assume you know how to load a ﬁle using the File API.

```js
var file = // get handle to local file.
var reader = new FileReader();
reader.onload = function(event){
	var data = event.target.result;
	console.log(ArrayBufferToBinary(data));
};
reader.readAsArrayBuffer(file); // gets an ArrayBuffer of the file
```

## Manipulating ArrayBuers with DataViews
DataViews provide methods to read and write individual values from an ArrayBuﬀer, instead of viewing the entire
thing as an array of a single type. Here we set two bytes individually then interpret them together as a 16-bit
unsigned integer, ﬁrst big-endian then little-endian.

```js
var buffer = new ArrayBuffer(2);
var view = new DataView(buffer);

view.setUnit(0, 0xFF);
view.setUnot(0, 0x01);

console.log(view.getUnit16(0, false)); // 65281
console.log(view.getUnit16(0, true)); // 511
```

## Iterating through an arrayBuffer
For a convenient way to iterate through an arrayBuﬀer, you can create a simple iterator that implements the
DataView methods under the hood:

```js
var ArrayBufferCursor = function(){
	var ArrayBufferCursor = function(arrayBuffer){
		this.dataview = new DataView(arrayBuffer,0);
		this.size = arrayBuffer.byteLength;
		this.index = 0;
	}
	ArrayBufferCursor.prototype.next = function(type){
		switch(type){
			case 'Unit8':
				var result = this.dataview.getUnit8(this.index);
				this.index += 1;
				return result;
			case 'Int16':
				var result = this.dataview.getInt16(this.index,true);
				this.index += 2;
				return result;
			case 'Uint16':
                    var result = this.dataview.getUint16(this.index, true);
                    this.index += 2;
                    return result;
                case 'Int32':
                		var result = this.dataview.getInt32(this.index, true);
                    this.index += 4;
                    return result;
                case 'Uint32':
               		var result = this.dataview.getUint32(this.index, true);
                    this.index += 4;
                    return result;
                case 'Float':
                case 'Float32':
                	var result = this.dataview.getFloat32(this.index, true);
                    this.index += 4;
                    return result;
                case 'Double':
                case 'Float64':
                	var result = this.dataview.getFloat64(this.index, true);
                    this.index += 8;
                    return result;
                default:
                throw new Error("Unknown datatype");	
		}
	};
	ArrayBufferCursor.prototype.hasNext = function(){
		return this.index < this.size;
	}
	return ArrayBufferCursor;
}
```

You can then create an iterator like this:

```js
var cusor = new ArrayBufferCursor(arrayBuffer);
```

You can use the hasNext to check if theres's still items

```js
for(;cursor.hasnext();){
		// There's still items to process
}
```

You can use next method to take the next value:

```js
var nextValue = cursor.next('Float');
```

With such an iterator, writing your own parser to process binary data becomes pretty easy.

# Template Literals
Template literals are a type of string literal that allows values to be interpolated, and optionally the interpolation
and construction behaviour to be controlled using a "tag" function.

## Basic interpolation and multiline strings
Template literals are a special type of string literal that can be used instead of the standard '...' or "..." . They
are declared by quoting the string with backticks instead of the standard single or double quotes: `...` .
Template literals can contain line breaks and arbitrary expressions can be embedded using the ${ expression }
substitution syntax. By default, the values of these substitution expressions are concatenated directly into the
string where they appear.

```js
const name = "John";
const score = 74;

console.log(`Game Over!`
${name}'s score was ${score * 10}.');
Game Over!
John's score was 740.
```

## Raw strings
The String.raw tag function can be used with template literals to access a version of their contents without
interpreting any backslash escape sequences.
String.raw`\n` will contain a backslash and the lowercase letter n, while `\n` or '\n' would contain a single
newline character instead.

```js
const patternString = String.raw`Welcome, (\w+)!`;
const pattern = new RegExp(patternString);

const message = "Welcome, John!";
pattern.exec(message);
["Welcome, John!","John"]
```

# Fetch

## POST Data
Posting form data

```js
fetch(`/example/submit`,{
	method: 'POST',
	body: new FormData(document.getelementById('example-form'))
});
```

Posting JSON data

```js
fetch(`/example/submit.json`,{
	method: 'POST',
	body: JSON.steingify({
		email: document.getElementById('example-email').value,
		comment: document.getElementById('example-comment').value
	})
});
```

## Using Fetch to Display Questions from the Stack Overﬂow API

```js
const url = 'http://api.stackexchange.com/2.2/questions?site=stackoverflow&tagged=javascript';

const questionList = document.createElement('ul');
document.body.appendChild(questionList);

const responseData = fetch(url).then(response => response.json());
responseData.then(({items, has_more, quota_max, quota_remaining}) => {
for (const {title, score, owner, link, answer_count} of items) {
    const listItem = document.createElement('li');
    questionList.appendChild(listItem);
    const a = document.createElement('a');
    listItem.appendChild(a);
    a.href = link;
    a.textContent = `[${score}] ${title} (by ${owner.display_name || 'somebody'})`
    }
});
```

# Modules

## Deﬁning a module
In ECMAScript 6, when using the module syntax ( import / export ), each ﬁle becomes its own module with a private
namespace. Top-level functions and variables do not pollute the global namespace. To expose functions, classes,
and variables for other modules to import, you can use the export keyword.

```js
function somethingPrivate(){
	console.log('TOP SECRET')
}

export const PI = 3.14;
export function doSomething(){
	console.log('Hello from a module!')
}

function doSomethingElse(){
	console.log("Something else")
}

export {doSomethingElse}
export class MyClass{
	test(){}
}
```

## Destructuring inside variables
Aside from destructuring objects into function arguments, you can use them inside variable declarations as follows:

```js
const person = {
	name: 'Jhon Doe',
	age: 45,
	location: 'Paris,France',
};
let {name,age, location} = person;
console.log('I am ' + name + ', aged ' + age + ' and living in ' + location + '.');
```

## Default Value While Destructuring
We often encounter a situation where a property we're trying to extract doesn't exist in the object/array, resulting
in a TypeError (while destructuring nested objects) or being set to undefined . While destructuring we can set a
default value, which it will fallback to, in case of it not being found in the object.

```js
var obj = {a:1};
var {a:x,b:x1 = 10} = obj;
console.log(x,x1); // 1,10

var arr = [];
var [a = 5, b = 10, c] = arr;
console.log(a,b,c); // 5,10 undefined
```

## Renaming Variables While Destructuring
Destructuring allows us to refer to one key in an object, but declare it as a variable with a diﬀerent name. The
syntax looks like the key-value syntax for a normal JavaScript object.

````js
let user = {
	name: 'Jhon Smith',
	id: 10,
	email: 'johns@workcorp.com',
};

let{user: userName, id: userId} = user;
console.log(userName) // Jhon Smith
console.log(userId) // 10
````

# WebSockets

## Working with string messages

```js
var wsHost = "ws://my-sites-url.com/path/to/echo-web-socket-handler";
var ws = new WebSocket(wsHost);
var value = "an example message";

ws.onmessage = function(message){
	if(message === value){
		console.log("The echo host sent the correct message.");
	}else{
		console.log("Expected: " + value);
		console.log("Received: " + message);
	}
};

ws.onopen = function(){
    ws.send(value);
};
```

## Working with binary messages

```js
var wsHost = "http://my-sites-url.com/path/to/echo-web-socket-handler";
var ws = new WebSocket(wsHost);
var buffer = new ArrayBuffer(5); // 5 byte buffer
var bufferView = new DataView(buffer);

bufferView.setFloat32(0,Math.PI);
bufferView.setUint8(4,127);

ws.binaryType = 'arraybuffer';
ws.onmessage = function(message){
	var view = new DataView(message.data);
	console.log('Unit8:',view.getUnit8(4),'Float32:', view.getFloat32(0))
};

ws.onopen = function(){
	ws.send(buffer);
};
```

# Localization

## Number formatting
Number formatting, grouping digits according to the localization.

```js
const usNumberFormat = new Intl.NumberFormat('en-US');
const esNumberFormat = new Intl.NumberFormat('es-EsS');

const usNumber = usNumberFormat.format(99999999.99); // "99,999,999.99"
const esNumber = esNumberFormat.format(99999999.99); // "99.999.999,99"
```

## Number formatting
Number formatting, grouping digits according to the localization.

```js
const usCurrencyFormat = new Intl.NumberFormat('en-US',{style: 'currency',currency: 'USD'})
const esCurrencyFormat = new Intl.NumberFormat('es-ES',{style: 'currency',currency: 'EUR'})

const usCurrency = usCurrencyFormat.format(100.10); // "$100.10"
const esCurrency = esCurrencyFormat.format(100.10); // "100.10 €"
```

## Date and time formatting
Date time formatting, according to the localization.

```js
const usDateTimeFormatting = new Intl.DateTimeFormat('en-US');
const esDateTimeFormatting = new Intl.DateTimeFormat('es-ES');

const usDate = usDateTimeFormatting.format(new Date('2016-07-21')); // "7/21/2016"
const esDate = esDateTimeFormatting.format(new Date('2016-07-21')); // "21/7/2016"
```

# Geolocation

## Get updates when a user's location changes
You can also receive regular updates of the user's location; for example, as they move around while using a mobile
device. Location tracking over time can be very sensitive, so be sure to explain to the user ahead of time why you're
requesting this permission and how you'll use the data.

````js
if(navigator.geolocation){
	var watchId = navigator.geolocation.watchPosition(updateLocation, geolocationfailure);
}else{
	console.log("Geolocation is not supported by this browser.");
}
var updateLocation = function(position){
	console.log("New position at: " + position.coords.latitude + ", " + position.coords.longitude);
};
````

## Get a user's latitude and longitude

```js
if(navigator.geiolocation){
	navigator.geolocation.getCurrentPosition(geolocationSuccess, geolocationFailure);
}else{
	console.log("Geolocation is not supported by this browser.");
}
var geolocationSuccess = function(pos){
	console.log("Your location is " + pos.coords.latitude + ", " + pos.coords.longitude + ".");
};
var geolocationFailure = function(err){
	console.log("ERROR (" + err.code + "): " + err.message);
};
```

## More descriptive error codes
In the event that geolocation fails, your callback function will receive a PositionError object. The object will include
an attribute named code that will have a value of 1 , 2 , or 3 . Each of these numbers signiﬁes a diﬀerent kind of error;
the getErrorCode() function below takes the PositionError.code as its only argument and returns a string with
the name of the error that occurred.

```JS
var getErrorCode = function(err){
	switch(err.code){
		case err.PERMISSION_DENIED:
			return "PERMISSION_DENIED";
		case err.POSITION_UNAVAILABLE:
			return "POSITION_UNAVAILABLE";
		case err.TIMEOUT:
			return "TIMEOUT";
		default: 
			return "UNKNOWN_ERROR";
	}
};
```

It can be used in geolocationFailure() like so:

```js
var geolocationFailure = function(err){
	console.log("ERROR (" + getErrorCode(err) + "): " + err.message);
};
```

# Modularization Techniques

## ES6 Modules

In ECMAScript 6, when using the module syntax (import/export), each ﬁle becomes its own module with a private
namespace. Top-level functions and variables do not pollute the global namespace. To expose functions, classes,
and variables for other modules to import, you can use the export keyword.
Note: Although this is the oﬃcial method for creating JavaScript modules, it is not supported by any major
browsers right now. However, ES6 Modules are supported by many transpilers.

```js
export function greet(name){
	console.log("Hello %s!",name);
}
var myMethod = function(param){
	return "Here's what you said: " + param;
};
export {myMethod}
export class MyClass{
	test(){}
}
```

## Immediately invoked function expressions (IIFE)
Immediately invoked function expressions can be used to create a private scope while producing a public API.

```js
var Module = (function(){
	var privateData = 1;
	return{
		getPrivateData:function(){
			return privateData;
		}
	};
})();
Module.getPrivateData(); // 1
Module.privateData; // undefined
```

## Asynchronous Module Deﬁnition (AMD)
AMD is a module deﬁnition system that attempts to address some of the common issues with other systems like
CommonJS and anonymous closures.

Here's an example of AMD:

```js
define("myModule",["jquery","lodash"],function($,_){
	// This publicly accessible object is our module
	// Here we use an object, but it can be of any type
	var myModule = {};
	var privateVar = "Nothing outside of this module can see me";
	var privateFn = function(param){
		return "Here's what you said: " + param;
	};
	myModule.version = 1;
	myModule.moduleMethod = function(){
		// We can still access global variables from here, but it's better
		// if we use the passed ones
		return privateFn(windowTitle);
	};
	return myModule;
});
```

## CommonJS - Node.js
CommonJS is a popular modularization pattern that's used in Node.js.
The CommonJS system is centered around a require() function that loads other modules and an exports property
that lets modules export publicly accessible methods.
Here's an example of CommonJS, we'll load Lodash and Node.js' fs module:

```js
var fs = require("fs"), _ = require("lodash");
var myPrivateFn = function(param){
	return "Here's what you said: " + param;
};
export.myMethod = function(param){
	return myPrivateFn(param);
};
```

You can also export a function as the entire module using module.exports :

```js
module.export = function(){
	return "Hello!";
};
```

# Proxy

## Proxying property lookup
To inﬂuence property lookup, the get handler must be used.
In this example, we modify property lookup so that not only the value, but also the type of that value is returned.
We use Reﬂect to ease this.

```js
let handler = {
	get(target,property){
		if(!Reflect.has(target,property)){
			return{
				value: undefined,
				type: 'undefined'
			};
		}
		let value = Reflect.get(target,property);
		return{
			value: value,
			type: typeof value
		};
	}
};
let proxied = new Proxy({foo: 'bar'},handler);
console.log(proxied.foo); // logs `Object{value:"bar",type: "string"}`
```

##  Very simple proxy (using the set trap)
This proxy simply appends the string " went through proxy" to every string property set on the target object .

```js
let object = {};
let handler = {
	set(target,prop,value){
		if('string' === typeof value){
			target[prop] = value + " went trough proxy";
		}
	}
};
let proxied = new Proxy(object,handler);
proxied.example = "ExampleValue";
console.log(object);
// logs:{example:"ExampleValue went through proxy"}
// you could also access the object via proxied.target
```

# Behavioral Design Patterns

**Example usage:**

```js
function Employee(name){
	this.name = name;
	// Implement `notify` so the subject can pass us messages
	this.notify = function(meetingTime){
		console.log(this.name + ': There is a meeting at ' + meetingTime);
	};
}
var bob = new Employee('Bob');
var jane = new Employee('Jane');
var meetingAlerts = new Subject();
meetingAlerts.registerObserver(bob);
meetingAlerts.registerObserver(jane);
meetingAlerts.notifyObservers('4pm');
//Output:
// Bob: There is a meeting at 4pm
// Jane: There is a meeting at 4pm
```

Mediator Pattern
Think of the mediator pattern as the ﬂight control tower that controls planes in the air: it directs this plane to land
now, the second to wait, and the third to take oﬀ, etc. However no plane is ever allowed to talk to its peers.
This is how mediator works, it works as a communication hub among diﬀerent modules, this way you reduce
module dependency on each other, increase loose coupling, and consequently portability.
This Chatroom example explains how mediator patterns works:

```js
var Participant = function (name) {
    this.name = name;
    this.chatroom = null;
};

Participant.prototype = {
    send: function (message, to) {
        this.chatroom.send(message, this, to);
    },
    receive: function (message, from) {
        console.log(from.name + " to " + this.name + ": " + message);
    }
};

var Chatroom = function () {
    var participants = {};

    return {

        register: function (participant) {
            participants[participant.name] = participant;
            participant.chatroom = this;
        },

        send: function (message, from, to) {
            if (to) {                      // single message
                to.receive(message, from);
            } else {                       // broadcast message
                for (key in participants) {
                    if (participants[key] !== from) {
                        participants[key].receive(message, from);
                    }
                }
            }
        }
    };
};

function run() {

    var yoko = new Participant("Yoko");
    var john = new Participant("John");
    var paul = new Participant("Paul");
    var ringo = new Participant("Ringo");

    var chatroom = new Chatroom();
    chatroom.register(yoko);
    chatroom.register(john);
    chatroom.register(paul);
    chatroom.register(ringo);

    yoko.send("All you need is love.");
    yoko.send("I love you John.");
    john.send("Hey, no need to broadcast", yoko);
    paul.send("Ha, I heard that!");
    ringo.send("Paul, what do you think?", paul);
}
// Yoko to John: All you need is love.
// Yoko to Paul: All you need is love.
// Yoko to Ringo: All you need is love.
// Yoko to John: I love you John.
// Yoko to Paul: I love you John.
// Yoko to Ringo: I love you John.
// John to Yoko: Hey, no need to broadcast
// Paul to Yoko: Ha, I heard that!
// Paul to John: Ha, I heard that!
// Paul to Ringo: Ha, I heard that!
// Ringo to Paul: Paul, what do you think?
```

## Iterator
An iterator pattern provides a simple method for selecting, sequentially, the next item in a collection.

```js
class BeverageForPizza{
	constructor(preferenceRank){
		this.beverageList = beverageList;
		this.pointer = 0;
	}
	next(){
		return this.beverageList[this.pointer++];
	}
}
var withPepperoni = new BeverageForPizza(["Cola","Water","Beer"]);
withPepperoni.next(); // Cola
withPepperoni.next(); // Water
withPepperoni.next(); // Beer
```

**As a Generator**

```js
class FibonacciIterator{
	constructor(){
		this.previos = 1;
		this.beforePrevios = 1;
	}
	next(){
		var current = this.previos + this.beforePrevios;
		this.beforePrevios = this.previous;
		this.previous = current;
		return current;
	}
}
var fib = new FibonacciIterator();
fib.next(); // 2
fib.next(); // 3
fib.next(); // 5
```

In ECMAScript 2015

````js
function* FibonacciGenerator(){
	var previous = 1;
	var beforePrevious = 1;
	while(true){
		var current = previous + beforePrevious;
		beforePrevious = previous;
		previous = current;
		yield current; // This is like return but 
						// keeps the current state of the function 
						//i.e remembers its place between calls
	}
}
var fib = FibonacciGenerator();
fib.next().value; // 2
fib.next().value; // 3
fib.next().value; // 5
fib.next().done; // false
````

# Async functions (async/await)
async and await build on top of promises and generators to express asynchronous actions inline. This makes
asynchronous or callback code much easier to maintain.
Functions with the async keyword return a Promise , and can be called with that syntax.
Inside an async function the await keyword can be applied to any Promise , and will cause all of the function body
after the await to be executed after the promise resolves.

## Introduction
A function deﬁned as async is a function that can perform asynchronous actions but still look synchronous. The
way it's done is using the await keyword to defer the function while it waits for a Promise to resolve or reject.
Note: Async functions are a Stage 4 ("Finished") proposal on track to be included in the ECMAScript 2017 standard.
For instance, using the promise-based Fetch API:

```js
async function getJSON(url){
	try{
		const response = await fetch(url);
		return await response.json();
	}
	catch(err){
		// Rejections in the promise will get throw here
		console.error(err.message);
	}
}
```

# File API, Blobs and FileReaders

![image-20210708142309302](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708142309302.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JS</title>
        <style>
        </style>
    </head>
    <body>
        <input type="file" id="upload">
        <script>
            document.getElementById('upload').addEventListener('change',readFileAsString)
            function readFileAsString(){
                var files = this.files;
                if(files.length === 0){
                    console.log('No file is selected');
                    return;
                }
                var reader = new FileReader();
                reader.onload = function(event){
                    console.log('File content:',event.target.result);
                };
                reader.readAsText(files[0]);
            }
        </script>
    </body> 
</html>


```

Get the properties of the ﬁle
If you want to get the properties of the ﬁle (like the name or the size) you can do it before using the File Reader. If
we have the following html piece of code:

![image-20210708143440327](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210708143440327.png)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>JS</title>
        <style>
        </style>
    </head>
    <body>
        <input type="file" id="newFile">
        <script>
            document.getElementById('newFile').addEventListener('change',getFile);
            function getFile(event){
                var files = event.target.files,
                file = files[0];
                console.log('Name of the file',file.name);
                console.log('Size of the file',file.size);
            }
        </script>
    </body> 
</html>
```

## Client side csv download using Blob

```js
function downloadCsv(){
	var blob = new Blob([csvString]);
	if(window.navigator.msSaveOrOpenBlob){
		window.navigator.msSaveBlob(blob,"filename.csv");
	}else{
		var a = window.document.createElement("a");
		a.href = window.URL.createObjectURL(blob,{
			type: "text/plain"
		});
		a.download = "filename.csv";
		document.body.appendChild(a);
		a.click();
		document.body.removeChild(a);
	}
}
var string = "a1,a2,a3";
downloadCSV(string);
```

# Memory effciency

## Drawback of creating true private method
One drawback of creating private method in JavaScript is memory-ineﬃcient because a copy of the private method
will be created every time a new instance is created. See this simple example.

```js
function contact(first,last){
	this.firstName = first;
	this.lastName = last;
	this.mobile;
	// private method
	var formatPhoneNumber = function(number){
		// format phone number based on input
	};
	// public method 
	this.setMobileNumber = function(number){
		this.mobile = formatPhoneNumber(number);
	};
}
var rob = new contact('Rob','Sanderson');
var don = new contact('Donald','Trump');
var andy = new contact('Andy','Whitehall');
```

# Performance Tips
JavaScript, like any language, requires us to be judicious in the use of certain language features. Overuse of some
features can decrease performance, while some techniques can be used to increase performance.

## Initializing object properties with null
All modern JavaScript JIT compilers trying to optimize code based on expected object structures. Some tip from
mdn.

```js
function f1(){
	var P = function(){
		this.value = 1
	};
	var big_array = new Array(10000000).fill(1).map((x,index) => {
		p = new P();
		if(index > 5000000){
			p.x = "some_string";
		}
		return p;
	});
	big_array.reduce((sum,p) => sum + p.value,0);
}
function f2(){
	var P = function(){
		this.value = 1;
		this.x = null;
	};
	var big_array = new Array(10000000).fill(1).map((x,index) =>{
		p = new P();
		if(index > 5000000){
			p.x = "some_string";
		}
		return p;
	});
	big_array.reduce((sum,p) => sum + p.value,0);
}
function perform(){
	var start = perfomance.now();
	f1();
	var duration = perfomance.now() - start;
	console.log('duration of f1 ' + duration);
	
	start = perfomance.now();
	f2();
	duration = perfomance.now() - start;
	console.log('duration of f2' + duration);
}
```

## Reuse objects rather than recreate

**Example:**

```js
var i,a,b,len;
a = {x:0,y:0}
function test(){
	return {x:0,y:0};
}
function test1(a){
	a.x = 0;
	a.y = 0;
	return a;
}
for(i = 0;1 < 100; i ++){
	b = test();
}
for(i = 0; i < 100; i++){
	b = test1(a);
}
```

## Be consistent in use of Numbers
If the engine is able to correctly predict you're using a speciﬁc small type for your values, it will be able to optimize
the executed code.
In this example, we'll use this trivial function summing the elements of an array and outputting the time it took:

```js
var sum = (function(arr){
	var start = process.hrtime();
	var sum = 0;
	for(var i=0; i<arr.length; i++){
		sum += arr[i];
	}
	var diffSum = process.hrtime(start);
	console.log(`Summing took ${diffSum[0] * 1e9 + diffSum[1]} nanoseconds`);
	return sum;
})(arr);
```

```js
(function f(){
	var a=b=0;
})()
console.log('a: ' + a);
console.log('b: ' + b);
```

# Unit Testing JavaScript

## Unit Testing Promises with Mocha, Sinon, Chai
and Proxyquire
Here we have a simple class to be tested that returns a Promise based on the results of an external
ResponseProcessor that takes time to execute.
For simplicity we'll assume that the processResponse method won't ever fail.

```js
import {processResponse} from '../utils/response_processor';
const ping = () => {
	return new Promise((resolve,_reject) => {
		const response = processResponse(data);
		resolve(response);
	});
}
module.exports = ping;
```

This allows me to use es6 syntax. It references a test_helper that will look like

```js
import chai from 'chai';
import sinon from 'sinon';
import sinonChai from 'sinon-chai';
import chaiAsPromised from 'chai-as-promised';
import sinonStubPromise from 'sinon-stub-promise';
chai.use(sinonChai);
chai.use(chaiAsPromised);
sinonStubPromise(sinon);
```

Proxyquire allows us to inject our own stub in the place of the external ResponseProcessor . We can then use sinon
to spy on that stub's methods. We use the extensions to chai that chai-as-promised injects to check that the
ping() method's promise is fullfilled , and that it eventually returns the required response.

```js
import {expect}			from 'chai';
import sinon			from 'sinon';
import proxyquire		from 'proxyquire';

let fromattingStub = {
	wrapResponse: ()=>{}
}
let ping = poxyquire('../../../src/api/ping',{
	'../utils/formatting': formattingStub
});
describe('ping',() => {
	let wrapResponseSpy,pingResult;
	const response = 'some response';
	
	beforeEach(() => {
		wrapResponseSpy = sinon.stub(formattingStub,'wrapResponse').returns(response);
		pingResult = ping();
	})
	afterEach(() => {
		formattingStub.wrapResponse.restore();
	})
	it('returns a fullfilled promise',() => {
		expect(pingResult).to.be.fulfilled;
	})
	it('eventually returns the correct response', () =>{
		expect(pingResult).to.eventually.equal(response);
	})
});
```

# Web Cryptography API

## Creating digests (e.g. SHA-256)

```js
var input = new TextEncoder('utf-8').encode('Hello world!');
crypto.subtle.digest('SHA-256',input)
.then(function(digest){
	var view = new DataView(digest);
	var hexstr = '';
	for(var i = 0;i < view.byteLength; i++){
		var b = view.getUint8(i);
		hexstr += '0123456789abcdef'[(b& 0xf0) >> 4];
		hexstr += '0123456789abcdef'[(b & 0x0f)];
	}
	console.log(hexstr);
	var digestAsArray = new Uint8Array(digest);
	console.log(digestAsArray);
})
.catch(function(err){
	console.error(err);
});
```

## Converting PEM key pair to CryptoKey
So, have you ever wondered how to use your PEM RSA key pair that was generated by OpenSSL in Web
Cryptography API? If the answers is yes. Great! You are going to ﬁnd out.
NOTE: This process can also be used for public key, you only need to change preﬁx and suﬃx to:

```js
function removeLines(str){
	return str.replace("\n","");
}
function base64ToArrayBuffer(b64){
	var byteString = window.atob(b64);
	var byteArray = new Uint8Array(byteString.length);
	for(var i=0; i < byteString.length; i++){
		byteArray[i] = byteString.charCodeAt(i);
	}
	return byteArray;
}
function pemToArrayBuffer(pem){
	var b64Lines = removeLines(pem);
	var b64Prefix = b64Lines.replace('-----BEGIN PRIVATE KEY-----','');
	var b64Final = b64Prefix.replace('-----END PRIVATE KEY-----','');
	return base64ToArrayBuffer(b64Final);
}
window.crypto.subtle.importKey(
	"pkcs8",
	pemToArrayBuffer(yourprivatekey),
	{
		name: "RSA-OAEP",
		hash:{name: "SHA-256"} // or SHA-512
	},
	true
	["decrypt"]
)then(function(importedPrivateKey){
	console.log(importedPrivateKey);
}).catch(function(err){
	console.log(err);
});
```

