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
# Glossary

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
