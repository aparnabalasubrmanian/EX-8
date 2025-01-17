# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

AIM :
   To write a python program for creating Echo Client and Echo Server using TCP
 Sockets Links.

ALGORITHM :
```
   1. Start the program.
   2. Get the frame size from the user
   3. To create the frame based on the user request.
   4. To send frames to server from the client side.
   5. If your frames reach the server, it will send ACK signal to client otherwise it will
      send NACKsignal to client.
   6. Stop the program
```
PROGRAM :
```
CLIENT:
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
   
SERVER:
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   c.send(ClientMessage.encode())
```

OUTPUT :
CLIENT:
![c8](https://github.com/aparnabalasubrmanian/EX-8/assets/123351172/cd13cf87-66d8-47bc-bb23-27249a77dea1)

SERVER:
![s8](https://github.com/aparnabalasubrmanian/EX-8/assets/123351172/3191634d-8235-4959-98d9-8b095cf54082)

RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links
was successfully created and executed.
