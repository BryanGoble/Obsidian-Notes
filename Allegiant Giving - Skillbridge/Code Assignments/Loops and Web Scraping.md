For this assignment, I used BeautifulSoup once again to parse through a sites' `<a>` tags. The user provided the url, the position of the selected `<a>` tag to be followed and the count, or number of times to repeat this process.

```Python
import urllib.request, urllib.parse, urllib.error
from bs4 import BeautifulSoup
import ssl

# Ignore SSL certificate errors
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE

url = input('Enter URL: ')
count = int(input('Enter count: '))
pos = int(input('Enter position: '))

# Retrieve all of the anchor tags
for i in range(count):
    html = urllib.request.urlopen(url, context=ctx).read()
    soup = BeautifulSoup(html, 'html.parser')

    tags = soup('a')

    url = tags[pos - 1].get('href', None)
    print(url)
```