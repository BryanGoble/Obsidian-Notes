# Courses
1. [Google IT Automation with Python (Course 5)](https://www.coursera.org/learn/configuration-management-cloud/)
## Introduction to Automation at Scale

Puppet is an automation tool used for managing and configuring computer systems, particularly in IT infrastructure and server environments. It helps organizations automate the deployment, configuration, and maintenance of software and settings on a large scale. Here's a simple explanation of how Puppet works and how it can be used with Python:

1. **Configuration Management:** Puppet allows you to define the desired state of your servers and infrastructure using code, which is called "Puppet manifests." These manifests specify how each system should be configured, including which software to install, what settings to apply, and how services should run.

2. **Agent-Based:** Puppet operates on a client-server model. It has a central server (Puppet Master) and agent nodes (Puppet Agents) installed on the managed systems. The Puppet Master stores and distributes the configuration manifests, while Puppet Agents apply those configurations on their respective systems.

3. **Declarative Language:** Puppet uses a declarative language, which means you describe what you want the system to look like rather than specifying the steps to get there. This makes it easier to manage complex configurations.

4. **Idempotent:** Puppet is idempotent, meaning it ensures that the desired system state is reached, even if you apply the configuration multiple times. If a configuration is already in the desired state, Puppet won't make unnecessary changes.

5. **Fact:** hash that stores information about the details of a particular system.

Now, regarding Python:

- Puppet can execute various actions on managed systems, including running scripts and commands. This is where Python comes into play. You can use Python scripts within your Puppet manifests to perform specific tasks or custom configurations on your servers.

- For example, you can write a Puppet manifest that installs Python on all your servers and then uses Python scripts to configure specific applications or services. Python is a versatile scripting language that can be integrated into Puppet to extend its capabilities.

- Puppet also has a built-in module for managing Python packages and virtual environments, making it easier to manage Python-related configurations.

In summary, Puppet is an automation tool that helps manage and configure computer systems, and it can work seamlessly with Python by allowing you to use Python scripts within your configuration manifests to customize and automate tasks on your servers. This combination provides flexibility and scalability in managing your infrastructure.

- Module - Used to organize the configuration management tools.
- Node Definitions - Used to apply different rule catalogs to various types of machines
- Certificate Authority (CA) - Either queues a certificate request for manual validation, or uses pre-shared data to verify before sending the certificate to the agent. (Validates the identity of each machine)
### Puppet Commands
- `puppet apply -v <manifest_file_here.pp>` - Applies the puppet manifest for future execution.
- `=>` - Used to define all rules
- `puppet parser validate` - Checks the syntax of the manifest.
## Cloud Computing
- Containers - applications that are packaged together with their configuration and dependencies.

- Infrastructure as a Service (IaaS) - provides users with the bare minimum needed to utilize a server's computational resources, such as a virtual machine. It is the user's responsibility to configure everything else.
- Software as a Service (SaaS) - A cloud provider delivers an entire application or program to the customer
- Platform as a Service (PaaS) - A cloud provider offers a preconfigured platform to the customer
### Scaling
- Automatic scaling - The service offered by the Cloud provider will use metrics to automatically increase or decrease the capacity of the system.
- Manual scaling - Changes are controlled by humans instead of software.

## Capstone Project
### Recap from previous courses
- Web Application - application that you interact with over HTTP. 
- Web Services - web application that also have an API.
- API Call - Used to send a message to a web service
- API Endpoint - The part of the program that listens on the network for API calls
- Data Serialization - process of taking an in-memory data structure, like a Python object, and turning it into something that can be stored on disk or transmitted across a network.

Example serialization with JSON
```Python
import json

with open('people.json', 'w') as people_json:
    json.dump(people, people_json, indent=2)
    
# This code uses the **json.dump()** function to serialize the **people** object into a JSON file.
[
  {
	"name": "Sabrina Green",
	"username": "sgreen",
	"phone": {
	  "office": "802-867-5309",
	  "cell": "802-867-5310"
	},
	"department": "IT Infrastructure",
	"role": "Systems Administrator"
  },
  {
	"name": "Eli Jones",
	"username": "ejones",
	"phone": {
	  "office": "684-348-1127"
	},
	"department": "IT Infrastructure",
	"role": "IT Specialist"
  },
]
```

Example serialization with YAML (Yet Another Markup Language)
```Python
import yaml

with open('people.yaml', 'w') as people_yaml:
    yaml.safe_dump(people, people_yaml)

# In this example, we’re using the **yaml.safe_dump()** method to serialize our object into YAML:
- department: IT Infrastructure
  name: Sabrina Green
  phone:
    cell: 802-867-5310
    office: 802-867-5309
  role: Systems Administrator
  username: sgreen
- department: IT Infrastructure
  name: Eli Jones
  phone:
    office: 684-348-1127
  role: IT Specialist
  username: ejones
```

#### JSON
- JSON is **human-readable**, which means it's encoded using printable characters, and formatted in a way that a human can understand.
- Supports a few elements of different data types:
	- **Strings** - enclosed in quotes
	- **Numbers**
	- **Objects** - key-value pair structures like Python dictionaries
		- These key-value pairs can also contain another object as a value.
	- **Arrays** - Equivalent to Python lists.
		- Can contain strings, numbers, objects, or other arrays.
- JSON elements are always **comma-delimited**.
- **.dump()** method is used to serialize JSON data to a file.
- **.dumps()** method will return the string of data rather than dumping to a file.
- **.load()** method does the inverse and will deserialize JSON from a file into basic Python objects.
- **.loads()** method also does the inverse and will deserialize JSON from a string into a basic Python object.

#### Requests library
Example basic request for a webpage
```Python
import requests

response = requests.get('https://www.google.com')

# To view what is stored in the response
print(response.text[:300]) # Grabs the first 300 characters

# <!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="de"><head><meta content="text/html; charset=UTF-8" http-equiv="Content-Type"><meta content="/images/branding/googleg/1x/googleg_standard_color_128dp.png" itemprop="image"><title>Google</title><script nonce="dZfbIAn803LDGXS9

# Instead, we can look at the raw response data
response = requests.get('https://www.google.com', stream=True)

# Output the first 100 characters of raw data
print(response.raw.read()[:100])

# b'\x1f\x8b\x08\x00\x00\x00\x00\x00\x02\xff\xc5Z\xdbz\x9b\xc8\x96\xbe\xcfS`\xf2\xb5-\xc6X\x02$t\xc28\xe3v\xdc\xdd\xee\xce\xa9\xb7\xdd;\xe9\x9d\xce\xf6W@\t\x88\x11`@>D\xd6\x9b\xce\xe5<\xc3\\\xcd\xc5\xfc\xab8\x08\xc9Nz\x1f.&\x8e1U\xb5j\xd5:\xfc\xb5jU\x15\x87;^\xe2\x16\xf7)\x97\x82b\x1e\x1d\x1d\xd2S'

# To check if a request was good or not
response.ok
# True or False

# You can also get the status code
response.status_code
# 200, 400, 404, etc.

# Always good practice to check status codes before proceeding
response = requests.get(url)
if not response.ok:
    raise Exception("GET failed with status code {}".format(response.status_code))
    
# The code block above isn't necessarily needed either as we can use the .raise_for_status() method
response = requests.get(url)
response.raise_for_status()
```

- GET method - By sending a GET request, you're asking the server to GET the resource for you.
	- A GET request can have parameters.
		- A question mark will be used to separate the URL from the parameters.
```Python
p = {"search": "grey kitten", "max_results": 15}
response = requests.get("https://example.com/path/to/api", params=p)
response.request.url

# 'https://example.com/path/to/api?search=grey+kitten&max_results=15'
```

- POST method - used to respond to forms or submit data to web sites.
	- Instead of setting the params attribute, which gets turned into a query string and appended to the URL, we use the **data** attribute, which contains the data that will be sent as part of the POST request.
```Python
p = {"description": "white kitten", "name": "Snowball", "age_months": 6}
response = requests.post("https://example.com/path/to/api", data=p)
response.request.url

# 'https://example.com/path/to/api'

# The data parameters have been tied into the body of the HTTP message rather than the URL, to see these we can use the **body** attribute
response.request.body

# 'description=white+kitten&name=Snowball&age_months=6'

# So, if we need to send and receive data from a web service, we can turn our data into dictionaries and then pass that as the **data** attribute of a POST request.

# Today, it's super common to send and receive data specifically in JSON format, so the Requests module can do the conversion directly for us, using the **json** parameter.

response = requests.post("https://example.com/path/to/api", json=p)
response.request.url

# 'https://example.com/path/to/api'

response.request.body

# b'{"description": "white kitten", "name": "Snowball", "age_months": 6}'
```

#### Email Message Module
- Email Header Fields (Always key-value pairs)
	- From
	- To
	- Subject

```Python
# Create an empty email message
>>> from email.message import EmailMessage
>>> message = EmailMessage()
>>> print(message) # Outputs the string representation of the object

# To see more than the above, we can start assigning values to message dictionary
>>> sender = 'me@example.com'
>>> recipient = 'you@example.com'

# Assign them to the From and To fields of the message
>>> message['From'] = sender
>>> message['To'] = recipient
>>> print(message)
# From: me@example.com
# To: you@example.com

# Subject assignment
>>> message['Subject'] = 'Greetings from {} to {}!'.format(sender, recipient)
>>> print(message)
# From: me@example.com
# To: you@example.com
# Subject: Greetings from me@example.com to you@example.com!

# Add the message body
>>> body = """Hey there!
...
... I'm learning to send emails using Python!"""
>>> message.set_content(body)
>>> print(message)
# From: me@example.com
# To: you@example.com
# Subject: Greetings from me@example.com to you@example.com!
# MIME-Version: 1.0
# Content-Type: text/plain; charset="utf-8"
# Content-Transfer-Encoding: 7bit

# Hey there!

# I'm learning to send email using Python!
```

- Adding Attachments
	- Whenever an attachment is sent in an email, the attachment is encoded into the email as some form of text. This is called the Multipurpose Internet Mail Extensions (MIME) standard or mime type.
```Python
# If you know the mime type, then you can use that directly otherwise you can use the mimetypes module to make a good guess.
>>> import os.path
>>> attachment_path = "/tmp/example.png"
>>> attachment_filename = os.path.basename(attachment_path)
>>> import mimetypes
>>> mime_type, _ = mimetypes.guess_type(attachment_path)
>>> print(mime_type)
# image/png

# Above, the mime_type string contains the MIME type and subtype, separated by a slash. The EmailMessage type needs a MIME type and subtype as separate strings, so we can split it up.
>>> mime_type, mime_subtype = mime_type.split('/', 1)
>>> print(mime_type)
# image
>>> print(mime_subtype)
# png

# Now we can add it to our email message
>>> with open(attachment_path, 'rb') as ap:
...     message.add_attachment(ap.read(),
...                            maintype=mime_type,
...                            subtype=mime_subtype,
...                            filename=os.path.basename(attachment_path))
... 
>>> print(message)
# Content-Type: multipart/mixed; boundary="===============5350123048127315795=="

# --===============5350123048127315795==
# Content-Type: text/plain; charset="utf-8"
# Content-Transfer-Encoding: 7bit

# Hey there!

# I'm learning to send email using Python!

# --===============5350123048127315795==
# Content-Type: image/png
# Content-Transfer-Encoding: base64
# Content-Disposition: attachment; filename="example.png"
# MIME-Version: 1.0

# iVBORw0KGgoAAAANSUhEUgAAASIAAABSCAYAAADw69nDAAAACXBIWXMAAAsTAAALEwEAmpwYAAAg
# AElEQVR4nO2dd3wUZf7HP8/M9k2nKIJA4BCUNJKgNJWIBUUgEggCiSgeVhA8jzv05Gc5z4KHiqin
# eBZIIBDKIXggKIeCRCAhjQAqx4UiCARSt83uzDy/PzazTDZbwy4BnHde+9qZydNn97Pf5/uUIZRS
# (...We deleted a bunch of lines here...)
# wgAAAABJRU5ErkJggg==

# --===============5350123048127315795==--
```

- Sending the Email through an SMTP Server
```Python
# Import the smptlib module
>>> import smtplib

# Create an smptlib.SMTP object and try to connect to the local machine
>>> mail_server = smtplib.SMTP('localhost')
# Traceback (most recent call last):
#   File "<stdin>", line 1, in <module>
#   (...We deleted a bunch of lines here...)
# ConnectionRefusedError: [Errno 61] Connection refused

# This means that we don't have an SMTP server up and running on our local host, but instead we can connect to the SMTP server for our personal emails.
# When setting this up, you'll most likely need to setup some sort of secure connection using SSL/TLS. To do this, the smtplib module has two classes, the standard .SMTP() class and the .SMTP_SSL() class which creates a connection over SSL/TLS.
>>> mail_server = smtplib.SMTP_SSL('smtp.example.com')

# If you care to see the behind the scenes messages that this module is sending then you can use the debug class
>>> mail_server.set_debuglevel(1)

# We've made the connection to the SMTP server above, but now we need to authenticate using username/password. For this, we'll use the getpass module to prevent leaving our password out in the open for prying eyes.
>>> import getpass
>>> mail_pass = getpass.getpass('Password? ')
# Password?
>>> '<Enter-password-here>'

# Be careful with the mail_pass variable, because it is still storing your password as a string
>>> print(mail_pass)
# It'sASecr3t!

# Now we can authenticate to the email server using the SMTP object's login method
>>> mail_server.login(sender, mail_pass)
# (235, b'2.7.0 Accepted')

# If the login attempt succeeds, the login method will return a tuple of the SMTP status code and a message explaining the reason for the status. If the login attempt fails, the module will raise a SMTPAuthenticationError exception.

# To send the email now
>>> mail_server.send_message(message)
# {}

# Done! The returned dictionary is only populated with recipients that weren't able to receive our message.

# Now that we're done. Close the connection to the server
>>> mail_server.quit()
```
#### Generating PDFs from Python
- There are a few tools available, but we're focusing on ReportLab since it has a ton of features for creating PDF documents.
```Python
# In this example, we have a dictionary of our fruit collection that we want to transcribe into a PDF.
fruit = {
  "elderberries": 1,
  "figs": 1,
  "apples": 2,
  "durians": 3,
  "bananas": 5,
  "cherries": 8,
  "grapes": 13
}

# We'll use the SimpleDocTemplate class to build our PDF
>>> from reportlab.platypus import SimpleDocTemplate
>>> report = SimpleDocTemplate("/tmp/report.pdf")

# The report object just generated a PDF using the filename '/tmp/report.pdf'. Now we can add some content to it.
# ReportLab uses something called Flowables. These are essentially chunks of a document that reportlab can arrange to make a complete report.
>>> from reportlab.platypus import Paragraph, Spacer, Table, Image

# Each of those classes build a part of the document, but we also need to tell reportlab how to style the document.
>>> from reportlab.lib.styles import getSampleStyleSheet
>>> styles = getSampleStyleSheet()

# Add a document title
>>> report_title = Paragraph("A Complete Inventory of My Fruit", styles["h1"])

# Now we'll add a table based on our fruit data
>>> table_data = []
>>> for k, v in fruit.items():
...   table_data.append([k, v])
...
>>> print(table_data)
# [['elderberries', 1], ['figs', 1], ['apples', 2], ['durians', 3], ['bananas', 5], ['cherries', 8], ['grapes', 13]]

# Now we have a list of lists that we can add to our report
>>> report_table = Table(data=table_data)
>>> report.build([report_title, report_table])

# The table is there, but it's pretty ugly so we can modify our code to style it.
>>> from reportlab.lib import colors
>>> table_style = [('GRID', (0,0), (-1,-1), 1, colors.black)]
>>> report_table = Table(data=table_data, style=table_style, hAlign="LEFT")
>>> report.build([report_title, report_table])

# Add graphics to the PDF. We'll add a pie chart
>>> from reportlab.graphics.shapes import Drawing
>>> from reportlab.graphics.charts.piecharts import Pie
>>> report_pie = Pie(width=3*inch, height=3*inch)

# For the Pie chart, we need two lists. One for the data and another for the labels.
>>> report_pie.data = []
>>> report_pie.labels = []
>>> for fruit_name in sorted(fruit):
...   report_pie.data.append(fruit[fruit_name])
...   report_pie.labels.append(fruit_name)
...
>>> print(report_pie.data)
# [2, 5, 8, 3, 1, 1, 13]
>>> print(report_pie.labels)
# ['apples', 'bananas', 'cherries', 'durians', 'elderberries', 'figs', 'grapes']

# The pie object isn't Flowable, but it can be placed inside of a Flowable Drawing.
>>> report_chart = Drawing()
>>> report_chart.add(report_pie)

# Add the Drawing to the report
report.build([report_title, report_table, report_chart])
```