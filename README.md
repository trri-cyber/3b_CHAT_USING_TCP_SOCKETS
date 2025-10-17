# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server:
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
## OUTPUT:
## client:
![image](https://github.com/Rajaraman77/3b_CHAT_USING_TCP_SOCKETS/assets/150319383/b11b7db7-2daa-4452-af95-3f19c7615a7d)
## server:
![image](https://github.com/Rajaraman77/3b_CHAT_USING_TCP_SOCKETS/assets/150319383/ce4fe94e-f652-42e6-89fa-cf6179cfa69c)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
