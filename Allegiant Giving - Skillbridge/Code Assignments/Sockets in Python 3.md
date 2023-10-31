In this assignment, we focused on constructing code that opened a socket connection to the example site on port 80 then printed the contents of the file 'intro-short.txt'.

```Python
import socket

mysock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
mysock.connect( ('data.pr4e.org', 80) ) # Host, Port

mysock.send('GET http://data.pr4e.org/intro-short.txt HTTP/1.0\r\n\r\n'.encode())

while True:
    data = mysock.recv(512) # Receive upto 512 bytes of data
    if (len(data) < 1):
        break
    print(data.decode())

mysock.close()
```