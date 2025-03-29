# 2a_Stop_and_Wait_Protocol
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


CLIENT:

import socket  <br>
s=socket.socket() <br>
s.listen(5) <br>
c,addr=s.accept() <br>
while True:<br>
<t> i=input("Enter a data: ") <br>
<t> c.send(i.encode()) <br>
   ack=c.recv(1024).decode()<br>
   if ack:<br>
      print(ack)<br>
      continue<br>
   else:<br>
      c.close()<br>
      break<br>
    
SERVER:

import socket<br>
s=socket.socket()<br>
s.connect(('localhost',8000))<br>
while True:<br>
   print(s.recv(1024).decode())<br>
   s.send("Acknowledgement Recived".encode())<br>
 
## OUTPUT
![Screenshot (354)](https://github.com/user-attachments/assets/f90180ec-e279-45d4-991b-eab484bb1ab6)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
