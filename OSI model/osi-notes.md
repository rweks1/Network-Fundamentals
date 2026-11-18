# The OSI Model (Open Systems Interconnection Model)
1. Introduction

The Open Systems Interconnection (OSI) Model is a conceptual framework used to explain how data is transmitted between devices over a network.

It was developed by the International Organization for Standardization (ISO) to standardize network communication and allow different computer systems and networking technologies to communicate with one another.

The OSI model divides network communication into seven layers, with each layer performing a specific function.

The seven layers are:

Physical Layer
Data Link Layer
Network Layer
Transport Layer
Session Layer
Presentation Layer
Application Layer

The OSI model helps network engineers, system administrators, and cybersecurity professionals understand, design, troubleshoot, and maintain computer networks.

2. The Seven Layers of the OSI Model
Layer 1: Physical Layer

The Physical Layer is the first and lowest layer of the OSI model.

It is responsible for transmitting raw binary data (bits: 0s and 1s) across a physical medium.

Main functions:

Transmits raw bits over a communication medium.
Defines physical network connections.
Specifies cables, connectors, and electrical signals.
Determines data transmission speeds.
Defines how devices connect physically.

Examples of technologies and equipment:

Ethernet cables.
Fiber optic cables.
Hubs.
Repeaters.
Network connectors.
Wireless radio signals.

Data unit: Bits.

Example: When two computers are connected using an Ethernet cable, the Physical Layer handles the transmission of electrical or optical signals between them.

Layer 2: Data Link Layer

The Data Link Layer is responsible for transferring data between devices on the same local network.

It organizes bits into frames and uses MAC (Media Access Control) addresses to identify devices on a local network.

Main functions:

Converts bits into frames.
Uses MAC addresses for local device identification.
Detects transmission errors.
Controls access to the communication medium.
Supports communication between devices on the same network segment.

Examples of technologies and equipment:

Ethernet (IEEE 802.3).
Wi-Fi (IEEE 802.11).
Switches.
Bridges.
MAC addresses.

Data unit: Frames.

Example: When a computer sends data to another computer on the same LAN, the Data Link Layer uses MAC addresses to help deliver the Ethernet frame to the correct device.

Layer 3: Network Layer

The Network Layer is responsible for logical addressing and routing data between different networks.

It determines the best available path for data to travel from the source network to the destination network.

Main functions:

Provides logical addressing using IP addresses.
Routes packets between networks.
Determines network paths.
Handles packet forwarding.
Supports communication across different networks.

Examples of technologies and equipment:

IPv4.
IPv6.
Routers.
ICMP.
IP routing protocols such as OSPF.

Data unit: Packets.

Example: When you access a website hosted on another network, the Network Layer uses IP addressing and routing to help deliver packets toward the destination.

Layer 4: Transport Layer

The Transport Layer provides end-to-end communication between applications running on different devices.

It manages data delivery and can provide reliability, error recovery, and flow control depending on the transport protocol used.

Main functions:

Divides application data into smaller units.
Supports end-to-end communication.
Uses port numbers to identify applications and services.
Provides reliability when using TCP.
Supports faster, connectionless delivery using UDP.
Performs segmentation and reassembly.

Main protocols:

TCP (Transmission Control Protocol):

Connection-oriented.
Provides reliable data delivery.
Uses acknowledgements.
Retransmits lost data.
Maintains data order.

UDP (User Datagram Protocol):

Connectionless.
Does not guarantee delivery.
Has lower protocol overhead.
Commonly used for real-time communication and streaming.

Examples of applications:

Web browsing.
Email.
Online gaming.
Video conferencing.

Data unit: Segments (TCP) and datagrams (UDP).

Example: When downloading a file, TCP helps ensure that the data arrives reliably and in the correct order.

Layer 5: Session Layer

The Session Layer manages communication sessions between applications on different devices.

It establishes, maintains, and terminates communication sessions.

