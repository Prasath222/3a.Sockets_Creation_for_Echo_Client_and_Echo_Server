# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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
## CLIENT

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

## SERVER

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
## OUPUT

## CLIENT
<img width="1540" height="625" alt="Screenshot 2025-10-08 084207" src="https://github.com/user-attachments/assets/eab5ec43-1200-44f0-a258-b2475b3da363" />

## SERVER
<img width="1333" height="675" alt="Screenshot 2025-10-08 084246" src="https://github.com/user-attachments/assets/d786d5eb-c65a-43f8-9d18-2eb07d1558d3" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
