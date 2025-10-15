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
server.py
~~~
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5)
print("Server started and listening on port 8000...")  
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
~~~
client.py
~~~
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
~~~
## OUPUT
server.py

<img width="568" height="193" alt="Screenshot 2025-10-15 182018" src="https://github.com/user-attachments/assets/3c39d692-5eb1-4f8f-aba5-7f55b17a98d9" />

client.py

<img width="576" height="189" alt="Screenshot 2025-10-15 182033" src="https://github.com/user-attachments/assets/b2e7cc2b-6d6f-4a25-99f9-24f1b4be9159" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
