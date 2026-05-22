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

Developed By: SHAMSHEER BANU M 


Register No:  21225040400
server.py:

```import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept()
while True: 
    ClientMessage=c.recv(1024).decode() 
    print("Student: ",ClientMessage) 
    msg=input("Faculty: ") 
    c.send(msg.encode())
```


client.py:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True:
    msg=input("Student: ")
    s.send(msg.encode())
    print("Faculty: ",s.recv(1024).decode())
```
## OUPUT

SERVER
<img width="827" height="282" alt="image" src="https://github.com/user-attachments/assets/9e7ab1d5-d3f6-41e4-83f9-b59a9a6dfd0e" />



CLIENT
<img width="837" height="290" alt="image" src="https://github.com/user-attachments/assets/827b2b75-fced-4fe3-96bb-211ba551cb4c" />
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
