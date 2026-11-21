Linux-Based TCP Chat and File Transfer System using Netcat
Overview
This project demonstrates the fundamentals of TCP/IP networking using Netcat (nc) on Kali Linux. The objective was to establish direct communication between two endpoints, exchange messages in real time, transfer files over a TCP connection, and monitor network activity using Linux networking utilities.

The project was developed as a hands-on networking and cybersecurity lab to understand client-server communication, port management, TCP connections, and packet flow within a Linux environment.

Objectives
Establish TCP communication between two endpoints.
Create a terminal-based chat session using Netcat.
Transfer files over a TCP connection.
Monitor active network connections.
Analyze network traffic during communication.
Gain practical experience with Linux networking tools.
Technologies Used
Kali Linux
Netcat (nc)
TCP/IP
ss
tcpdump
Linux Terminal
Features
Real-Time Communication
Created a TCP listener on a custom port.
Connected a client to the listener.
Exchanged text messages between endpoints.
File Transfer
Sent files over TCP connections using Netcat.
Successfully transferred text files between sender and receiver.
Verified file integrity after transmission.
Connection Monitoring
Used ss to inspect listening ports and established connections.
Observed client and server port assignments.
Verified active TCP sessions.
Traffic Analysis
Captured network traffic using tcpdump.
Monitored packet flow during communication and file transfer.
Studied basic TCP traffic behavior.
Project Workflow
1. Start TCP Listener
nc -lvnp 4444
2. Connect as Client
nc <IP_ADDRESS> 4444
3. Exchange Messages
Client: Hello
Server: Hi
Client: How are you?
Server: Fine
4. Transfer a File
Receiver:

nc -lvnp 4444 > received.txt
Sender:

nc <IP_ADDRESS> 4444 < hello.txt
5. Verify Received File
cat received.txt
6. Monitor Active Connections
ss -tan
7. Capture Network Traffic
sudo tcpdump -i eth1 port 4444
Network Architecture
+-------------+                +-------------+
|   Client    |  TCP : 4444    |   Server    |
| Netcat (nc) | -------------> | Netcat (nc) |
+-------------+                +-------------+
Learning Outcomes
Through this project, I gained practical knowledge of:

TCP/IP communication
Client-server architecture
Network ports and sockets
Linux networking commands
Packet capture and analysis
Network troubleshooting
File transfer over TCP
Basic cybersecurity networking concepts
Future Improvements
Multi-client chat support
Encrypted communication
Bash automation scripts
User authentication
File integrity verification using SHA256
Logging and monitoring dashboard
Resume Description
Implemented a Linux-based TCP communication and file transfer system using Netcat. Established client-server connections, performed real-time messaging and file transfers, monitored active sessions using ss, and analyzed network traffic using tcpdump. Developed hands-on experience with TCP/IP networking, Linux administration, network monitoring, and cybersecurity fundamentals.

Author
Tamil M.Sc. Information Technology Cybersecurity Enthusiast