Main functions:

Establishes communication sessions.
Maintains active sessions.
Terminates sessions when communication is complete.
Helps coordinate communication between applications.
Supports synchronization and recovery checkpoints in some systems.

Examples:

Remote Procedure Call (RPC).
NetBIOS session services.
Session management in application communication systems.

Data unit: Data.

Example: During a remote communication session, session-related functions help manage the ongoing exchange of information between applications.

Layer 6: Presentation Layer

The Presentation Layer is responsible for ensuring that data is represented in a format that the receiving application can understand.

It handles data translation, encryption, decryption, and compression.

Main functions:

Data format translation.
Data encryption and decryption.
Data compression and decompression.
Character encoding.
Data representation.

Examples:

UTF-8.
ASCII.
JPEG.
PNG.
MPEG.
Encryption and encoding formats.

Data unit: Data.

Example: When information is encrypted before transmission, presentation-related functions can help ensure that the receiving system can decrypt and interpret the information.

Layer 7: Application Layer

The Application Layer is the highest layer of the OSI model.

It provides network services and interfaces that applications use to communicate over a network.

It does not refer to the applications themselves but to the network services and protocols they use.

Main functions:

Provides network services to applications.
Supports web browsing.
Supports file transfers.
Supports email communication.
Enables name resolution.
Supports network management.

Examples of protocols:

HTTP and HTTPS.
FTP and SFTP.
SMTP.
DNS.
DHCP.
SSH.

Data unit: Data.

Example: When you open a website using a browser, HTTP or HTTPS is used to facilitate communication between the browser and the web server.

3. Summary of the Seven OSI Layers
Layer	Name	Main Function	Data Unit
7	Application	Network services for applications	Data
6	Presentation	Translation, encryption and compression	Data
5	Session	Manages communication sessions	Data
4	Transport	End-to-end delivery and reliability	Segments/Datagrams
3	Network	Logical addressing and routing	Packets
2	Data Link	MAC addressing and framing	Frames
1	Physical	Transmission of raw bits	Bits
4. Data Encapsulation and Decapsulation

Encapsulation is the process of adding protocol information to data as it moves down the OSI layers before transmission.

When a sender transmits data:

The Application Layer generates data.
The Presentation Layer formats or encrypts the data.
The Session Layer manages the communication session.
The Transport Layer adds transport information, including port numbers.
The Network Layer adds IP addressing information.
The Data Link Layer adds MAC addressing and frame information.
The Physical Layer transmits the data as bits.

At the receiving device, the reverse process takes place. This is called decapsulation.

Each layer processes and removes the relevant information before passing the remaining data to the next higher layer.

Data flow

Sending device:

Application → Presentation → Session → Transport → Network → Data Link → Physical

Receiving device:

Physical → Data Link → Network → Transport → Session → Presentation → Application

5. OSI Model and Networking Devices

Different networking devices operate primarily at different OSI layers.

Device	Primary OSI Layer
Hub	Layer 1 – Physical
Repeater	Layer 1 – Physical
Switch	Layer 2 – Data Link
Bridge	Layer 2 – Data Link
Router	Layer 3 – Network
Layer 4 Firewall	Layer 4 – Transport

Note: Some modern devices operate across multiple OSI layers. For example, multilayer switches can operate at Layers 2 and 3, while advanced firewalls can inspect information from several layers.

6. OSI Model vs TCP/IP Model

The OSI model is a seven-layer conceptual reference model, while the TCP/IP model is a networking framework based on the protocols used for communication across the Internet.

The TCP/IP model is commonly represented using four layers.

OSI Model	TCP/IP Model
Application (Layer 7)	Application
Presentation (Layer 6)	Application
Session (Layer 5)	Application
Transport (Layer 4)	Transport
Network (Layer 3)	Internet
Data Link (Layer 2)	Network Access
Physical (Layer 1)	Network Access
Main differences
OSI has seven layers, while the commonly used TCP/IP model has four.
OSI is primarily a reference model for understanding network communication.
TCP/IP is a practical protocol suite used for communication across interconnected networks.
OSI provides a more detailed separation of networking functions.
7. Importance of the OSI Model

