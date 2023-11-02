# Courses
1. [Programming For Everybody (Using Python to Access Web Data)](https://www.coursera.org/learn/python-network-data)
2. [Something](https://www.coursera.org/learn/python-databases)

## 12.3 - Unicode Characters and Strings
In simple terms, Unicode characters and strings in Python 3 allow you to work with a wide range of characters and symbols from various languages and writing systems, making it easier to handle text in a global context.

1. **Unicode Characters**:
   - Unicode is a standard that assigns a unique number (called a code point) to every character, symbol, and emoji from almost all the world's writing systems.
   - Unicode characters include letters from different languages (e.g., English, Chinese, Arabic), special symbols (e.g., ©, €), and emojis (e.g., 😊).
   - Unicode ensures that you can represent and work with text in multiple languages and character sets within a single program.

2. **Strings**:
   - In Python 3, a string is a sequence of Unicode characters. It can be made up of letters, digits, symbols, and spaces.
   - Strings are enclosed in single (' '), double (" "), or triple (''' ''' or """ """) quotes.
   - Examples of strings:
     - `"Hello, world!"` (English text)
     - `"你好，世界！"` (Chinese text)
     - `"مرحبا بالعالم!"` (Arabic text)
     - `"😊"` (Emoji)
   
So, in Python 3, you can work with text that includes characters and symbols from different languages and cultures using Unicode. This makes it a powerful tool for handling multilingual and diverse text data in your programs.

In simple terms, `.encode()` and `.decode()` are methods in Python 3 that allow you to convert between strings and bytes when working with networking or file I/O.

1. **.encode()**:
   - When you have a text string (a sequence of characters), you can use `.encode()` to convert it into a sequence of bytes.
   - This is particularly useful when you want to send text data over a network or save it in a binary file.
   - You specify an encoding method (e.g., UTF-8) when using `.encode()`, which determines how the characters in the string are converted to bytes.
   - Example:

     ```python
     text_string = "Hello, World!"
     byte_data = text_string.encode("utf-8")
     ```

2. **.decode()**:
   - Conversely, when you receive a sequence of bytes (e.g., from a network connection or reading a binary file) and want to interpret it as a text string, you use `.decode()`.
   - You need to know the encoding that was used when the bytes were created in order to correctly decode them.
   - Example:

     ```python
     byte_data = b'Hello, World!'
     text_string = byte_data.decode("utf-8")
     ```

In networking, these methods help ensure that data is properly converted between text and binary representations when it's transmitted over the network, allowing different systems to communicate using a common encoding scheme, such as UTF-8, which supports a wide range of characters from various languages.

### Using urllib
In simple terms, Python 3's `urllib` is a built-in library that allows you to work with URLs (Uniform Resource Locators) in your Python programs. It provides a set of modules for fetching data from the internet, making HTTP requests, and handling URLs. Here's a basic explanation:

1. **urllib.request**: This module within `urllib` lets you open and read URLs. You can use it to send HTTP requests to web servers and retrieve the content from web pages or other online resources.

   ```python
   import urllib.request

   # Open a URL and read its content
   response = urllib.request.urlopen('https://www.example.com')
   html_content = response.read()
   print(html_content)
   ```

2. **urllib.parse**: This module helps you parse URLs into their components, like scheme (http, https), hostname, path, query parameters, etc., and also construct URLs from their individual components.

   ```python
   import urllib.parse

   # Parse a URL
   url = 'https://www.example.com/somepage?param=value'
   parsed_url = urllib.parse.urlparse(url)
   print(parsed_url.scheme)
   print(parsed_url.netloc)
   print(parsed_url.path)
   print(parsed_url.query)
   ```

3. **urllib.error**: This module contains exceptions that are raised when there are errors during URL operations, such as HTTP errors or network issues.

   ```python
   import urllib.error

   try:
       response = urllib.request.urlopen('https://www.nonexistentpage.com')
   except urllib.error.HTTPError as e:
       print("HTTP error:", e)
   except urllib.error.URLError as e:
       print("URL error:", e)
   ```

In simple terms, `urllib` is a handy tool for fetching web content, parsing URLs, and handling errors related to internet communication in Python. It's often used in web scraping, web API access, and other network-related tasks. However, some developers prefer using more feature-rich libraries like `requests` for HTTP requests due to its simpler and more user-friendly interface.

### BeautifulSoup
In simple terms, web scraping with BeautifulSoup in Python 3 is a way to extract information from websites. Here's an explanation:

1. **Getting Web Content**: Python can make requests to a website, just like a web browser. With web scraping, you use Python to fetch the web page's HTML code, which contains the information you want to extract.

2. **Parsing HTML**: BeautifulSoup is a Python library that helps you parse (read and understand) the HTML code of a web page. It organizes the HTML structure into a more accessible format that you can work with.

3. **Finding Data**: After parsing the HTML, you can use BeautifulSoup's functions to locate specific pieces of information on the web page, such as text, links, or images.

4. **Extracting Data**: Once you've identified the data you want, you can extract it from the HTML. You can then use this data in your Python program for various purposes, like analysis, storage, or display.

Here's a simple example:

```python
import requests
from bs4 import BeautifulSoup

# Make a request to a website
response = requests.get("https://example.com")

# Parse the HTML content of the webpage
soup = BeautifulSoup(response.text, "html.parser")

# Find and extract specific data
title = soup.title.string  # Extract the title of the webpage
paragraphs = soup.find_all("p")  # Find all paragraphs on the page

# Print the extracted data
print("Title:", title)
for p in paragraphs:
    print("Paragraph:", p.text)
```

In this code:

- We use the `requests` library to make an HTTP request to a website and get its HTML content.
- Then, we use BeautifulSoup to parse the HTML and navigate it to find specific elements like the webpage's title and paragraphs.
- Finally, we extract and print the desired data.

Web scraping can be used for various purposes, such as data analysis, content aggregation, or monitoring websites for changes. However, it's essential to respect websites' terms of service and legal regulations when scraping their content.

- *Code snippet to ignore SSL certificate errors
```Python
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE

# Set .urlopen(url, context=ctx) to refer back to the empty SSL
```

## 13.1 - XML
In simple terms, XML (Extensible Markup Language) is a way to structure and store data in a text-based format. It uses tags to define elements and their relationships, making it easy to represent structured data. Here's a basic explanation of parsing XML in Python 3:

**XML**: 
- XML is like a language for organizing information.
- It uses tags enclosed in angle brackets (`<tag>`) to define elements.
- Elements can have attributes (additional information) inside the tags.
- Elements can be nested within each other to create a hierarchy.

**Parsing XML in Python**:
- Parsing XML means reading an XML document and extracting information from it.
- Python provides libraries like `xml.etree.ElementTree` and `xml.dom.minidom` for XML parsing.
- The process involves opening and reading an XML file or string, then navigating through the elements to access the data you need.

Here's a simple example using `xml.etree.ElementTree`:

```python
import xml.etree.ElementTree as ET

# Sample XML data
xml_data = '''
<data>
    <item>
        <name>Apple</name>
        <price>1.00</price>
    </item>
    <item>
        <name>Banana</name>
        <price>0.50</price>
    </item>
</data>
'''

# Parse the XML data
root = ET.fromstring(xml_data)

# Access and print information
for item in root.findall('item'):
    name = item.find('name').text
    price = float(item.find('price').text)
    print(f"Item: {name}, Price: ${price:.2f}")
```

In this example:
- We create a sample XML data string.
- We use `ET.fromstring()` to parse it and get the root element.
- We then use `find()` and `.text` to access the data inside the XML elements and print it.

This is a basic example of how you can parse XML data in Python to extract and work with structured information. You can adapt this approach for more complex XML documents and real-world scenarios.

### XSD
In simple terms, XSD stands for XML Schema Definition. It's a way to define the structure and constraints of XML data. XSD serves as a blueprint or a set of rules that describe what valid XML data should look like. It's often used to ensure that XML documents conform to a specific structure and data format.

Here's a simple example to illustrate XSD and data parsing in Python 3:

Suppose you have an XSD schema that defines the structure of a simple XML document representing information about books:

```xml
<!-- books.xsd -->
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="book">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="title" type="xs:string"/>
        <xs:element name="author" type="xs:string"/>
        <xs:element name="published" type="xs:date"/>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```

In this XSD schema:

- We define an XML element called "book."
- Inside "book," we specify that it should contain "title," "author," and "published" elements in that order.
- We also specify the data types for each element (e.g., "title" and "author" should be strings, and "published" should be a date).

Now, let's say you have an XML document (`books.xml`) that follows this schema:

```xml
<!-- books.xml -->
<book>
  <title>Python Programming</title>
  <author>John Doe</author>
  <published>2023-10-30</published>
</book>
```

To parse this XML data in Python 3 and validate it against the XSD schema, you can use the `lxml` library, which provides support for XML parsing and validation:

```python
from lxml import etree

# Load the XSD schema
xsd_schema = etree.XMLSchema(file="books.xsd")

# Load and parse the XML document
xml_doc = etree.parse("books.xml")

# Validate the XML document against the XSD schema
if xsd_schema.validate(xml_doc):
    print("XML document is valid according to the XSD schema.")
else:
    print("XML document is not valid according to the XSD schema.")
```

In this Python script:

- We load the XSD schema using `etree.XMLSchema`.
- We load and parse the XML document using `etree.parse`.
- We validate the XML document against the XSD schema using `xsd_schema.validate`.

If the XML document conforms to the XSD schema, it will be considered valid, and the script will print "XML document is valid according to the XSD schema." Otherwise, it will print "XML document is not valid according to the XSD schema."

## 13.5 - JavaScript Object Notation (JSON)
In simple terms, JSON (JavaScript Object Notation) is a lightweight and easy-to-read data interchange format. It's used to store and exchange data between different programs or systems, especially when they're written in different programming languages. JSON data is represented as text, making it human-readable and machine-readable.

Here's a simple explanation of JSON and an example in Python 3:

**JSON Basics:**
- JSON data consists of key-value pairs enclosed in curly braces `{}`.
- Keys are strings enclosed in double quotes.
- Values can be strings, numbers, objects (nested key-value pairs), arrays (ordered lists of values), `true`, `false`, or `null`.

**Example:**
Suppose you want to represent information about a person using JSON:

```json
{
  "name": "John Doe",
  "age": 30,
  "is_student": false,
  "hobbies": ["reading", "hiking"],
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA"
  }
}
```

In this JSON example:

- `"name"` is a key with a string value.
- `"age"` is a key with a numeric value.
- `"is_student"` is a key with a Boolean (true or false) value.
- `"hobbies"` is a key with an array of strings as its value.
- `"address"` is a key with an object (nested key-value pairs) as its value.

In Python, you can work with JSON data using the built-in `json` module. Here's an example of how to parse (read) JSON data in Python:

```python
import json

# JSON data as a string (you can also read it from a file)
json_data = '''
{
  "name": "John Doe",
  "age": 30,
  "is_student": false,
  "hobbies": ["reading", "hiking"],
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA"
  }
}
'''

# Parse the JSON data into a Python dictionary
data = json.loads(json_data)

# Accessing values in the parsed JSON
print("Name:", data["name"])
print("Age:", data["age"])
print("Hobbies:", ", ".join(data["hobbies"]))
print("City:", data["address"]["city"])
```

In this example, we first import the `json` module, then use `json.loads()` to parse the JSON data into a Python dictionary. Once parsed, you can access and manipulate the data using regular Python syntax.

## 13.6 - Service-Oriented Architecture
In simple terms, Service-Oriented Architecture (SOA) in Python 3 refers to a way of designing and building software systems where different parts of the system are organized as independent services. Each service performs a specific function and communicates with other services through well-defined interfaces or APIs (Application Programming Interfaces).

Here's how SOA applies to Python 3:

1. **Services**: In Python 3, services are typically implemented as separate Python programs or modules. Each service focuses on a specific task or capability within the larger software system. For example, you might have one service for handling user authentication, another for processing payments, and another for generating reports.

2. **Intercommunication**: Services in SOA communicate with each other using standard protocols and data formats. Python 3 provides libraries and frameworks for building APIs and handling communication between services. Common methods for communication include HTTP, JSON, and RESTful APIs.

3. **Independence**: Services are designed to be independent, meaning they can be developed, deployed, and scaled separately from each other. This makes it easier to update or replace one service without affecting the entire system.

4. **Flexibility and Reusability**: SOA promotes flexibility and reusability of code. Python's modular and object-oriented programming features are well-suited for building reusable service components. You can create libraries or modules that provide specific functionality and reuse them across multiple services.

5. **Scalability**: Python 3 and SOA allow you to scale different services independently based on their specific demands. For example, if one service experiences high traffic, you can scale it up without affecting the performance of other services.

6. **Maintenance**: When using Python 3 in SOA, maintenance becomes more manageable. You can update or fix issues in one service without disrupting the operation of the entire system. This modular approach simplifies debugging and maintenance efforts.

In summary, in Python 3, Service-Oriented Architecture involves designing and implementing software systems as a collection of independent services that communicate with each other through well-defined interfaces. This approach offers flexibility, scalability, and maintainability, making it easier to build and manage complex applications.

## 13.7 - Application Programming Interfaces (API)

**1. What is an API?**
   - An API is like a set of rules and tools that allows different software programs to communicate and work together. It defines how one piece of software can request and exchange data with another.

**2. Using APIs in Python 3:**
   - Python 3 can interact with various APIs to access data or services provided by other software systems, websites, or services.

**3. Making API Requests:**
   - In Python 3, you can use libraries like `requests` to make HTTP requests to web APIs. These requests can be used to retrieve data from a remote server.

   Example:
   ```python
   import requests

   response = requests.get("https://api.example.com/data")
   data = response.json()  # Convert the response to Python data
   ```

   - In this example, we use the `requests` library to send a GET request to an API, and we receive a response containing data, which we can then parse and use.

**4. Parsing API Responses:**
   - API responses often come in JSON format. Python 3 can easily parse JSON data using the built-in `json` module.

   Example:
   ```python
   import json

   json_data = '{"name": "John", "age": 30}'
   data = json.loads(json_data)
   print(data["name"])  # Accessing data from the JSON response
   ```

   - In this code, we parse a JSON response into a Python dictionary so that we can work with the data more easily.

**5. Using API Data:**
   - Once you have the data from an API, you can use it for various purposes, such as displaying it on a website, analyzing it, or integrating it into your own application.

**6. Authentication and API Keys:**
   - Some APIs require authentication to access data. In Python 3, you can include API keys or tokens in your API requests to authenticate yourself.

**7. API Documentation:**
   - When using an API in Python 3, it's essential to refer to the API's documentation, which provides information on how to make requests, what data is available, and any special requirements or limitations.

In summary, Python 3 can interact with APIs to retrieve and work with data from various sources, allowing you to access and utilize external services and information in your Python applications.

### REST vs SOAP
In simple terms, **REST (Representational State Transfer)** and **SOAP (Simple Object Access Protocol)** are two different approaches for creating APIs (Application Programming Interfaces) that allow different software systems to communicate with each other. Here are the key differences between REST and SOAP APIs:

1. **Protocol**:
   - **REST**: It is an architectural style and does not rely on a specific protocol. However, it is commonly implemented over HTTP.
   - **SOAP**: It is a protocol with a specific set of rules and uses XML for message formatting. It can work over various lower-level protocols like HTTP, SMTP, and more.

2. **Message Format**:
   - **REST**: Uses a variety of message formats, such as JSON, XML, HTML, and plain text, but JSON is the most common choice.
   - **SOAP**: Uses XML exclusively for message formatting.

3. **Ease of Use**:
   - **REST**: Generally considered simpler and easier to work with, especially for web services. It relies on standard HTTP methods like GET, POST, PUT, DELETE, which are familiar to web developers.
   - **SOAP**: Typically more complex due to its strict XML structure and additional standards. It often requires specialized libraries or tools to work with.

4. **Statelessness**:
   - **REST**: Emphasizes statelessness, meaning each request from a client to a server must contain all the information needed to understand and process the request. Sessions can be managed on the client side.
   - **SOAP**: Supports both stateful and stateless operations. It has built-in features for maintaining session state.

5. **Flexibility**:
   - **REST**: Provides flexibility in data formats and is often used in scenarios where simplicity and efficiency are essential, such as mobile applications and web services.
   - **SOAP**: Offers strict rules and standards, which can be advantageous in some enterprise-level scenarios where reliability and security are critical.

6. **Error Handling**:
   - **REST**: Uses standard HTTP status codes for indicating errors, making it easy to understand error responses.
   - **SOAP**: Has a more elaborate error handling mechanism using its own fault codes and structures.

7. **Caching**:
   - **REST**: Supports caching, which can improve performance by storing and reusing responses.
   - **SOAP**: Typically does not have built-in caching mechanisms.

8. **Security**:
   - **REST**: Offers security through HTTPS and can implement various authentication mechanisms, but it requires additional considerations for security.
   - **SOAP**: Provides built-in security features like WS-Security, which can be useful in enterprise-level applications.

In summary, REST is often preferred for its simplicity, speed, and widespread use in web and mobile applications. SOAP, on the other hand, is commonly used in enterprise-level systems where strict standards and reliability are crucial, even though it comes with additional complexity. The choice between REST and SOAP depends on the specific needs and constraints of a given project or system.

## 14.1 - Object Oriented Definitions and Terminology
Object-Oriented Programming (OOP) is a programming paradigm that organizes code into objects, which are instances of classes. It's a way of structuring and designing code to model real-world entities, making it more modular, reusable, and easier to maintain.

In simple terms, here's what OOP entails:

1. **Objects**: Objects are instances of classes, and they represent real-world entities or concepts. These objects have attributes (properties) and methods (functions) that define their behavior.

2. **Classes**: Classes serve as blueprints for creating objects. They define the structure (attributes) and behavior (methods) that objects of that class should have.

3. **Encapsulation**: Encapsulation is the concept of bundling data (attributes) and the methods (functions) that operate on that data into a single unit (an object). It allows you to control access to the internal state of an object.

4. **Inheritance**: Inheritance allows you to create new classes (child or subclass) based on existing classes (parent or superclass). The child class inherits attributes and methods from the parent class and can also have its own unique attributes and methods.

5. **Polymorphism**: Polymorphism enables different objects to respond to the same method or function call in a way that's appropriate for their specific class. It allows you to write more generic and flexible code.

In Python 3, OOP is implemented using classes and objects. Here's a simple example to illustrate how OOP is used in Python:

```python
# Define a class
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    def bark(self):
        print(f"{self.name} says Woof!")

# Create objects (instances) of the class
dog1 = Dog("Buddy", "Golden Retriever")
dog2 = Dog("Charlie", "Poodle")

# Access attributes and call methods of objects
print(f"{dog1.name} is a {dog1.breed}.")
dog2.bark()
```

In this example:

- We define a class called `Dog`, which has attributes (`name` and `breed`) and a method (`bark`).
- We create two instances of the `Dog` class (`dog1` and `dog2`) with different attribute values.
- We access attributes (`name` and `breed`) and call the `bark` method on the objects.

This demonstrates the fundamental concepts of OOP in Python: classes, objects, attributes, and methods, allowing you to model and manipulate objects with ease, making your code more organized and reusable.

## 15.1 - Relational Databases
In simple terms, a relational database in Python 3 is a structured and organized way to store and manage large amounts of data, where the data is organized into tables with rows and columns. It's called "relational" because it maintains relationships between different pieces of data.

Here are some key points to understand:

1. **Tables**: Data is stored in tables, which are similar to spreadsheets. Each table has rows and columns. Rows represent individual records or data entries, and columns represent different attributes or properties of those records.

2. **SQL**: Relational databases are typically managed using a language called SQL (Structured Query Language). You use SQL commands to create, retrieve, update, and delete data from the database. Python provides libraries and modules like SQLAlchemy and sqlite3 to interact with relational databases using SQL.

3. **Data Integrity**: Relational databases enforce data integrity through constraints. This means you can define rules that ensure the data in the database remains accurate and consistent. For example, you can specify that a certain column should only contain unique values or that a column cannot be left empty (a constraint called "NOT NULL").

4. **Relationships**: You can establish relationships between tables. For example, you can have one table that stores information about customers and another table that stores their orders. By using keys (like customer IDs), you can link records in these tables to represent that each order is associated with a specific customer.

5. **ACID Properties**: Relational databases follow the ACID (Atomicity, Consistency, Isolation, Durability) properties to ensure data reliability and transactional consistency. This means that database operations are guaranteed to be reliable and maintain the integrity of the data.

Here's a simple example using Python's built-in SQLite database:

```python
import sqlite3

# Connect to a SQLite database (or create one if it doesn't exist)
connection = sqlite3.connect('mydatabase.db')

# Create a cursor to interact with the database
cursor = connection.cursor()

# Create a table to store data
cursor.execute('''CREATE TABLE IF NOT EXISTS students (
                    id INTEGER PRIMARY KEY,
                    name TEXT,
                    age INTEGER
                )''')

# Insert data into the table
cursor.execute("INSERT INTO students (name, age) VALUES (?, ?)", ("Alice", 25))

# Retrieve data from the table
cursor.execute("SELECT * FROM students")
data = cursor.fetchall()
for row in data:
    print("ID:", row[0])
    print("Name:", row[1])
    print("Age:", row[2])

# Commit changes and close the connection
connection.commit()
connection.close()
```

In this example, we create a SQLite database, define a table called "students," insert data, retrieve data, and follow the ACID properties to maintain data integrity. This demonstrates the basic concepts of working with a relational database in Python 3.

### Database Administrator (dba)
A person responsible for the design, implementation, maintenance, and repair of an organization's database. The role includes the development and design of database strategies, monitoring and improving database performance and capacity, and planning for future expansion requirements. They may also plan, coordinate, and implement security measures to safeguard the database.

### Database Model
A database model or database schema is the structure or format of a database, described in a formal language supported by the database management system, in other words, a "database model" is the application of a data model  when used in conjunction with a database management system.

### Common Database Systems
Three major Database Management Systems in wide use:
- Oracle - Large, commercial, enterprise-scale, very very tweakable
- MySQL - Simpler but very fast and scalable - commercial open source
- SqlServer - Very nice - from Microsoft (also Access)
Many other smaller projects, free and open source
- HSQL, SQLite, Postgress, ...

