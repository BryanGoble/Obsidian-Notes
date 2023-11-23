Assessment Name: Process Text Files with Python Dictionaries and Upload to Running Web Service

This assessment is module 2 of the Google IT Automation Capstone. I was tasked with writing out python code that would process several txt files in `/data/feedback/`, read each line and assign each to a key in a dictionary. Finally, I had to use a POST request to upload the dictionary to the assigned `<external-ip>/feedback`. I was able to successfully parse the data and view the uploaded file contents in the web ui.

```Python
#!/usr/bin/env python3
import os, requests

def feedback_dict(feedback_file):
    with open('/data/feedback/' + feedback_file, mode='r', encoding='UTF-8') as file:
        lines = file.readlines()
        feedback = { 'title': lines[0], 'name': lines[1], 'date': lines[2], 'feedback': lines[3] }

    post_feedback(feedback)

def post_feedback(feedback):
    response = requests.post("http://34.83.174.188/feedback/", data=feedback)
    if response.ok:
        print('Uploaded feedback!')
    else:
        print(f'upload feedback error: {response.status_code}')

for i in os.listdir('/data/feedback/'):
    feedback_dict(i)
```