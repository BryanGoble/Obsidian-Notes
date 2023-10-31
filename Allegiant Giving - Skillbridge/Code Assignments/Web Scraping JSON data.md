Similar to last week, we continued working through web scraping fundamentals and covered JSON today. I was tasked with counting the number of comments and again summing the values found for all of them.

```Python
import urllib.request, urllib.parse, urllib.error
import json

url = input('Enter location: ')
uh = urllib.request.urlopen(url)
data = uh.read().decode()
print('Retrieving', url)
print('Retrieved', len(data), 'characters')

comments = json.loads(data)

count = 0
tot = 0
for item in comments['comments']:
    count += 1
    tot += item['count']

print('Count:', count)
print('Sum:', tot)
```