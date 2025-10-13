# Activity Exemplar: Analyze Network Attacks

## Section 1: Identify the Type of Attack That May Have Caused This Network Interruption

One potential explanation for the website’s connection timeout
error message is a DoS (Denial-of-Service) attack. The logs 
show that the web server stops responding after it is 
overloaded with SYN packet requests.This event could be a 
type of DoS attack called SYN flooding.

---

## Section 2: Explain How the Attack Is Causing the Website Malfunction

When website visitors try to establish a connection with the 
web server, a three-way handshake occurs using the TCP 
protocol. The handshake consists of three steps:
1. A SYN packet is sent from the source to the destination, requesting to connect.  
2. The destination replies to the source with a SYN-ACK packet to accept the connection request. The destination will reserve resources for the source to connect.  
3. A final ACK packet is sent from the source to the destination acknowledging the permission to connect.

In the case of a SYN flood attack, a malicious actor sends
a large number of SYN packets all at once, which overwhelms
the server’s available resources reserved for new
connections. When this happens, there are no server
resources left for legitimate TCP connection requests. The
logs indicate that the web server has become overwhelmed
and is unable to process visitors’ SYN requests. 
As a result, the server cannot open new connections, 
and visitors receive a connection timeout message.
