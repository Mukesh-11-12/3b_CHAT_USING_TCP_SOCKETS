# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```

## OUPUT

CLIENT:

<img width="1042" height="469" alt="image" src="https://github.com/user-attachments/assets/d08bc678-caa4-4c93-80f5-165b3ae5842a" />

SERVER:

<img width="1036" height="480" alt="image" src="https://github.com/user-attachments/assets/f7062ad9-468c-4fc9-afe6-cb530ca54bb9" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
