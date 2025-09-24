# 3b.CREATION FOR CHAT USING TCP SOCKETS

Name : Syed Abu Hanifa. L

REG No : 212224040346

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
### server
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

<img width="1920" height="1008" alt="Screenshot 2025-09-17 102545" src="https://github.com/user-attachments/assets/e97a2602-c3cc-468c-a281-b396f4e7c52b" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
