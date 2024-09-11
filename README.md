# Echoserver
Echo server and client using python socket

# AIM:
To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:
Design of echo server and client using python socket

### Step 2:
Implementation using Python code

### Step 3:
Testing the server and client 

## PROGRAM:
### Echo client.py
```
import socket
s=socket.socket()
s.connect(('localhost',65124))
while(1):
  msg=input("Client>")
  s.send(msg.encode())
  print("Server>"+s.recv(1024).decode())
```

### Echo server.py
```
import socket
s=socket.socket()
s.bind(('localhost',65124))
s.listen(5)
c,addr=s.accept()
while(1):
   msg=c.recv(1024).decode()
   print(msg)
   c.send(msg.encode())
```

## OUTPUT:
![eth ex1](https://github.com/user-attachments/assets/5c84ad17-2c44-4bf0-8848-f03ed633d06b)

## RESULT:
The program is executed successfully
