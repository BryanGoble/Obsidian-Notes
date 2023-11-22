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

