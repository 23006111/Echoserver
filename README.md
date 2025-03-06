## NAME:RAMYA P
## REG NO:212223230168

# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
## client.py
~~~
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'RAMYA P, 6-3-25, 212223230168')
    print(f'Received: {s.recv(1024)!r}')
~~~
## server.py
~~~
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
~~~


## OUTPUT:
![image](https://github.com/user-attachments/assets/02d865f4-3960-49c0-86c5-68435145c59a)


## RESULT:
The program is executed successfully.
