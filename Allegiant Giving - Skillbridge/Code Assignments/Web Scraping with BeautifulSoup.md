For this assignment, I was tasked with parsing through a sites' `<span>` tags containing an assortment of numbers.

```Python
from urllib.request import urlopen
from bs4 import BeautifulSoup
import ssl

# Ignore SSL certificate errors
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE

url = input('Enter - ')
html = urlopen(url, context=ctx).read()
soup = BeautifulSoup(html, "html.parser")

# Retrieve all of the span tags and number values then sum
comments = soup('span')
print(sum(int(num.contents[0]) for num in comments))
```