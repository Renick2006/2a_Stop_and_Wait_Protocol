# 2a_Stop_and_Wait_Protocol
# NAME: RENICK FABIAN RAJESH
# REG NO: 212224230227

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
## Client:
```
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
```
## Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   print(s.recv(1024).decode())
   s.send("Acknowledgement Recived".encode())

```
   



## OUTPUT

![Screenshot 2025-03-19 103344](https://github.com/user-attachments/assets/51f63590-c8d4-4aa3-9715-7f6d280b4a58)
![Screenshot 2025-03-19 103401](https://github.com/user-attachments/assets/9f3c1329-b394-43ff-97ae-db40b4080583)
![Screenshot 2025-03-18 111911](https://github.com/user-attachments/assets/cb7fcd5f-26d1-46e9-92e7-f1eb0361e7b1)
![Screenshot 2025-03-18 112047](https://github.com/user-attachments/assets/c6d35d98-3968-49a2-a419-9fe34709a604)



## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
