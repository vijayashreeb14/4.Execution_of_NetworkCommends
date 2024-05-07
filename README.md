# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>
program:ping command
client:

import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())      
server:
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode()) 

Tracer:
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans) 


Output:
Tracer:

![Screenshot 2024-05-07 193219](https://github.com/vijayashreeb14/4.Execution_of_NetworkCommends/assets/161238151/e495f43d-bf7f-4d08-8536-179dbb5de9a3)

client:

![image](https://github.com/vijayashreeb14/4.Execution_of_NetworkCommends/assets/161238151/7952a040-9c65-45a9-94e0-b3a76ef5bf16)

Server:

![Screenshot 2024-05-07 193343](https://github.com/vijayashreeb14/4.Execution_of_NetworkCommends/assets/161238151/a4b3ff6a-6a9a-44a0-9940-7a2f0e310641)

Result:
Thus Execution of Network commands Performed.
