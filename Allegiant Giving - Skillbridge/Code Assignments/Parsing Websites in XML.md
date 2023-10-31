For the last assignment of my Week 3 course, we briefly touched on using the XML Element Tree. I had to find all of the comments in a specific url, count how many there were, then once again sum the total number value found in each comment.

```Python
import urllib.request, urllib.parse, urllib.error
import xml.etree.ElementTree as ET
import ssl

# Ignore SSL certificate errors
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE

url = input('Enter location: ')
print('Retrieving', url)

html = urllib.request.urlopen(url, context=ctx).read().decode()
print('Retrieved', len(html), 'characters')

tree = ET.fromstring(html)

counts = tree.findall('.//comment')
print('Count:', len(counts))

tot = 0
for i in range(len(counts)):
    tot += int(counts[i].find('count').text)
print('Sum:', tot)
```