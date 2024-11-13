# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

**NAME : THARUN SRIDHAR**

**REGISTER NO : 212223230230**

# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.

## PROGRAM

**Server**
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

**Client**
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```


## OUTPUT

**SERVER**
![WhatsApp Image 2024-09-24 at 08 22 51_bf342a5b](https://github.com/user-attachments/assets/cd6def60-bb5f-4802-8d78-adfc6611c0c9)

**CLIENT**
![WhatsApp Image 2024-09-24 at 08 23 28_9a90f8e3](https://github.com/user-attachments/assets/dda8797d-0e52-4438-9ea0-94c5a6d6a2d3)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
