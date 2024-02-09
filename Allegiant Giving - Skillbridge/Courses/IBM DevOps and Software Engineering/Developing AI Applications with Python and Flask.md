---
tags:
  - Python
  - Flask
  - AI
---
# Courses
1. [IBM DevOps and Software Engineering Professional Certificate](https://www.coursera.org/programs/allegiant-giving-corporation-on-demand-learning-program-mjqmr/professional-certificates/devops-and-software-engineering)
	1. [Developing AI Applications with Python and Flask](https://www.coursera.org/learn/python-project-for-ai-application-development)

# Static Code Analysis (Resources)

Static code analysis, or static analysis, is an application code efficiency verification activity that analyses source code for quality, reliability, and security without executing the code. Static code analysis is an essential part of any application development cycle and is available as a part of multiple frameworks with Python.

One of the most popular frameworks is PyLint. PyLint basically evaluates the code against compliance with the PEP8 coding style guide and generates comments wherever it finds an issue.
## Resources

Here is a list of resources to help you gain more knowledge on static code analysis.

- [PEP 8 Style Guide for Python Code](https://peps.python.org/pep-0008/ "PEP 8 Style Guide for Python Code")
- [What Is Static Code Analysis?](https://in.mathworks.com/discovery/static-code-analysis.html "What Is Static Code Analysis? MATLAB and Simulink - MATLAB & Simulink (mathworks.com)")
- [Static Program Analysis](https://en.wikipedia.org/wiki/Static_program_analysis "Static program analysis - Wikipedia")
- [How Static Code Analysis Works](https://www.perforce.com/blog/qac/how-static-code-analysis-works "How static code analysis works")

# Test Cases

## Example Test Case

```Python
"""
Module to be tested
"""

def square(number):
    """
    This function returns the square of a given number
    """
    return number ** 2

def double(number):
    """
    This function returns twice the value of a given number
    """
    return number * 2

def add(a,b):
    """
    This function returns the sum of the given numbers
    """
    return a + b
```

```Python
"""
Example unittest test cases
"""

import unittest
from mymodule import square, double, add

class TestSquare(unittest.TestCase):
    def test1(self):
        self.assertEqual(square(2), 4) # test when 2 is given as input the output is 4.
        self.assertEqual(square(3.0), 9.0)  # test when 3.0 is given as input the output is 9.0.
        self.assertNotEqual(square(-3), -9)  # test when -3 is given as input the output is not -9.

class TestDouble(unittest.TestCase):
    def test1(self):
        self.assertEqual(double(2), 4) # test when 2 is given as input the output is 4.
        self.assertEqual(double(-3.1), -6.2) # test when -3.1 is given as input the output is -6.2.
        self.assertEqual(double(0), 0) # test when 0 is given as input the output is 0.

class TestAdd(unittest.TestCase):
    def test1(self):
        self.assertEqual(add(2, 4), 6)
        self.assertEqual(add(0, 0), 0)
        self.assertEqual(add(2.3, 3.6), 5.9)
        self.assertEqual(add('hello', 'world'), 'helloworld')
        self.assertEqual(add(2.3000, 4.300), 6.6)
        self.assertNotEqual(add(-2, -2), 0)

unittest.main()
```

# Summary - Week 1

- The application development lifecycle has seven phases, including:    
	- Requirement Gathering: You collect user, business, and technical requirements for the app
	- Analysis: You analyze the requirements
	- Design: You design the complete solution
	- Code and test: You build and test the different components of the app
	- User and system test: Users test the app for usability, and you perform system integration testing and performance testing
	- Production: The application is available to all end users
	- Maintenance: You upgrade or fix any user or system issues
- All web apps are APIs, but not all APIs are web apps. Both share data between apps, but not all APIs require networks like web apps do.
- The PEP8 guidelines for code readability include the following:
	- Four spaces for indentation
	- Blank lines to separate functions and classes 
	- Spaces around operators and after commas
- The PEP8 coding conventions for consistency and manageability include:
	- Add larger blocks of code inside functions
	- Name functions and files using lowercase with underscores
	- Name classes using CamelCase
	- Name constants in capital letters with underscores separating words
- To ensure that your code adheres to the predefined style and standard without executing the code, you can use the Static code analysis method.
- Unit testing is a method to validate if code units are operating as designed. You must test every unit before integration with the final codebase.
- To create a package:
	- Create a folder with the package name
	- Create an empty __init__.py file
	- Create the required modules
	- In the __init__.py file, add code to reference the modules needed in the package
- You can verify the package via the bash terminal in a Python shell.

# Cheatsheet: Python Coding Practices and Packaging Concepts

|Package/Method|Description|Code Example|
|---|---|---|
|**Packaging**|To create a package, the folder structure is as follows:<br><br>1. **Project folder** → **Package name** → ****init**.py**, **module_1.py**, **module_2.py**, and so on.<br><br>3. In the ****init**.py** file, add code to reference the modules in the package.|**module1.py**<br><br>def function_1(arg):<br><br>    return <operation output><br><br>****init**.py**:<br><br>from . import function_1|
|**Python Style Guide**|- Four spaces for indentation<br><br>- Use blank lines to separate functions and classes<br><br>- Use spaces around operators and after commas<br><br>- Add larger blocks of code inside functions<br><br>- Name functions and files using lowercase with underscores<br><br>- Name classes using CamelCase<br><br>- Name constants in capital letters with underscores separating words|def function_1(a, b):<br><br>     if a > b:<br><br>         c = c + 5<br><br>    else:<br><br>        c = c - 3<br><br>    return c<br><br>…<br><br>c = function_1(a, b)<br><br>**Constant Definition example**<br><br>MAX_FILE_UPLOAD_SIZE|
|**Static Code Analysis**|Use Static code analysis method to evaluate your code against a predefined style and standard without executing the code.<br><br>For example, use Pylint to perform static code analysis.|**Shell code:**<br><br>pylint code.py|
|**Unit Testing**|Unit testing is a method to validate if units of code are operating as designed.<br><br>During code development, each unit is tested. The unit is tested in a continuous integration/continuous delivery test server environment.<br><br>You can use different test functions to build unit tests and review the unit test output to determine if the test passed or failed.|import unittest<br><br>from mypackage.mymodule import my_function<br><br>class TestMyFunction(unittest.TestCase):<br><br>    def test_my_function(self):<br><br>        result = my_function(<args>)<br><br>        self.asserEqual(result, <response>)<br><br>unittest.main()|
# Decorators in Flask
### What are decorators

Decorators help in annotating the methods and tell what a particular method is meant for. These are different from comments. This is used by the interpreter while running the code.
## Method decorators

Let’s say we have a python code where we want all the output to be in JSON format. It doesn’t make sense to include code for these in each of the methods as it makes the lines of code redundant. In such cases, we can handle this with a decorator.

1. `def jsonify_decorator(function):`
2.     `def modifyOutput():`
3.         `return {"output":function()}`
4.     `return modifyOutput`

6. `@jsonify_decorator`
7. `def hello():`
8.     `return 'hello world'`

10. `@jsonify_decorator`
11. `def add():`
12.     `num1 = input("Enter a number - ")`
13.     `num2 = input("Enter another number - ")`
14.     `return int(num1)+int(num2)`

16. `print(hello())`
17. `print(add())`

The method decorator is also referred to as the wrapper, which wraps the output of the function, that it decorates. In the above code sample, `jsonify-decorator` is the decorator method. We have added this decorator to `hello()` and `add()`. The output of these method calls will now be wrapped and decorated with the jsonify_decorator.

The output of invoking the above python code will be:

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0222EN-SkillsNetwork/labs/module_1/images/decorated_output.png)

As you can see the method call has been wrapped with the decorator. The coder has a free will to choose the name of the decorator. Here the name chosen is `jsonify_decorator`.

## Route Decorators

You may have observed when you visit any domain you have the root and then have other end-points you can access. See the examples below.

`https://mydomain.com/`

`https://mydomain.com/about`

`https://mydomain.com/register`

We will look at creating these endpoints when we will create a web application using the flask module in the labs that will follow.

But to define these endpoints in Python we use what we call **Route Decorators**.

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0222EN-SkillsNetwork/labs/module_1/images/route_decorator.png)

**@app.route(“/“)** is a Python decorator that Flask provides to assign URLs in our app to functions easily. You can easily tell that the decorator is telling our @app that whenever a user visits our application’s domain, in our case, execute the `home()` function.

We can handle multiple routes with a single function by just stacking additional route decorators above the method which should be invoked when the route is called. The following is a valid example of serving the same “Hello World!” message for 3 separate routes:

1. `@app.route("/")`
2. `@app.route("/home")`
3. `@app.route("/index")`
4. `def home():`
5.     `return "Hello World!"`

The route decorators also take `method` as a second parameter, which can be set to the type of HTTP methods, the route will support. We will learn about this in the later sections.

The route decorator can also be more specific. For example, to get the details of a user whose userId is U0001, you may go to  
`http://mydomain.com/userdetails/U0001`. It doesn’t make sense to define a different route for each user you may be dealing with. In such cases, we define the route like this.

1. `@app.route("/userdetails/<userid>")`
2. `def getUserDetails(userid):`
3.     `return "User Details for  "+userid`

# CRUD Operations using Additional Features in Flask
## Overview

**Create, Read, Update**, and **Delete** (CRUD) are basic functions that any application with a database must perform. To effectively implement the CRUD operations, you will need to manage different HTTP methods, such as `GET` and `POST` requests. A `GET` request is generally used to retrieve or read data and is often used to display a form. A `POST` request is commonly used to send data to create or update data. An example of a POST request is form submission.

This reading aims to introduce you to additional features of Flask, focusing on the CRUD functions. You will also learn how these functions are interrelated and how they utilize the different HTML files, dynamic routes, and various HTTP methods.
## Accessing Form Data with flask.request.form

You can use `flask.request.form` to access form data that a user has submitted via a `POST` request. For instance, this feature can be used if you have a login form with username and password fields.

In your HTML file, you might have a form like this:

1. `<form method="POST" action="/login">`
2.     `<input type="text" name="username">`
3.     `<input type="password" name="password">`
4.     `<input type="submit" value="Submit">`
5. `</form>`

The Python code to access the username and password will be as follows:

1. `from flask import request`

3. `@app.route('/login', methods=['POST'])`
4. `def login():`
5.     `username = request.form['username']`
6.     `password = request.form['password']`
7.     `# process login here`
## Redirecting to a URL with flask.redirect

Flask provides a function called flask.redirect to guide users to a different webpages (or endpoints). The flask.redirect function can be useful in several scenarios. For example, you can use the flask.redirect function to redirect a user to a **login** page when they try to access a restricted **admin** page.

Python code:

1. `from flask import redirect`

3. `@app.route('/admin')`
4. `def admin():`
5.     `return redirect('/login')`
## Generating Dynamic URLs with flask.url_for

The `flask.url_for` function dynamically generates URLs for a given endpoint. Dynamically generating URLs can be particularly useful when the URL for a route is altered. The `flask.url_for` function automatically updates the URL throughout your templates or code, minimizing manual work. For example, consider the scenario where a user is trying to access the **admin** page and must be redirected to the **login** page. In this scenario, `url_for('login')` will retrieve the URL for the **login** page from the existing routes.

Python code:

1. `from flask import url_for`

3. `@app.route('/admin')`
4. `def admin():`
5.     `return redirect(url_for('login'))`

7. `@app.route('/login')`
8. `def login():`
9.     `return "<Login Page>"`
## Handling different HTTP request types

Flask allows you to define routes to manage different types of HTTP requests. You can define the route with both the access methods, GET and POST, and in the function description, define the use cases for both methods.

Python code:

1. `@app.route('/data', methods=['GET', 'POST'])`
2. `def data():`
3.     `if request.method == 'POST':`
4.         `# process POST request`
5.     `if request.method == 'GET':`
6.         `# process GET request`

In the HTML file, you will add a form that allows both `GET` and `POST` requests:

1. `<!-- For POST -->`
2. `<form method="POST" action="/data">`
3.     `<!-- Your input fields here -->`
4.     `<input type="submit" value="Submit">`
5. `</form>`

7. `<!-- For GET -->`
8. `<a href="/data">Fetch data</a>`

In the last example, the `/data` route accepts both `GET` and `POST` requests. The type of the request can be checked using `flask.request.method`.
## CRUD operations

The CRUD operations represent the four basic functions that you require to interact with any persistent storage, such as a database. In web development, the CRUD operations often correspond to HTTP methods.
### **Create operation**

Creating data often involves presenting a form to the user to gather the information that you want to store in the database as a new record. In Flask, this data is accessed using `flask.request.form`.

HTML form for creating data:

1. `<form method="POST" action="/create">`
2.     `<input type="text" name="name">`
3.     `<input type="submit" value="Create">`
4. `</form>`

Python code:

1. `@app.route('/create', methods=['GET', 'POST'])`
2. `def create():`
3.     `if request.method == 'POST':`
4.         `# Access form data`
5.         `name = request.form['name']`
6.         `# Create a new record with the name`
7.         `record = create_new_record(name)  # Assuming you have this function defined`
8.         `# Redirect user to the new record`
9.         `return redirect(url_for('read', id=record.id))`
10.     `# Render the form for GET request`
11.     `return render_template('create.html')`
### Read operation

Reading data involves accessing the data and presenting it to the user. To access specific entries, the request needs to go with specific IDs. Therefore, you will need to pass the ID as an argument to the function. The following example shows that the ID can be accessed from the route.

Python code:

1. `@app.route('/read/<int:id>', methods=['GET'])`
2. `def read(id):`
3.     `# Get the record by id`
4.     `record = get_record(id)  # Assuming you have this function defined`
5.     `# Render a template with the record`
6.     `return render_template('read.html', record=record)`
### Update operation

Updating data requires the process of accessing specific entries, like the **Read** operation, and involves giving new data to the concerned parameter, like the **Create** operation. Therefore, the route should access the ID and contain both access methods.

Sample HTML form for updating data:

1. `<form method="POST" action="/update/{{record.id}}">`
2.     `<input type="text" name="name" value="{{record.name}}">`
3.     `<input type="submit" value="Update">`
4. `</form>`

Python code:

1. `@app.route('/update/<int:id>', methods=['GET', 'POST'])`
2. `def update(id):`
3.     `if request.method == 'POST':`
4.         `# Access form data`
5.         `name = request.form['name']`
6.         `# Update the record with the new name`
7.         `update_record(id, name)  # Assuming you have this function defined`
8.         `# Redirect user to the updated record`
9.         `return redirect(url_for('read', id=id))`

11.     `# Render the form for GET request with current data`
12.     `record = get_record(id)  # Assuming you have this function defined`
13.     `return render_template('update.html', record=record)`
### Delete operation

Deleting data involves removing a record based on its ID. The Delete operation will typically require the ID to be passed, as reported by the HTML page, in the form of an argument to the function.

Sample HTML form for deleting data:

1. `<form method="POST" action="/delete/{{record.id}}">`
2.     `<input type="submit" value="Delete">`
3. `</form>`

Python code:

1. `@app.route('/delete/<int:id>', methods=['POST'])`
2. `def delete(id):`
3.     `# Delete the record`
4.     `delete_record(id)  # Assuming you have this function defined`
5.     `# Redirect user to the homepage`
6.     `return redirect(url_for('home'))`

## Example Flask App

### Hello World Server

```Python
# server.py - Text Output
from flask import Flask
app = Flask(__name__)

@app.route("/")
def index():
    return "hello world"
```

Use the following command to run the server from the terminal:

`flask --app server --debug run`

![Run Flask server in debug mode](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-CD0320EN-SkillsNetwork/images/m1-flask-run-app.png "Run Flask server in debug mode")

You should now be able to use the CURL command on `localhost:5000/`.

> Note that the terminal is already running the server, you can use the `Split Terminal` button to split the terminal and run the following command in the second tab.

`curl -X GET -i -w '\n' localhost:5000`

The `-X` argument specifies the `GET` command, and the `-i` argument displays the header from the response.

![Curl command](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-CD0320EN-SkillsNetwork/images/m1-flask-curl-get.png "Curl command")

You should see `Hello World` returned as the output of the CURL command.

> Note the return status of `HTTP 200 OK` and the `Content-type` of `text/html`.

```Python
# server.py - JSON Output
from flask import Flask
app = Flask(__name__)

@app.route("/")
def index():
    return "hello world"
```

You should now be able to use the CURL command with `localhost:5000/`.

> Note that the terminal is running the server, you can use the `Split Terminal` button to split the terminal and run the following command in the second tab.

`curl -X GET -i -w '\n' localhost:5000`

![Flask returns JSON response](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-CD0320EN-SkillsNetwork/images/m1-flask-json-run.png "Flask returns JSON response")

You should see `{"message": "Hello World"}` JSON returned as the output of the CURL command.

> Note the return status of `HTTP 200 OK` and the `Content-type` of `application/json` this time.

# Summary: Web App Deployment using Flask

- Python libraries are like toolkits. Each library has specific tools to simplify and expedite certain programming tasks. Frameworks are predefined structures for application development. Framework enables you to build the complete application, while libraries aid with specific functionality.
- Flask is a microframework that ships with minimal dependencies. To build websites, Flask has features like debugging servers, routing, templates, and error handling. Flask can be installed as a python package. Django is a full-stack framework compared to Flask. You can create a server by instantiating the Flask class.
- Flask provides a Request and a Response object for each client call. You can get additional information from the Flask Request, like headers. You can parse the Request Object to get query parameters, body, and other arguments. You can even set status on Response objects before sending a response back to the client.
- You can use dynamic routes to create RESTful endpoints.
- There are multiple classes of HTTP status codes showing success, user error, or server error. Flask implicitly returns a success code of 200 with the response. You can also provide status codes explicitly. Flask also provides application-level error handlers.
- Flask is a microframework for creating web applications and supports CRUD.
	- Install the Flask package using pip.
	- To create a web application using Flask:
	- Import Flask
	- Instantiate Flask
	- Run the app
- You can render both static and dynamic templates with Flask.

# Cheatsheet: Web App Deployment using Flask
|Package/Method|Description|Code Example|
|---|---|---|
|**@app decorator**|An app decorator is a Python tool that allows programmers to modify the behavior or function of a class. App decorators take paths as an argument.|from flask import Flask<br><br>app = Flask(__name__)|
|**@app.route decorator**|A decorator in Flask used to map URLs to specific functions in a Flask application.|@app.route('/')<br><br>def hello_world():<br><br>    return "<b>My first Flask application in action!</b>"|
|**200 OK status**|Flask servers automatically return a 200 OK status when you return from the @app.route method. 200 is also returned by default when you use the jsonify() method to respond to a request. A successful response with a status code of 200 will be sent back when the given code executes.|@app.route('/')<br><br>def hello_world():<br><br>     return ("<b>My first Flask application in action!", 200)|
|**Error 404**|**400** indicates an invalid request. This status could imply the parameters are missing or improper or the request is invalid in another way.<br><br>**401** indicates the credentials are missing or invalid.<br><br>**403** implies that the client credentials are not sufficient to fulfill the request. If the server is unable to find the resource, it returns a 404 status.<br><br>**405** indicates that the requested operation is not supported.|@app.route('/')<br><br>def search_response():<br><br>    query = request.args.get("q")<br><br>    if not query:<br><br>         return {"error_message": "Input parameter missing"}, 422<br><br>    # fetch the resource from the database<br><br>    resource = fetch_from_database(query)<br><br>    if resource:<br><br>        return {"message": resource}<br><br>    else:<br><br>        return {"error_message": "Resource not found"}, 404|
|**Error 500**|500 is used when there is an error on the server.|@ app.errorhandler(500)<br><br>def server_error(error):<br><br>    return {"message": "Something went wrong on the server"}, 500|