Understanding the OSI model is important because it:

Simplifies networking: Divides complex communication processes into manageable layers.
Improves troubleshooting: Helps identify which part of a network may be experiencing a problem.
Promotes standardization: Allows different devices and technologies to communicate.
Supports network design: Helps engineers understand how networking technologies interact.
Improves cybersecurity knowledge: Helps security professionals understand where different security controls operate.
Supports learning: Provides a foundation for understanding TCP/IP, routing, switching, and network protocols.
8. Practical Examples of OSI Layers
Example 1: Opening a website

When you visit a website:

Layer 7: The browser uses HTTP or HTTPS.
Layer 6: Data representation and encryption functions are handled.
Layer 5: Session-related communication is managed.
Layer 4: TCP or UDP carries application traffic.
Layer 3: IP addresses help route packets.
Layer 2: Frames are transmitted across the local network.
Layer 1: Physical or wireless signals carry the bits.
Example 2: Sending data between computers

When one computer sends data to another:

The sender prepares the application data.
Transport protocols provide the appropriate delivery service.
IP addresses identify the source and destination.
MAC addresses support delivery across the local link.
Physical signals transmit the data.
The receiving computer processes the information through the reverse layers.
9. Troubleshooting Using the OSI Model

The OSI model helps network technicians troubleshoot problems systematically.

Layer	Example of a Problem
Layer 1	Damaged Ethernet cable or no Wi-Fi signal
Layer 2	Incorrect VLAN configuration or MAC-related issue
Layer 3	Incorrect IP address, subnet mask or default gateway
Layer 4	Blocked TCP/UDP port or connection failure
Layer 5	Session establishment or maintenance failure
Layer 6	Data format or encryption compatibility issue
Layer 7	DNS, HTTP or application service failure

A useful troubleshooting approach is to start at Layer 1 and move upward, although the starting point can depend on the symptoms.

10. Memory Trick for the Seven Layers

To remember the OSI layers from Layer 7 down to Layer 1:

All People Seem To Need Data Processing

All – Application
People – Presentation
Seem – Session
To – Transport
Need – Network
Data – Data Link
Processing – Physical

From Layer 1 upward:

Please Do Not Throw Sausage Pizza Away

Please – Physical
Do – Data Link
Not – Network
Throw – Transport
Sausage – Session
Pizza – Presentation
Away – Application
11. Key Takeaways

The OSI model is an essential foundation in computer networking.

The seven layers work together to explain how information moves from one device to another across a network.

The most important concepts to remember are:

Layer 1 handles physical transmission.
Layer 2 handles frames and MAC addresses.
Layer 3 handles IP addressing and routing.
Layer 4 handles end-to-end transport using TCP and UDP.
Layer 5 manages communication sessions.
Layer 6 handles data representation, encryption and compression.
Layer 7 provides network services to applications.

Understanding these layers provides a strong foundation for studying switching, routing, subnetting, network security, and troubleshooting.

12. Personal Learning Reflection

What I learned:

I learned that the OSI model explains network communication through seven different layers. Each layer performs a specific function, and all the layers work together to enable devices to communicate.

What I found interesting:

I found it interesting that data goes through encapsulation before transmission and decapsulation when it reaches the receiving device.

I also learned how MAC addresses, IP addresses, and port numbers serve different purposes in network communication.

Areas I need to practise:

Identifying the seven OSI layers.
Understanding encapsulation and decapsulation.
Differentiating between MAC addresses and IP addresses.
Understanding TCP and UDP.
Identifying networking problems using the OSI model.
Applying the concepts using Cisco Packet Tracer.

Learning Resource: Cisco Networking Academy – https://www.netacad.com/
