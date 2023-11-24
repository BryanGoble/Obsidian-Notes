```Python
#!/usr/bin/env python3
import requests, os

files = os.listdir('supplier-data/descriptions/')

def upload_fruits(file):
    file = file

    def read_files():
        with open(('supplier-data/descriptions/' + file), 'r') as fruit_file:
            line = fruit_file.readlines()
            fruit = { 'name': line[0], 'weight': (int(line[1][:3])), 'description': line[2], 'image_name': (file[:3] + '.jpeg') }
            return fruit

    fruit = read_files()
    print(fruit)
    r = requests.post('http://34.29.191.160/fruits/', data=fruit)
    if r.ok:
        print('Uploaded fruit!')
    else:
        print(f'Error Uploading Fruit: {r.status_code}')

for file in files:
    upload_fruits(file)
```