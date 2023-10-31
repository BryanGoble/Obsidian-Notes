This assignment focused on being able to read a file and use regex to parse through the data. The goal was to read the document, picking out all numbers and totaling their value.

```Python
import re

data = input('Enter location of file: ') # C:\actual.txt

with open(data, 'r') as file:
    content = file.read()

print( sum([int(i) for i in re.findall(r'[0-9]+', content)]) )
```
