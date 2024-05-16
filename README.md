# 2a_Stop_and_Wait_Protocol
ANANTTHA VARTHAN.S
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
```
CLIENT
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
SERVER

s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
```
## OUTPUT
![Screenshot 2024-05-16 140058](https://github.com/anandsandy4623/2a_Stop_and_Wait_Protocol/assets/135193077/359857df-0ecb-4fd9-a2c2-f5a7ad0cf4a7)

![Screenshot 2024-05-16 140107](https://github.com/anandsandy4623/2a_Stop_and_Wait_Protocol/assets/135193077/7c24d6f3-3219-40a5-976e-af8b5a45228e)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
