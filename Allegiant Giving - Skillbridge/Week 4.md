# Courses
1. [Programming For Everybody (Using Python to Access Web Data)](https://www.coursera.org/learn/python-network-data)


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