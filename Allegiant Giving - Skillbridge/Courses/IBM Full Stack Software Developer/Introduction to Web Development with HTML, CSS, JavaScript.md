# Courses
1. [IBM Full Stack Software Developer Professional](https://www.coursera.org/programs/allegiant-giving-corporation-on-demand-learning-program-mjqmr/professional-certificates/ibm-full-stack-cloud-developer)
	1. [Introduction to Web Development...](https://www.coursera.org/learn/introduction-to-web-development-with-html-css-javacript)

# Introduction to Application Development

- Front-end developers work on the parts of the website or app that the user sees and interact with. 
- Back-end developers work on the logic and functionality that keeps the website or app running and responding to users’ inputs. 
- Full-stack developers have both sets of skills. 
- Front-end developers and back-end developers work closely together. 
- Frameworks and libraries extend the functionality of coding languages such as JavaScript and Python. 
- Common languages for front-end development include: HTML, CSS, and JavaScript. 
- Common languages and frameworks for back-end development include: Python, Django, and Flask. 
- Version control systems keep track of changes and resolve conflicts between them. 
- CI/CD (Continuous Integration with Continuous Delivery/Deployment) is a best practice developers use to deliver frequent changes reliably.
# HTML Overview

- HTML provides the basic structure and content for a website using tags. 
- Tags represent the elements of an HTML page. 
- The HTML DOM Tree describes how a website is structured. 
- HTML uses APIs to enhance the user experience, providing features for advanced animation, audio, and video. 
- Scripting provides a more interactive user experience when browsing websites. 
- It is recommended to not rely on scripting as it can be disabled. 
- HTML5 sandboxes help manage iframe mashups.  
- HTML5 Browser Support Tables describe which browsers support which HTML5 features. 
- JavaScript is used to check if an element is supported by a browser. 
- CSS provides consistent style and design throughout the website. 
- There are two types of CSS layouts to design websites: fluid and fixed.
## Non HTML5 Specific Tags

**Comments**

HTML comments are used to include information in your code that is not to be displayed in your browser. This tag provides a way to document your source code and give more information about the code thus, enabling other users to understand the purpose of the code when working on a large database with other developers.

To insert a comment into your code, use the comment tag `<!-- [YOUR COMMENT HERE] -->`, replacing `[YOUR COMMENT HERE]` with your comment. There are no limitations to what your comment could be, it can be text (both single-line and multi-line) or even other additional HTML tags.

**Div**

The `<div>` tag defines a division of the page, and is used to group content together. Any type of content can be placed in a div tag, and it is not necessary that it should be semantically related.

`<div>` tags are commonly used when many elements are required to have the same format. Grouping such elements together in the same `<div>` tag enables a developer to easily style them by either using a class or an id.

When using a `<div>` tag, note that browsers will insert a line break before and after the element.

```HTML
<div>
	<h1>This is a heading in a div element</h1>
	<p>This is some text in a div element.</p>
</div>
```

## Structural HTML5 Elements

**Section**

The `<section>` element is used to group content in a more specific way than the `<div>` tag. The content within a `<section>` element is grouped in a semantically meaningful way, that is, there is a reason, other than for styling purposes for putting the content together. Content within a `<section>` tag has a theme, which is usually indicated by a heading tag (e.g. `<h1>`) used immediately after the opening `<section>` tag.

```HTML
<section>
	<h1>Section 1</h1>
	<p>This is text related to section 1.</p>
</section>

<section>
	<h1>Section 2</h1>
	<p>This is some text related to section 2.</p>
</section>
```

**Article**

An `<article>` element is even more specific than a `<section>`tag. It is used to group together semantically related, self-contained content which can be meaningful on its own. Similar to the `<section>` element, articles usually have headings immediately after their opening tag to indicate what the article is about.

```HTML
<article>
	<h1>Article 1</h1>
	<p>This paragraph is related only to article one and is meaningful on its own, without the rest of the code.</p>
</article>

<article>
	<h1>Article 2</h1>
	<p>This paragraph is related only to article two and is meaningful on its own, without the rest of the code.</p>
</article>
```

**Header**

The `<header>` element is a container used to define the introductory/header information of a page. It can be used for a navigational bar, or to wrap a table of contents.

An HTML document can contain more than one `<header>` elements, however, they cannot be placed within `<address>`, `<footer>`, or other `<header>` elements.

**Footer**

A `<footer>` element defines the area at the bottom of the page (known as a footer). This often contains copyright information, contact information, and contact links.

```HTML
<body>
	<article>
		<header>
			<h1>G8 summit protests</h1>
		</header>
		<div>
			<section id="public">
				<h1>Public demonstrations</h1>
				<p>...more...</p>               
			</section>
			<section id="control">
				<h1>Crowd control</h1>
				<p>...more...</p>               
			</section>         
		</div>
		<footer>
			<p>Published today.</p>
		</footer>
	</article>
</body>
```
## HTML5 Elements for Grouping

**Aside**

The `<aside>` element is used to provide additional information that is related to the main discussion​. It lets you display further content or additional resources without detracting from the main discussion​, and is often placed as a sidebar in a document.

While the `<aside>` element itself is not displayed different from the rest of the content, it is useful for understanding your code and for styling purposes.

```HTML
<p>This is a paragraph of text that casually mentions a concept and continues explaining the main point</p>

<aside>
	<h4>Concept Definition</h4>
	<p>This goes over the concept mentioned in the paragraph to provide readers with further explanation if needed. However, it does not detract from the main content.</p>
</aside>
```

**Figure**

The `<figure>` tag defines self-contained content, such as a diagram or photo, that is referred to from the main content​. The content within the `<figure>` element should be related to the main content, but still independant in such a way that if removed from the document, it would not affect the flow.

**Figcaption**

The `<figcaption>` tag defines the caption for the contents of the `<figure>` element​. It can be placed as the first or last child element within the `<figure>` element​.

```HTML
<figure>
	<img src="images/IDSNlogo.png" width="500" height="500"/>
	<figcaption>IBM Developer Skills Network Logo</figcaption>
</figure>
```

## Navigational Elements

The `<nav>` element is used as a way to group navigational elements which are used to move between pages, such as the navigation bar typically found at the top of websites.

The `<nav>` tag is a convenience tag which does not alter the appearance on webpages. However, it is useful in styling all navigational elements, as well as omitting the content for certain functionalities, such as with screen readers.

```HTML
<nav>
	<div class="menu">
		<a href="#">Home</a> |
		<a href="about.html">About</a> |
		<a href="register.html">Register</a> |
		<a href="#">Sign in</a>
	</div>
</nav>
```
## Additional HTML5 Elements

This section will introduce you to new HTML5 elements which are commonly used. This is not a comprehensive list, but is meant to familiarize you with the most common ones.

### Embedding Content

**Audio**

The `<audio>` element is used to embed sound content, such as music or podcasts. It contains one or more `<source>` tags with different audio sources (e.g. MP3, WAV), so the browser can select the first supported source to play.

If a browser does not support the audio formats provided, the browser will instead display any text within the `<audio>` element.

```HTML
<audio>
	<source src="soundtrack.mp3" type="audio/mpeg">
	<source src="soundtrack.ogg" type="audio/ogg">
	Your browser does not support the audio formats provided.
</audio>
```

**Canvas**

The `<canvas>` element is used to draw graphics via scripting. JavaScript is one way to utilize scripting to draw these graphics, as shown in the example below.

```HTML
<canvas>
	Your browser does not support the canvas tag.
</canvas>

<script>
	var canvas = document.getElementsByTagName("canvas")[0];
	var context = canvas.getContext("2d");
	context.fillRect(0, 0, 100, 100);
</script>
```

If a browser does not support graphical content or JavaScript is disabled, the browser will display any text within the `<canvas>` element.

**Embed**

The `<embed>` element is used as a container to embed external resources such as media players and plug-in applications into your web page.

```HTML
<embed type="text/html" src="another_webpage.html">
```

**Track**

The `<track>` element defines text tracks, such as subtitles or captions, for `<audio>` and `<video>` elements. This text should be visible as the related media source it playing, and are formatted in the WebVTT (.vtt) format.

```HTML
<video>
	<source src="common_html_elements.mp4" type="video/mp4">
	<track src="english_subtitles.vtt" kind="subtitles" srclang="en" label="English">
	<track src="spanish_subtitles.vtt" kind="subtitles" srclang="es" label="Spanish">
</video>
```

# CSS Overview & HTML 5 Elements

- CSS creates a uniform look throughout each element of each page of the website. 
- CSS is usually coded in external style sheets and creates base styles for a website. 
- CSS frameworks assists in implementing UI elements and creating dynamic web pages. 
- CSS has two types of frameworks: 
	- Utility-first frameworks, which provide utility classes to help in building one's own styles and layouts. 
	- Component frameworks, which provide a wide selection of pre-styled components and templates that can be implemented onto a website. 
- Plain (Vanilla) CSS lets developers write the styles and layouts of a website. 
- HTML5 elements provide structure and function to websites. 
- HTML5 uses the `<input>` tag to allow users to input information.
# HTML/CSS - Glossary

|**Term**|**Definition**|
|---|---|
|**AngularJS**|An open-source JavaScript framework for dynamic web applications|
|**Application Programming Interface (API)**|Code that allows two software programs to communicate with each other.|
|**Build Automation**|Allow you to download dependencies, compile code, package binary code, run tests, deploy to production.|
|**Build Automation Servers**|Execute build-automation utilities on a scheduled or triggered basis.|
|**Build Automation Utilities**|Generate executables by compiling and linking code.|
|**Component Framework**|Component frameworks provide pre-styled components and templates which are easy to add to any website.|
|**Continuous Integration/ Continuous Deployment (CI/CD)**|A method for releasing code and integrating it into code that has already been developed in order to prevent the application from breaking throughout the app’s lifecycle.|
|**CSS**|"Cascading Style Sheet"s is a style sheet language that describes how HTML elements are displayed​. It is the design that is layered over the top of an HTML web page​.|
|**Django**| A framework for Python web development. |
|**DOM Tree**|“Document Object Model” is the data representation of the objects that comprise the structure and content of a document on the web.|
|**Dynamic Content**|Data that is created each time a request is sent to a server.|
|**Endpoint**|The point at which an API connects with the software program.|
|**Fixed Layout**|A fixed layout is a layout where ​you specify the height and width of elements, and those values remain the same regardless of which operating system or browser you use to access the website.|
|**Fluid Layout**|A fluid layout is a layout in which ​the height and width of elements is flexible ​and can expand or contract based on the browser window, the operating system, and other user preferences.|
|**Frameworks**|Provide a standard way to build an application. Frameworks dictate architecture and program flow.|
|**IDE**|“Integrated Development Environment” Helps create and manage code.|
|**Inversion of Control**|A predefined workflow where the developer is not in full control of how the application operates.|
|**JavaScript Framework**|An application framework written in JavaScript to create responsive sites.|
|**LESS**|“Learner Style Sheets” add more style and functions to CSS.|
|**less.js**|A JavaScript tool that converts LESS styles to CSS.|
|**Libraries**|Reusable collections of code|
|**Opinionated**|Frameworks that have a lot of control are sometimes considered “opinionated”.|
|**Package Managers**|Coordinate with file archivers to extract packages. Verify check sums and digital certificates. Locate, download, and install updates of existing software from a repository as well as manage dependencies. Common package managers include the following: Debian Package Management System (DPMS), Red Hat Package Manager for Linux, Chocolatery for Windows, Homebrew and MacPorts for MacOS.|
|**Packages**|Archive files that include app files, instructions for installation, and metadata.|
|**React.js**|A JavaScript framework developed by Facebook that helps build and drop elements onto a page.|
|**Responsive Design**|Design technique that automatically resizes a display to adapt to a specific screen size.|
|**Route**|Allows front-end client to plug into correct socket on the backend. They are the paths that network traffic takes from a virtual machine (VM) instance to other destinations.|
|**SASS**|“Syntactically Awesome Stylesheets” are an extension of CSS.|
|**Static Content**|A display of data that has been previously stored on a server.|
|**Utility Framework**|The utility framework provides utility classes that are scoped to individual CSS properties, which helps in building custom designs in HTML files.|
|**Version Control**|Allows you to revert to earlier versions of code, resolves conflicts between the same files, and split and merge different code branches.|
|**Vue.js**|A community-based JavaScript framework focused on UI. Includes UI components such as buttons and other visual elements, and is both a library and a framework.|
|**Web Storage APIs**|APIs that allow data storage in a browser.|
|**XHTML**|An “eXtensible Hypertext Markup Language” similar to HTML but with stricter formatting rules.|
|**XML**|An “eXtensible Markup Language” Designed to store and transport data allowing users to define their own markup languages, primarily to displaydocuments on the web.|

# JavaScript APIs

To understand what a JavaScript API is, it is important to first know what an API is. An API, or Application Programming Interface, is a way for two applications to communicate with each other. It delivers your request to another device, such as a database, and returns the response back to you.

Imagine you are sitting in a restaurant and have selected your order. The menu outlines a list of food items, and the corresponding meals are prepared in the kitchen. Your waiter is the link between you and the kitchen, who communicates your order to the kitchen and returns the food back to you. This communication is similar to how APIs work. An API is analogous to a waiter, as it communicates a request from one device to another, and returns the response back to the first device.

The menu in the example is the API documentation. In a restaurant, if you order a food item which does not exist on the menu, the waiter will inform you that it is an invalid choice, and will be incapable of delivering the food item. Similarly, each API has documentation that outlines the requests you are allowed to make, and the type of response you should expect to recieve. If you try to make an invalid request, you will come across an error.

JavaScript APIs are Application Programming Interfaces that use JavaScript scripting to dynamically access and modify content.
## REST Architecture

Most JavaScript APIs follow the Representational State Transfer (REST) architectural style. These are referred to as RESTful APIs, and follow the CRUD paradigm. CRUD stands for Create, Read, Update, and Delete, and model the four basic functionalities needed when communicating between services and with a database. In a REST environment, these CRUD operations are often aliased as follows:

- Create → POST
- Read → GET
- Update → PUT
- Delete → DELETE

As an example, imagine an API which communicates with a banking service to process online payments. It is possible to use all four CRUD operations for this API. An example of each is provided below.

|Method|URL|Description|
|---|---|---|
|POST|api/customer|Create a new banking customer|
|GET|api/customers/{id}|Retrieve the information of a customer|
|PUT|api/customers/{id}|Update information for a specific customer|
|DELETE|api/customers/{id}|Delete a banking customer|

The URLs in each example are important, as they determine the specific item/customer that is being accessed.

In the POST request, you can see that a new customer is created with the API. Depending on the specifications of the API, this may include options to provide data for this customer, such as a name or credit card details. It may also automatically generate new information upon creation, such as an id.

The GET request allows you to retrieve all the information associated with a customer. The API assumes a unique id for each customer, that is used in the URL to specify which customer’s information you are searching. A response for this request can come in many different formats, such as JSON or XML, depending on the API.

In the PUT request, you are able to update the information for a specific customer. This will overwrite the current data with new data. Similar to the GET request, you can specify a specific customer using the id. You can provide new data to be updated in different ways that are specific to the API. Some APIs allow you to include a “body” in which you can specify a load of data to be sent with the request. For example, you can attach the following body to the PUT request in order to update a customer’s first and last name:

```JSON
{
	"first_name": "Thomas",
	"last_name": "Watson"
}
```

In the DELETE request given in the example, you can remove a customer entirely by once again providing the id.
## Document Object Model (DOM) API

The Document Object Model (DOM) API is one of the most basic JavaScript APIs available. It connects web pages to scripts by representing the structure of a document (e.g. an HTML web page) in memory, making it accessible for modfication as required.

The DOM API is covered in more detail in the videos, and will not be reviewed here.
## XMLHttpRequest

A popular JavaScript API is XMLHttpRequest (XHR), which allows you to retrieve data without refreshing the entire page. This is important when you to want to update only a part of a page without disrupting what a user is currently doing on the page.

XMLHttpRequest is used heavily in Asynchronous JavaScript And XML (AJAX) programming. Full documentation on its usage can be found on [this page](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest).
## Advanced APIs

There are more advanced JavaScript APIs available, each with a different use and specification. Many of these APIs can be found on the [official Mozilla Developer website](https://developer.mozilla.org/en-US/docs/Web/API) or you can search the internet for the required API.

## Summary

- JavaScript is a scripting language that enables developers to add dynamic content to webpages.
- JavaScript variables are declared using the var keyword and take their type from the value assigned.
- Program execution is controlled by statements like If…Then…Else, Switch, For loops, and While loops.
- JavaScript uses blocks of code, called functions, that can be called from anywhere in the script.
- New methods and properties can be added to an object by modifying the prototype for that object.
- Prototypes allow you to define properties and methods for all instances of a specific object.
- Client-side scripts are programs that accompany HTML documents and are used by developers to incorporate more interactive elements.
- The script tag can incorporate a script within an HTML document or call a script from an external file.
- The Document Object Model (DOM) is the programming interface between HTML or XHTML and JavaScript.
- Developers can access HTML DOM elements from JavaScript scripts using the correct DOM notation.
- APIs are often used to access HTML DOM elements in web pages.

|**Term**|**Definition**|
|---|---|
|**AJAX**|“Asynchronous JavaScript and XML” that encompasses more than asynchronous server calls through JavaScript and XML. It is not programing language or technology but rather a programming concept. Ajax represents a series of techniques that provide richer, interactive web applications through HTML, JavaScript, Cascading style sheets, and modifying the web page through the Document Object Model. The name is misleading though because nowadays, JSON is commonly used instead of XML.|
|**Anonymous Functions**|A type of function that has no name or we can say which is without any name. It is declared without any identifier and is often used as a parameter of another function. It is a common way to execute a function immediately after its declaration.|
|**Array**|A data structure that aids the programmer in the storage and retrieval of data by indexed keys. Arrays use a zero-based indexing scheme, meaning that the first element of an array has an index of zero. Arrays grow or shrink dynamically by adding or removing elements.|
|**Classes**|Classes act as a blueprint or template for building objects with similar characteristics and behaviours. A class encapsulates data (in the form of properties) and functions (in the form of methods) that work on that data.|
|**Client-Side Script**|A program that accompanies an HTML doc or embedded in HTML. Scripts run during load of a document or when an action is performed.  <br>They can be used to validate forms, process input, or dynamically create document elements.  <br>Embed a script in HTML, with the `<script>` tag in either of the following ways:  <br>  • `<script> // JS code </script>`  <br>  • `<script src="path name"></script>`  <br>Use `<noscript>` tag for browsers with JavaScript disabled or ones that don’t support JavaScript.|
|**Document Objects**|Document representing the main web page that gives access to all HTML elements on the page. When page is loaded HTML doc becomes a document. It is referred to with “document”.|
|**DOM**|“Document Object Model” is a programming interface (API) between HTML and JavaScript. It allows for dynamically accessing and updating content, structure, and style. JavaScript uses the DOM to access and modify web page elements in the browser.|
|**Element Nodes**|All HTML tags.|
|**Element Objects**|The most general base class that all element objects in a Document inherit. It only has methods and properties common to all elements. Everything in a HTML page is an element. And one element can have other elements nested within itself.|
|**Event**|An event is something either a browser or a user does that the JavaScript can react to such as a button click or when a user submits input on a form.|
|**Event Binding**|Refers to telling the browser that a function should be called whenever some ‘event’ occurs.|
|**Event Handlers**|A function that declares what to do when an action is performed such as the click of a button. Example:  <br>`<button type="button" onclick="showAnswers()"> Show Solution`  <br> `<script>`  <br>  `function showAnswers() {`  <br>   `//code`  <br>   `alert("A")`  <br>  `}`  <br> `</script>`  <br>`</button>`  <br>Note that showAnswers() is an event handler.|
|**Extend**|This keyword is used in class declarations or class expressions to create a class that **is** a child of another class.|
|**Functions**|Functions are modules of code that execute a particular task. They may take-in data, called arguments or parameters, and sometimes return data as well, called the return value. Functions are commonly defined with this syntax:  <br>`function functionName() {`  <br> `// function code;`  <br> `// optional return statement;`  <br>`}`|
|**IIFE**|“Immediately Invoked Function Expression” runs immediately after it is defined.  After the function executes it cannot be called again elsewhere in the program.  It is a type of self-executing function.|
|**Nodes**|The basis of all elements in the Document Object Model (DOM) structure.|
|**Objects**|Objects are instances created from a class. They are real-world entities that represent the characteristics defined by the class. Objects have a special set of properties that store data and methods that specify behaviours. These methods and properties can be accessed and changed to carry out specific tasks and communicate with other programs.|
|**Prototypes**|A function prototype lets you easily define and add properties or methods to an object. Prototypes exist for all objects that can be created with the keyword”new”. All object constructors create objects that inherit properties and methods that are defined by the prototype. At instantiation objects inherit the current state of the prototype. Note however, that scripts can override prototype properties and functions. Following is an example of using a prototype to add a method to the Car class:  <br>`function Car(make, model, year) {`  <br> `this.make = make;`  <br> `this.model = model;`  <br> `this.year = year;`  <br>`}`  <br>`Car.prototype.getName = function() {`  <br> `return this.make + ‘ ’ + this.model + ‘ ’ + this.year;`  <br>`}`|
|**Script**|Offers developers  means to modify and extend HTML documents in highly interactive ways. Scripts can be used to validate forms or to process input as it is typed. Scripts can be triggered by events that occur on a web page, such as the clicking of a button. Scripts can be used to dynamically create document elements on an HTML page.|
|**Self-Executing Functions**|Often used to initialize data or declare DOM elements.  These functions can be  anonymous.|
|**Text Nodes**|The nodes that contain actual text that go between an element start tag and end tag.|
|**this**|Keyword “this” refers to current instance of the object. The value of “this” can vary depending on how the object is called.|
## Javascript - Cheatsheet

|Class or Method|Description|Example|
|---|---|---|
|`appendChild()`|An HTML DOM method that after creating an element, you can use this function to place the element in the appropriate location within the document. The element to append is the only parameter.|`//Creates the element <p> and text “Hello World”. Appends Hello World <p> to the HTML document.`  <br>`<head>`  <br> `<script>`  <br>  `function addPara() {`  <br>   `var newPara = document.createElement(“p”);`  <br>   `var newText = document.createTextNode(“Hello World!”);`  <br>   `newPara.appendChild(newText);`  <br>   `document.body.appendChild(newPara);`  <br>  `}`  <br> `</script>`  <br>`</head>`  <br>`<body onload=“addPara()”>`  <br>`</body>`|
|`Arrays`|Created by declaring the array elements in [ ]. An array can be assigned to a variable, usually using the keyword const or var. Arrays use zero based indexing to access their elements.|`const Beatles = [“Ringo”, “Paul”, “George”, “John”];`  <br>`//Here Beatles[0] is “Ringo”.`|
|`Date()`|Constructor is new Date([optional parameters]). If the constructor is declared with no parameters, it returns current local date and time. New dates can be created by passing parameters to new Date function.|`//create a new date from a string`  <br>`var newDate = new Date(“2021-1-17 13:15:30”);`  <br>  <br>`//create a new date instance representing 17 Jan 2021 00:00:00`  <br>`//note that the month number is zero-based`  <br>`var newDate = new Date(2021, 0, 17);`|
|`document.createElement()`|Takes one tag name parameter and creates an element with that name. Can place the element elsewhere on the page using functions like insertBefore(), appendChild(), replaceChild().|`//Creates the element <p> and text “Hello World”. Appends Hello World <p> to the HTML document.`  <br>`<head>`  <br> `<script>`  <br>  `function addPara() {`  <br>   `var newPara = document.createElement(“p”);`  <br>   `var newText = document.createTextNode(“Hello World!”);`  <br>   `newPara.appendChild(newText);`  <br>   `document.body.appendChild(newPara);`  <br>  `}`  <br> `</script>`  <br>`</head>`  <br>`<body onload=“addPara()”>`  <br>`</body>`|
|`document.createTextNode()`|Takes a string as input text and returns a text node with the input text.|`//Creates the element <p> and text “Hello World”. Appends Hello World <p> to the HTML document.`  <br>`<head>`  <br> `<script>`  <br>  `function addPara() {`  <br>   `var newPara = document.createElement(“p”);`  <br>   `var newText = document.createTextNode(“Hello World!”);`  <br>   `newPara.appendChild(newText);`  <br>   `document.body.appendChild(newPara);`  <br>  `}`  <br> `</script>`  <br>`</head>`  <br>`<body onload=“addPara()”>`  <br>`</body>`|
|`document.getElementByID()`|A method of the DOM that takes an ID value parameter and returns an element that matches the id.|`//Changes the content of the div to “Hello World!”`  <br>`<div id=“div1”>`  <br> `<p>Hello</p>`  <br> `<p>Hello</p>`  <br>`</div>`  <br>  <br>`<script>`  <br> `document.getElementById(“div1”).innerHTML = “<p>Hello World!</p>”;`  <br>`</script>`|
|`document.getElementsByTagName()`|A method of the DOM that takes a tag name parameter and returns an array called “NodeList” that contains elements with the specified tag name.|`//Gets an array of all elements in a document with the <p> tag.`  <br>`var tagNameArray = document.getElementsByTagName(“p”);`|
|`document.write()`|Writes HTML or JavaScript to a document. Note that it overwrites any other text in the document so is mostly used for testing purposes only.|`//Writes “Hello World” to the output stream.`  <br>`document.write(“Hello World”);`|
|`element.getAttribute()`|Returns the value of the specified attribute. Takes one parameter: the attribute name whose value is to be returned.|`//Removes the CSS style color blue`  <br>`<div id="div1" style="color: blue"></div>`  <br>`<script>`  <br> `var div1 = document.getelementById("div1").getAttribute(“style”);`  <br>`</script>`|
|`element.innerHTML()`|A property of the Element class that returns or alters contents of an HTML element as a text string.|`//Changes the content of the div to “Hello World!”`  <br>`<div id=“div1”>`  <br> `<p>Hello</p>`  <br> `<p>Hello</p>`  <br>`</div>`  <br>  <br>`<script>`  <br> `document.getElementById(“div1”).innerHTML = “<p>Hello World!</p>”;`  <br>`</script>`|
|`element.removeAttribute()`|A property of the Element class that removes all previously set inline CSS styles for a particular element. Takes one parameter: the attribute name that is being removed.|`//Removes the CSS style color blue`  <br>`<div id="div1" style="color: blue"></div>`  <br>`<script>`  <br> `var div1 = document.getelementById("div1").getAttribute(“style”);`  <br>`</script>`|
|`element.setAttribute()`|A property of the Element class that overwrites all previously set inline CSS styles for a particular element. Takes two parameters: the attribute name that is being set and the attribute value the attribute is set to.|`//In all elements named “theImage” sets the name of all src attributes to “another.gif”`  <br>`document.getElementById(“theImage”).setAttribute(“src”, “another.gif”);`|
|`element.style()`|A property of the Element class that returns or alters inline CSS. Syntax is element.style.propertyName = value|`//Changes the CSS style color from blue to red`  <br>`<div id="div1" style="color: blue"></div>`  <br>`<script>`  <br> `var div1 = document.getelementById("div1");`  <br> `div1.style.color = "red";`  <br>`</script>`|
|`Error Objects`|Instance creates two properties about the error: message that contains description of the error and the name property identifies the type of error. Generic error plus 6 other core errors: TypeError, RangeError, URIError, EvalError, ReferenceError, SyntaxError.  <br>Error object can be extended to create custom error messages using the throw keyword.|`//Catch statement defines a block of code to be executed if an error occurs in the try block.`  <br>`catch (err) {`  <br> `document.getElementById(“myfile”).innerHTML = err.name;`  <br>`}`  <br>`//Creates custom error message`  <br>`throw new Error(“Only values 1-10 are permitted”);`|
|`History Objects`|The history object is part of the window object and contains the URLs visited by the user within a browser window. It exposes useful methods and properties that let you navigate back and forth through the user's history and manipulate the contents of the history stack.|`//Go back two pages if the history exists in the history list.`  <br>`history.go(-2);`|
|`insertBefore()`|An HTML DOM method that, after creating an element, places a child element in the appropriate location before an existing child. The method takes two parameters, the node object to be inserted and the existing node to insert before.|`//Creates a new <li> element and places it in the elementList before the first child of <ul>`  <br>`let newLI = document.createElement("li");`  <br>`newLI.innerText = "new Element";`  <br>`let elementList = document.getElementById("thisList");`  <br>`elementList.insertBefore(newLI, elementList.childNodes[0]);`|
|`Location Objects`|The location object is part of the window object and contains information about the current URL.|`//Returns the hostname property`  <br>`let myhost = location.hostname;`  <br>`newLI.innerText = "new Element";`|
|`Navigator Objects`|The navigator object is part of the window object class in the DOM that represents the client Internet browser, also called the user agent. There is no standard for this object so what it returns differs from browser to browser.|`//Retrieves the name of the browser`  <br>`var browsername = navigator.appName;`|
|`onload()`|A DOM event that starts a method when a page is loaded.|`//Executes myFunction after MyHTMLPage has been loaded`  <br>`document.getElementById(“MyHTMLPage”).onload = function () {myFunction};`|
|`replaceChild()`|After creating an element, this function replaces a child node with a new node.|`//Creates a new node and replaces the second element in “thisList” with the word “blue”`  <br>`let secondBullet = document.createTextNode(“blue”);`  <br>`var myList = document.getElementById(“thisList”).childNodes[1];`  <br>`myList.replaceChild(secondBullet,   myList.childNodes[1]);`|
|`Screen Objects`|The screen object is part of the window object class in the DOM that can be used to return properties about the user’s screen.|`//Returns the height and width of the user’s screen`  <br>`var height=screen.height;`  <br>`var width=screen.width;`|
|`Window Objects`|The DOM window object is at the top of the DOM hierarchy and serves as the global object. Everything in the DOM takes place in a window. The window object controls the environment that contains the document.|`//Opens a new browser window with the specified URL`  <br>`window.open(“http://www.w3schools.com”);`|
|`window.open()`|Opens a new window. The first parameter is a path, a URL, or an empty string, and optional parameters include the window name, features such as the placement of the window or the dimensions, and a Boolean replace value. The feature parameter is a comma separated string of name-value pairs and the replace parameter is an optional Boolean. This parameter has been deprecated so modern browsers may not support it. This method returns a reference to the new window object.|`//Opens a new window that opens the IBM home page and has a width of 600 and a height of 800)`  <br>`let thisWindow = window.open(“http://www.ibm.com”, “myWindow”, “width”=600, “height”=800);`|
|`window.scrollTo()`|Scrolls to a particular place in a window. Parameters include the x-coordinate which is the left-most pixel and the y-coordinate which is the upper-most pixel.|`//Scrolls the window to the pixel located at the coordinate (20, 200)`  <br>`window.scrollTo(20, 200);`|
|`Wrapper Objects`|Primitive types can be converted to objects using wrapper objects. They are the same name as the primitive except they start with uppercase letter. The `typeof` keyword returns a string indicating the data type of the operand.|`//Enables the use of properties and methods of the String class such as the property n.length`  <br>`let n = new String (“abc”);`  <br>  <br>`//Returns string`  <br>`typeof “abc”;`  <br>  <br>`//Returns object`  <br>`typeof new String(“abc”);`|
 