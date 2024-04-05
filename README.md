# 2a_Stop_and_Wait_Protocol
Name: T. Gayathri
Register No: 212223100007
Department: CSE(CS)
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
## CLIENT
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
## SERVER 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received ".encode())
```
## OUTPUT
## CLIENT
![Screenshot 2024-04-05 104523](https://github.com/NaliniG007/2a_Stop_and_Wait_Protocol/assets/149037327/7651724f-c584-4bac-9c1a-ee0db897b11a)
## SERVER 
![Screenshot 2024-04-05 104538](https://github.com/NaliniG007/2a_Stop_and_Wait_Protocol/assets/149037327/3f07ba9d-3633-4402-a662-29ecc8b84dc0)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
