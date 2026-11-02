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
###SERVER
```python
import socket

server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server.bind(("127.0.0.1", 5000))
server.listen(1)

print("Server waiting for connection...")

conn, addr = server.accept()
print("Client connected:", addr)

message = conn.recv(1024).decode()
print("Message from client:", message)

response = "Hello Client, message received successfully!"
conn.send(response.encode())

conn.close()
server.close()
```
### CLIENT
```python
import socket

client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client.connect(("127.0.0.1", 5000))

message = "Hello Server, this is Client!"
client.send(message.encode())

response = client.recv(1024).decode()
print("Message from server:", response)

client.close()
```


## OUPUT
<img width="465" height="73" alt="image" src="https://github.com/user-attachments/assets/bb260a3f-11f8-49b6-8c1e-f0e665e8852b" />

<img width="567" height="36" alt="image" src="https://github.com/user-attachments/assets/f673da5a-84d5-4453-9652-b4de19ecdebf" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
