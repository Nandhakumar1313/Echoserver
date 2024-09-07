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
```
Name:Nandhakumar G R
Register no:212222100029
```
### Client.py
```python
import socket

s=socket.socket()
s.connect(('localhost',65124))
while(1):
   msg=input("Client>")
   s.send(msg.encode())
   print("Server>"+s.recv(1024).decode())
```
### Server.py
```python
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
### Client.py
![Nandhakumar G R](https://github.com/user-attachments/assets/5f301f81-83c9-4c0f-b775-ec225dd2ea2f)

### Server.py
![Nandhakumar G R](https://github.com/user-attachments/assets/7029b6e1-8ccf-444a-bbb0-493884c7d8da)

## RESULT:
The program is executed successfully
