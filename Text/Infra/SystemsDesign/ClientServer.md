## Client-Server Model 


**[back to index](https://github.com/mlfa03/MLOPs/blob/main/README.md)**

### Client
* A machine or process that requests data or service from a server, processes data from a server. 
* A single machine or piece of software can be both client and a server at the same time. For instance, a single machine could act as a server 
for end users and as a client for a database.
* Initially, the client does not know how to 'talk to' the server. It makes then, in the background, a DNS query to find out what the IP address
is. Only then can it really speak to the server. 
* **DNS query** is a special request that goes to a predetermined set of servers and 'asks for' the IP address of the server. 

### Server
* Machines that are waiting for receive requests from other machines (clients). Once they get these requests, they can send responses to the clients. 
* A machine or process that provides data or service for a client, usually by listening for incoming network calls. 
* A single machine or piece of software can be both client and a server at the same time. For instance, a single machine could act as a server 
for end users and as a client for a database.

### Client-server model 
* The paradigm by which modern systems are designed, which consists of clients requesting data or service from servers and servers providing
data or service to clients. 

### IP Address 
* Unique identifier for a machine
* An address given to each machine connected to the public internet. 
* IPv4 address consist of four numbers separated by dots: a.b.c.d where all four numbers are between 0 and 255. Special values include:
    - **127.0.0.1** Your own local machine. Also referred to as localhost
    - **192.168.x.y** Your private network. For instance, your machine and all machines on your private wifi network will usually have the 192.168 prefix. 
    -
### Port 
* * In order for multiple programs to listen for new network connections on the same machine without colliding, they pick a port to listen on. A port is
* an integer between 0 and 65,535 (2^16 ports total). 
* * Typically, ports 0-1023 are reserved for system ports (also called well-known ports) and shouldn't be used by user-level-processes. Certain ports
* have pre-defined uses, and although you usually won't be required to have them memorized, they can sometimes come in handy. Below some examples:
*     - 22: secure shell 
*     - 53: DNS lookup 
*     - 80: HTTP
*     - 443: HTTPs

### DNS
* Short for Domain Name System, it describes the entities and protocols involved in the translation from domain names to IP Addresses. 
* Typically, machines make a DNS query to a well known entity which is responsible for returning the IP address (or multiple ones) of the requested
domain name in the response. 


