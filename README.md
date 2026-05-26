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
```
#chat_server.py
import socket
# Create socket
server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
# Bind host and port
host = '127.0.0.1'
port = 5000
server_socket.bind((host, port))
# Listen for client
server_socket.listen(1)
print("Waiting for client connection...")
# Accept connection
client_socket, addr = server_socket.accept()
print("Connected to:", addr)
while True:
 # Receive message from client
 client_message = client_socket.recv(1024).decode()
 print("Client:", client_message)
 # Exit condition
 if client_message.lower() == "bye":
   break
 # Send message to client
 message = input("Server: ")
 client_socket.send(message.encode())
 if message.lower() == "bye":
   break
# Close connection
client_socket.close()
server_socket.close()
```
```
#chat_server.py
import socket
# Create socket
server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
# Bind host and port
host = '127.0.0.1'
port = 5000
server_socket.bind((host, port))
# Listen for client
server_socket.listen(1)
print("Waiting for client connection...")
# Accept connection
client_socket, addr = server_socket.accept()
print("Connected to:", addr)
while True:
 # Receive message from client
 client_message = client_socket.recv(1024).decode()
 print("Client:", client_message)
 # Exit condition
 if client_message.lower() == "bye":
   break
 # Send message to client
 message = input("Server: ")
 client_socket.send(message.encode())
 if message.lower() == "bye":
   break
# Close connection
client_socket.close()
server_socket.close()
```
Developed by : vignesh vj 

Reg no : **212225230299


```
## OUPUT
```
<img width="1600" height="900" alt="WhatsApp Image 2026-05-26 at 2 10 01 PM" src="https://github.com/user-attachments/assets/9002fea3-1680-4334-8bd5-fcaff67385d1" />
```

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
