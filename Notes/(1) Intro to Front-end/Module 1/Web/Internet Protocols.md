A framework that caters to the **Request-Response Cycle** by delivering *data packets* back and forth the Server-Client pathway.

### Why?

* Data packets' order might get disturbed in transit.
* They may get misrouted.
* The data may get corrupted.

### How?

Just as the real-time conventional postal system.
The client sends a request to the server and gets the desired response via IP.

![[Pasted image 20230904183350.png]]

| Property | Postal System | Internet Protocol | 
|----------| -------- | -------- |   
| Address | <span style="color:gray">H-3, Street lane</span> | <span style="color:gray">192.162.0.5</span> |   
| Parcel | A mail | ![[Pasted image 20230905155226.png]] |
| Mode | Mailman | HTTP, TCP, UDP,... |


### Some Examples

| IP | Full Form | Application |
|--|--|--|
| HTTP | Hyper Text Transfer Protocol | Transfer web pages across the web |
| TCP | Transmission Control Protocol | Transfer data across the web in precise order and to the right client |
| UDP | User Datagram Protocol | Transfer data on the web corruption-free |
| DHCP | Dynamic Host Configuration Protocol | Gives each client its IP address and redirects responses to the correct ones.|
| DNS | Domain Name System Protocol | Regulates the corresponding website of an IP address. |
| IMAP | Internet Message Access Protocol | Retrieve messages and mails on the server |
| FTP | File Transfer Protocol | Send, receive, retrieve and delete files on a server |
| SMTP | Simple Mail Transfer Protocol | IMAP, but just for mails |
| SSH | Secure Shell Protocol | Access the server from client system, remotely |








