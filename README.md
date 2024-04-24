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
client:
~~~
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
~~~
server:
~~~
serverimport socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
~~~
Trancecode:
~~~
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
~~~
## Output
client

![Screenshot 2024-04-24 150935](https://github.com/vijayashreeb14/4.Execution_of_NetworkCommends/assets/161238151/fcf8a247-c8e1-4725-bf6b-1256901a509c)

server

![Screenshot 2024-04-24 150957](https://github.com/vijayashreeb14/4.Execution_of_NetworkCommends/assets/161238151/ef7a10dc-103e-449a-b6e7-d4afc46cc831)

Transroute command

![Screenshot 2024-04-24 151334](https://github.com/vijayashreeb14/4.Execution_of_NetworkCommends/assets/161238151/bc9d8e11-6147-4982-ba16-818c615d36bf)

## Result
Thus Execution of Network commands Performed 
