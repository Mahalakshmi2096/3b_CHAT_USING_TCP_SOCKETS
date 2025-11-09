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
Client:
```
import socket 
s=socket.socket()
s.connect(('localhost',8000)) 
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
Server:
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
Client:

<img width="957" height="561" alt="image" src="https://github.com/user-attachments/assets/2a9c5ce0-7ce5-49b2-aaba-51a30d2a15a4" />

Server:

<img width="957" height="566" alt="image" src="https://github.com/user-attachments/assets/58dbbfba-6065-4fcc-a650-2f449d9ee061" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
