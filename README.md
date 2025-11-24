# CCNA – Protocols and Models (Module 3)  

Quick-reference notes for NetAcad CCNA – Module 3: **Protocols and Models**.  
Focus is on how devices agree on rules (protocols), how protocol suites like TCP/IP are organized, and how data is encapsulated and addressed across networks.

⚠️ **This is a study helper, not an answer key.**  
I use it to revise concepts and remember key ideas for labs, Packet Tracer, and exams.

---

## Table of Contents

- [Module 3 Overview](#module-3-overview)  
- [Module Map](#module-map)
- [3.0 Introduction](#30-introduction)  
  - [3.0.1 Why should I take this module?](#301-why-should-i-take-this-module)  
  - [3.0.2 What will I learn to do in this module?](#302-what-will-i-learn-to-do-in-this-module)  
  - [3.0.3 Class Activity – Design a Communications System](#303-class-activity---design-a-communications-system)
- [3.1 The Rules](#31-the-rules)  
  - [3.1.1 Video – Devices in a Bubble](#311-video--devices-in-a-bubble)  
  - [3.1.2 Communications Fundamentals](#312-communications-fundamentals)  
  - [3.1.3 Communication Protocols](#313-communication-protocols)  
  - [3.1.4 Rule Establishment](#314-rule-establishment)  
  - [3.1.5 Network Protocol Requirements](#315-network-protocol-requirements)  
  - [3.1.6 Message Encoding](#316-message-encoding)  
  - [3.1.7 Message Formatting and Encapsulation](#317-message-formatting-and-encapsulation)  
  - [3.1.8 Message Size](#318-message-size)  
  - [3.1.9 Message Timing](#319-message-timing)  
  - [3.1.10 Message Delivery Options](#3110-message-delivery-options)  
  - [3.1.11 A Note About the Node Icon](#3111-a-note-about-the-node-icon)  
  - [3.1.12 Check Your Understanding – The Rules](#3112-check-your-understanding--the-rules)
- [3.2 Protocols](#32-protocols)  
  - [3.2.1 Network Protocol Overview](#321-network-protocol-overview)  
  - [3.2.2 Network Protocol Functions](#322-network-protocol-functions)  
  - [3.2.3 Protocol Interaction](#323-protocol-interaction)  
  - [3.2.4 Check Your Understanding – Protocols](#324-check-your-understanding--protocols)
- [3.3 Protocol Suites](#33-protocol-suites)  
  - [3.3.1 Network Protocol Suites](#331-network-protocol-suites)  
  - [3.3.2 Evolution of Protocol Suites](#332-evolution-of-protocol-suites)  
  - [3.3.3 TCP/IP Protocol Example](#333-tcpip-protocol-example)  
  - [3.3.4 TCP/IP Protocol Suite](#334-tcpip-protocol-suite)  
  - [3.3.5 TCP/IP Communication Process](#335-tcpip-communication-process)  
  - [3.3.6 Check Your Understanding – Protocol Suites](#336-check-your-understanding--protocol-suites)
- [3.4 Standards Organizations](#34-standards-organizations)  
  - [3.4.1 Open Standards](#341-open-standards)  
  - [3.4.2 Internet Standards](#342-internet-standards)  
  - [3.4.3 Electronic and Communications Standards](#343-electronic-and-communications-standards)  
  - [3.4.4 Lab – Research Networking Standards](#344-lab--research-networking-standards)  
  - [3.4.5 Check Your Understanding – Standards Organizations](#345-check-your-understanding--standards-organizations)
- [3.5 Reference Models](#35-reference-models)  
  - [3.5.1 The Benefits of Using a Layered Model](#351-the-benefits-of-using-a-layered-model)  
  - [3.5.2 The OSI Reference Model](#352-the-osi-reference-model)  
  - [3.5.3 The TCP/IP Protocol Model](#353-the-tcpip-protocol-model)  
  - [3.5.4 OSI and TCP/IP Model Comparison](#354-osi-and-tcpip-model-comparison)  
  - [3.5.5 Packet Tracer – Investigate the TCP/IP and OSI Models in Action](#355-packet-tracer--investigate-the-tcpip-and-osi-models-in-action)
- [3.6 Data Encapsulation](#36-data-encapsulation)  
  - [3.6.1 Segmenting Messages](#361-segmenting-messages)  
  - [3.6.2 Sequencing](#362-sequencing)  
  - [3.6.3 Protocol Data Units](#363-protocol-data-units)  
  - [3.6.4 Encapsulation Example](#364-encapsulation-example)  
  - [3.6.5 De-encapsulation Example](#365-de-encapsulation-example)  
  - [3.6.6 Check Your Understanding – Data Encapsulation](#366-check-your-understanding--data-encapsulation)
- [3.7 Data Access](#37-data-access)  
  - [3.7.1 Addresses](#371-addresses)  
  - [3.7.2 Layer 3 Logical Address](#372-layer-3-logical-address)  
  - [3.7.3 Devices on the Same Network](#373-devices-on-the-same-network)  
  - [3.7.4 Role of the Data Link Layer Addresses – Same IP Network](#374-role-of-the-data-link-layer-addresses--same-ip-network)  
  - [3.7.5 Devices on a Remote Network](#375-devices-on-a-remote-network)  
  - [3.7.6 Role of the Network Layer Addresses](#376-role-of-the-network-layer-addresses)  
  - [3.7.7 Role of the Data Link Layer Addresses – Different IP Networks](#377-role-of-the-data-link-layer-addresses--different-ip-networks)  
  - [3.7.8 Data Link Addresses](#378-data-link-addresses)  
  - [3.7.9 Lab – Install Wireshark](#379-lab--install-wireshark)  
  - [3.7.10 Lab – Use Wireshark to View Network Traffic](#3710-lab--use-wireshark-to-view-network-traffic)  
  - [3.7.11 Check Your Understanding – Data Access](#3711-check-your-understanding--data-access)
- [3.8 Module Practice and Quiz](#38-module-practice-and-quiz)  
  - [3.8.1 What did I learn in this module?](#381-what-did-i-learn-in-this-module)  
  - [3.8.2 Module Quiz – Protocols and Models](#382-module-quiz--protocols-and-models)

---

## Module 3 Overview

### Goal of the module

Understand **how communication actually works on a network**:

- Why protocols and rules are needed for devices to talk.
- How **protocol suites** like TCP/IP are organized into layers.
- What the **OSI** and **TCP/IP** reference models are and how they map to each other.
- How data is **encapsulated**, segmented, addressed, and delivered between local and remote devices.
- How different **addresses** (MAC, IP, port numbers) are used at different layers.
- Where **standards bodies** fit in (IETF, IEEE, ISO, etc.).

This repo is my personal brain-dump for Module 3 so I can quickly find:

- Definitions of all the core protocols (HTTP, TCP, IP, Ethernet, etc.).
- Layered model diagrams and mappings.
- Encapsulation / de-encapsulation flow notes.
- Addressing examples I can re-use in labs and Packet Tracer.

---

## Module Map

High-level view of what’s in this module:

### 3.0 – Introduction
Why protocols and models matter and what skills I should have at the end: understanding rules of communication, protocol stacks, and layered design.

### 3.1 – The Rules
Basic communication concepts:

- How devices “in a bubble” need shared **rules** to talk.
- Fundamentals of communication (sender, receiver, channel, encoding).
- What **protocols** are and how rules get established.
- Requirements like **encoding, formatting, size, timing, delivery options**.
- Encapsulation basics: wrapping messages with headers/trailers.

### 3.2 – Protocols
Dives into **individual network protocols**:

- Overview of network protocols and where they live (application, transport, internet, network access).
- Typical protocol functions: error detection, reliability, addressing, session control.
- How multiple protocols interact in a stack for one communication.

### 3.3 – Protocol Suites
Zooms out to full **protocol suites**, especially **TCP/IP**:

- What a protocol suite is and why suites replaced single-vendor stacks.
- TCP/IP as the dominant open suite.
- Example of how different TCP/IP protocols work together for a simple web request.
- Visual breakdown of the TCP/IP layers and core protocols in each.

### 3.4 – Standards Organizations
Who defines the rules:

- Why **open standards** matter in networking.
- Key internet standards bodies (like **IETF**, **ICANN**, etc.).
- Other electronic / telecom standards groups (like **IEEE**, **ISO**, **TIA**).
- Short research lab on standards and how to look them up.

### 3.5 – Reference Models
Theoretical models that structure networking:

- Benefits of layered models (simpler design, modularity, interoperability, troubleshooting).
- The **OSI 7-layer model**.
- The **TCP/IP 4-layer model**.
- How OSI and TCP/IP align and differ.
- Packet Tracer activity to watch both models in action for real traffic.

### 3.6 – Data Encapsulation
How data is prepared and sent:

- Why messages are **segmented** into smaller pieces.
- **Sequencing** so segments can be reassembled.
- Protocol Data Units (PDUs): segment, packet, frame, bits.
- Step-by-step encapsulation and de-encapsulation examples.
- Quick checks to make sure the flow makes sense.

### 3.7 – Data Access
How devices actually reach each other:

- Different **address types** (logical vs physical vs port numbers).
- Layer 3 logical addressing (IP) and how it identifies networks and hosts.
- Devices on the same network vs remote networks.
- How **MAC addresses** are used locally even when IP is involved.
- Role of **routers** and **default gateways**.
- Labs with **Wireshark** to capture and inspect real traffic and headers.

### 3.8 – Module Practice and Quiz
Wrap-up and assessment:

- Text summary of what I should now understand from Module 3.
- Final **Module Quiz – Protocols and Models** for self-checking.


---


### 3.0 Introduction

This module shifts from “plugging things in” to **how and why networks actually work** behind the scenes.

You already know how to cable devices and do basic IOS config.  
Now you’ll look at the **rules (protocols)** and **models (OSI / TCP-IP)** that explain:

- How devices agree on *how* to talk  
- How data is prepared, sent, delivered, and interpreted  
- How different vendors’ gear can still interoperate on the same network  

---

### 3.0.1 Why should I take this module?

Because configuration alone doesn’t guarantee that devices will communicate.

This module helps you:

- Understand **what protocols are**, who defines them, and why they matter  
- Use **models** (OSI and TCP/IP) to visualize where different protocols and tasks live  
- See how standards let multi-vendor networks work together instead of becoming “islands”  
- Build the mental map you’ll need later for routing, switching, security, and troubleshooting  

By the end, you won’t just memorize commands – you’ll know **where they sit in the stack** and what problem they solve.

---

### 3.0.2 What will I learn to do in this module?

**Module Title:** Protocols and Models  
**Module Objective:** Explain how network protocols enable devices to access **local and remote** network resources.

| Topic Title              | Topic Objective                                                                 |
|--------------------------|----------------------------------------------------------------------------------|
| **The Rules**            | Describe the kinds of rules communication needs to be successful.              |
| **Protocols**            | Explain *why* protocols are required in network communication.                 |
| **Protocol Suites**      | Explain the purpose of using an organized set of protocols (a suite).          |
| **Standards Organizations** | Explain the role of standards bodies in creating protocols for interoperability. |
| **Reference Models**     | Explain how the TCP/IP and OSI models help standardize the communication process. |
| **Data Encapsulation**   | Explain how encapsulation lets data be packaged and moved across a network.    |
| **Data Access**          | Explain how hosts access **local** resources on a network.                     |

Keep this table at the top of your notes as a “mini-map” of what Module 3 is trying to teach you.

---

### 3.0.3 Class Activity – Design a Communications System

**Scenario (short version)**  
You buy a new car, it starts having problems, and you take it to the *only* nearby repair shop.  
All the mechanics speak a different language, but you *must* get the car fixed.

Your job is to **design a communication model** so that:

- You can clearly describe the car’s symptoms  
- The mechanics can confirm what they understood  
- Both sides agree on steps, cost, and confirmation that the repair worked  

This mirrors networking: different systems, different “languages,” but shared **rules and procedures** allow successful communication. :contentReference[oaicite:0]{index=0}  

**Reflection question (for your own notes):**

> What steps did you decide were essential to communicate your repair request?
> Why are those steps important?

---

### 3.1 The Rules

High-level idea:  
For any communication to work (humans or networks), everyone needs to follow common **rules** – who talks, how they talk, in what format, at what time, and how we know the message arrived.

#### 3.1.1 Video – Devices in a Bubble

- A single device on a network is like a person in a “bubble”.
- Without shared **protocols** (rules), it cannot:
  - See its role in the network.
  - Understand messages from others.
  - Send messages in a way others understand.
- Protocols = what lets devices leave their bubble and participate in the network.

#### 3.1.2 Communications Fundamentals

Any communication method (talking, texting, networking) always has three core pieces:

- **Message source (sender)** – who is sending the information (person, PC, phone, server).
- **Message destination (receiver)** – who is supposed to get and interpret it.
- **Channel** – the medium/path the message travels over  
  (air for spoken voice, cable or Wi-Fi for network traffic, etc.).

A physical connection alone is not enough; devices also need rules about *how* to use the channel.

#### 3.1.3 Communication Protocols

- A **protocol** = a defined set of rules for communication.
- Human analogy: two people talking must:
  - Agree on a **language**.
  - Use understandable **sentence structure**.
- Network analogy:
  - A message flows: **source → transmitter → medium → receiver → destination**.
  - Each step follows strict rules (how bits are formed, framed, addressed, acknowledged, etc.).
- If rules are not followed, the message can be misunderstood or dropped.

#### 3.1.4 Rule Establishment

The scrambled sentence example shows that without rules, the message is hard to read.  
Protocols must cover at least:

- **Identified sender and receiver** – who is talking to whom.
- **Common language and grammar** – encoding, format, and structure everyone understands.
- **Speed and timing** – when to talk, when to listen, and how fast.
- **Confirmation / acknowledgments** – whether delivery needs to be confirmed or retried.

These rules must be agreed on *before* communication starts.

#### 3.1.5 Network Protocol Requirements

Network protocols share some core traits. They define **how** a message crosses the network, including:

- **Message encoding** – how information is turned into signals/bits.
- **Message formatting and encapsulation** – headers, fields, and how data is wrapped.
- **Message size** – maximum payload length, fragmentation rules, etc.
- **Message timing** – latency, timeouts, and retransmission behavior.
- **Message delivery options** – unicast, multicast, broadcast, best-effort vs reliable, etc.

#### 3.1.6 Message Encoding

Human analogy (phone call about a sunset):

- Thoughts → converted into a **language** (encoding).
- Spoken words → transmitted as **sound waves** over the phone.
- Listener → converts sound back into meaning (decoding).

Network version:

- Data is converted into **bits**.
- Bits are encoded as:
  - Voltages on copper,
  - Light pulses in fiber,
  - Radio waves / microwaves in wireless.
- The receiving host **decodes** these signals back into bits and then into useful data.

#### 3.1.7 Message Formatting and Encapsulation

Human analogy (sending a letter):

- The **letter** contains the message.
- The **envelope** has sender and receiver addresses in specific positions.
- If the format or addressing is wrong, the postal system cannot deliver it.
- Putting the letter into the envelope = **encapsulation**.  
  Taking it back out = **de-encapsulation**.

Network version:

- Internet Protocol (e.g. **IPv6**) defines a strict **packet format**:
  - Version, traffic class, flow label,
  - Payload length, next header, hop limit,
  - **Source IP address**, **Destination IP address**, etc.
- The IPv6 header (like the envelope) wraps the payload (the letter).  
- Routers and hosts read these fields to forward and deliver the packet correctly.

---
### 3.1.8 Message Size

**Idea:** Messages are usually broken into smaller pieces so they’re easier to handle.

- In human communication, long thoughts are split into sentences so the listener can process them.
- In networks, long messages are split into **frames** that must meet strict minimum and maximum size limits.
- Each frame carries:
  - A piece of the original data
  - Its own addressing information
- At the destination, all frames are **reassembled** into the original message.

---

### 3.1.9 Message Timing

**Idea:** When data is sent matters just as much as what is sent.

Message timing covers:

- **Flow Control**
  - Manages the **rate of data transmission**.
  - Prevents a fast sender from overwhelming a slow receiver.
  - Network protocols negotiate how quickly information can be sent.

- **Response Timeout**
  - How long a device waits for a reply before assuming something went wrong.
  - If no response is received in time, protocols define what action to take (retry, fail, etc.).

- **Access Method**
  - Decides **who can talk when** on a shared medium.
  - Prevents “collisions” when multiple devices try to send at the same time.
  - Wireless NICs, for example, use access methods to check if the medium is free before transmitting.

---

### 3.1.10 Message Delivery Options

**Idea:** There are different ways to deliver a message depending on who should receive it.

Network communication uses three main delivery types:

- **Unicast**
  - One sender → **one specific receiver**.
  - Most typical traffic on a network (e.g., your PC talking to a server).

- **Multicast**
  - One sender → **a selected group of receivers**.
  - Only hosts that joined the multicast group process the traffic; others ignore it.
  - Switches forward multicast frames out all ports except the incoming one, but only group members actually use them.

- **Broadcast**
  - One sender → **all devices** on the local network segment.
  - Everyone receives and processes the message (within the broadcast domain).

---

### 3.1.11 A Note About the Node Icon

**Idea:** Diagrams often simplify devices into generic “nodes”.

- Networking docs and topologies frequently show devices as **circles** (nodes) instead of detailed PC or switch icons.
- These node diagrams are used to illustrate:
  - **Unicast**: one arrow from one node to another.
  - **Multicast**: one node sending to several selected nodes.
  - **Broadcast**: one node sending to **all** other nodes.

This visual convention keeps protocol and delivery diagrams simple and easy to read.

---

### 3.1.12 Check Your Understanding – The Rules

- Short quiz with a few questions about:
  - Basic communication elements (source, destination, channel)
  - Protocol requirements (encoding, formatting, size, timing, delivery)
  - Unicast / multicast / broadcast concepts
- I use this section just to verify that I really understand the communication “rules” before moving on to the next topic.

---

### 3.2 Protocols

#### 3.2.1 Network Protocol Overview
- Network protocols are shared rules and formats that let devices exchange messages.
- Implemented in software, hardware, or both; each protocol has its own function and header format.

**Types of protocols:**

- **Network Communications Protocols**  
  - Allow devices to communicate over one or more networks.  
  - Examples: Ethernet, IP, TCP, HTTP, and many others.

- **Network Security Protocols**  
  - Protect data (authentication, integrity, encryption).  
  - Examples: SSH, SSL, TLS.

- **Routing Protocols**  
  - Let routers share routing information, compare paths, and choose the best route.  
  - Examples: OSPF, BGP.

- **Service Discovery Protocols**  
  - Automatically discover devices or services.  
  - Examples: DHCP (IP address allocation), DNS (name ↔ IP translation).

---

#### 3.2.2 Network Protocol Functions
Network communication protocols handle several key functions:

- **Addressing**  
  - Identifies sender and receiver using a defined addressing scheme.  
  - Examples: Ethernet MAC, IPv4, IPv6.

- **Reliability**  
  - Guarantees delivery or recovery if messages are lost/corrupted in transit.  
  - Example: TCP reliability mechanisms.

- **Flow Control**  
  - Ensures data flows at a rate that both devices can handle (prevents overwhelming the receiver).

- **Sequencing**  
  - Numbers each segment of data so the receiver can reassemble information in the correct order.

- **Error Detection**  
  - Detects if bits were corrupted during transmission (checksums, FCS, etc.).  
  - Examples: Ethernet, IPv4, IPv6, TCP all include error-detection fields.

- **Application Interface**  
  - Defines how applications talk over the network.  
  - Examples: HTTP/HTTPS when a browser talks to a web server.

---

#### 3.2.3 Protocol Interaction
Real communications use **multiple protocols together** as a stack.

Example: browsing a web page

- **HTTP**  
  - Controls how the web client (browser) and web server format and exchange requests/responses.

- **TCP**  
  - Manages the conversation between client and server: connection, reliability, sequencing, and flow control.

- **IP**  
  - Delivers packets from the source host to the destination host across one or more networks.

- **Ethernet**  
  - Delivers frames from one NIC to another on the local LAN.

Each layer focuses on its own job and relies on the lower layers to move the data across the network.

---

#### 3.2.4 Check Your Understanding – Protocols
- Quick quiz to verify you remember:
  - Types of protocols (communications, security, routing, service discovery).
  - Main protocol functions (addressing, reliability, flow control, sequencing, error detection, application interface).
  - How protocols interact in a stack (HTTP → TCP → IP → Ethernet).

---

### 3.3 Protocol Suites

#### 3.3.1 Network Protocol Suites
- A **protocol suite** = group of related protocols that work together to perform a full communication function.
- You can picture it as a **stack of layers**:
  - **Physical layer** – how bits/voices are physically sent (copper, fiber, radio… or people speaking).
  - **Rules layer** – agreements about *how* to communicate (language, take turns, signal when finished).
  - **Content layer** – the actual message (“Where is the café?”).
- In networking, multiple protocols in different layers cooperate to move data and make sense of it at the destination.

---

#### 3.3.2 Evolution of Protocol Suites
Several protocol suites existed over time:

- **TCP/IP Suite**
  - Most common + relevant today.
  - Open standard maintained by the **IETF**.
  - Layers: Application, Transport, Internet, Network Access.

- **OSI Protocols**
  - Family of protocols from **ISO** + **ITU** (1977).
  - Introduced the famous **7-layer OSI model**.
  - Today mostly used as a **reference model**, not as a full protocol stack.

- **AppleTalk**
  - Proprietary suite from Apple (1985).
  - Replaced by TCP/IP when Apple adopted IP in 1995.

- **Novell NetWare**
  - Proprietary NetWare/IPX suite from Novell (1983).
  - Novell later adopted TCP/IP around 1995 and dropped IPX.

*Bottom line:* TCP/IP “won” and is now the universal protocol suite; others are mostly historical.

---

#### 3.3.4 TCP/IP Protocol Suite

TCP/IP is organized in 4 layers. Each layer has typical protocols:

##### Application Layer
Used directly (or indirectly) by applications.

- **Name System**
  - **DNS** – translates domain names (e.g. `cisco.com`) to IP addresses.

- **Host Config**
  - **DHCPv4 / DHCPv6** – dynamically hand out IPv4 / IPv6 addresses and options.
  - **SLAAC** – lets IPv6 hosts self-configure addresses without a DHCPv6 server.

- **Email**
  - **SMTP** – sends mail from client → mail server, and server → server.
  - **POP3** – downloads mail from server to local client.
  - **IMAP** – accesses and manages mail directly on the server.

- **File Transfer**
  - **FTP** – reliable, connection-oriented file transfer, with acknowledgements.
  - **SFTP** – file transfer over SSH (encrypted).
  - **TFTP** – simple, connectionless file transfer (best-effort, no acknowledgements).

- **Web & Web Services**
  - **HTTP** – transfers web pages and other content.
  - **HTTPS** – HTTP over TLS; encrypted web traffic.
  - **REST** – style of web APIs using HTTP verbs/URLs to build web services.

---

##### Transport Layer
Handles host-to-host conversations.

- **TCP**
  - Connection-oriented, reliable.
  - Provides acknowledgements, sequencing, flow control.

- **UDP**
  - Connectionless, “best effort”.
  - No delivery guarantee, no built-in recovery (used where speed/low overhead matters).

---

##### Internet Layer
Logical addressing and routing.

- **Internet Protocol**
  - **IPv4** – 32-bit addresses, packets.
  - **IPv6** – 128-bit addresses, newer IP version.
  - **NAT** – translates private IPv4 addresses ↔ public IPv4 addresses.

- **Messaging (ICMP family)**
  - **ICMPv4** – error + status messages for IPv4 (e.g. ping).
  - **ICMPv6** – similar for IPv6.
  - **ICMPv6 ND** – Neighbor Discovery (address resolution, duplicate detection, etc.).

- **Routing Protocols**
  - **OSPF** – link-state IGP, area-based, open standard.
  - **EIGRP** – Cisco-developed advanced IGP, uses composite metrics.
  - **BGP** – main protocol used between ISPs and large organizations (inter-domain routing).

---

##### Network Access Layer
Physical + data link rules.

- **Address Resolution**
  - **ARP** – maps IPv4 addresses ↔ MAC addresses (Layer 2).

- **Data Link Protocols**
  - **Ethernet** – rules for wiring/signaling and framing on local networks.
  - **WLAN (Wi-Fi)** – rules for wireless signaling on 2.4 GHz / 5 GHz, etc.

---

#### 3.3.5 TCP/IP Communication Process

**Example: web server → client**

1. **At the server (encapsulation)**
   - Application generates **Data** (web page).
   - **TCP** wraps it into a **TCP segment** (adds ports, reliability info).
   - **IP** wraps segment into an **IP packet** (adds source/destination IPs).
   - **Ethernet/WLAN** wraps packet into a **frame** (adds MAC addresses, FCS).
   - Bits are sent across the physical medium (copper, fiber, radio).

2. **Across the network**
   - Each router/switch looks at the relevant header (IP or MAC) to forward the frame/packet.
   - Data moves hop-by-hop until it reaches the client.

3. **At the client (de-encapsulation)**
   - Frame is received; data link layer checks FCS, strips frame header → passes **IP packet** up.
   - Network layer processes IP header, strips it → passes **TCP segment** up.
   - Transport layer reorders, checks reliability, strips header → passes **application data** up.
   - Application (web browser) renders the page.

*Key idea:* each layer adds its own header on the way out (encapsulation) and strips it off in reverse order on the way in (de-encapsulation).

---


### 3.4 Standards Organizations

**Big idea:**  
Networks only work because vendors agree on common standards. Different organizations define and maintain those standards so that devices and software from many manufacturers can interoperate.

---

#### 3.4.1 Open Standards

- **Open standards** = public specifications that any vendor can implement.
- Examples in networking: IPv4, IPv6, DHCP, SLAAC, Ethernet, 802.11 WLAN, TCP/IP.
- **Why they matter**
  - Interoperability – devices from different vendors can work together.
  - Competition – users are not locked into one manufacturer.
  - Innovation – vendors can build new features on top of shared standards.
- Standards orgs are usually **vendor-neutral, non-profit** groups that publish these documents.

---

#### 3.4.2 Internet Standards

Main players involved in internet / TCP-IP standards:

- **ISOC – Internet Society**  
  Promotes open development and use of the internet worldwide.

- **IAB – Internet Architecture Board**  
  Overall technical and architectural oversight for internet standards.

- **IETF – Internet Engineering Task Force**  
  - Develops, updates, and maintains internet and TCP/IP standards.  
  - Publishes **RFCs (Request for Comments)**.  
  - Organized into many working groups (routing, security, etc.).

- **IRTF – Internet Research Task Force**  
  - Focuses on long-term research related to internet and TCP/IP protocols.  
  - Works through research groups (e.g., crypto, anti-spam).

- **ICANN – Internet Corporation for Assigned Names and Numbers**  
  - Coordinates IP address allocation and domain names.  
  - Manages top-level domains and DNS root.

- **IANA – Internet Assigned Numbers Authority**  
  - Operated under ICANN.  
  - Maintains global registries for IP addresses, **TCP/UDP port numbers**, and other protocol parameters.

---

#### 3.4.3 Electronic and Communications Standards

Other organizations focus on the **physical and telecom** layers:

- **IEEE – Institute of Electrical and Electronics Engineers**  
  - Huge engineering standards body.  
  - Defines networking standards such as **802.3 Ethernet** and **802.11 WLAN**.

- **EIA – Electronic Industries Alliance**  
  - Known for standards related to electrical wiring, connectors, and 19-inch equipment racks.

- **TIA – Telecommunications Industry Association**  
  - Develops communication standards for structured cabling, radio, cellular, VoIP, satellite, etc.

- **ITU-T – International Telecommunication Union – Telecommunication Standardization Sector**  
  - UN-level organization.  
  - Defines global telecom standards (e.g., DSL, IPTV, many transmission and signaling standards).

---

#### 3.4.4 Lab – Research Networking Standards

**Goal of the lab**

- **Part 1 – Research networking standards organizations**
  - Look up major standards bodies and concepts such as:  
    ISO, ITU, ICANN, IANA, IEEE, EIA, TIA, ISOC, IAB, IETF, W3C, RFCs, Wi-Fi Alliance, important individuals (e.g., Jon Postel, Vint Cerf).
  - Answer questions about:
    - Who publishes RFCs.
    - Who manages domain names and IP address allocation.
    - Who defines web standards (W3C).
    - Examples of specific standards (Ethernet, Wi-Fi security, etc.).

- **Part 2 – Reflection**
  - Reflect on how standards enable the modern internet and global commerce.
  - Think about what would break if each vendor used its own incompatible protocols.

---

#### 3.4.5 Check Your Understanding – Standards Organizations

Short **4-question quiz** that checks if you can:

- Match orgs to their responsibilities (IETF vs ICANN vs IEEE vs ITU, etc.).
- Recognize which bodies control domain names, IPs, ports, and which define physical/network standards.


===

### 3.5 Reference Models

#### 3.5.1 The Benefits of Using a Layered Model

- We can’t watch packets moving across a real network, so we use **models** to visualise what’s happening.
- A **layered model** breaks the network into manageable pieces (layers) with clear responsibilities.
- Benefits of a layered model:
  - Makes protocol design easier: each layer has defined inputs/outputs and services.
  - Devices/protocols from different vendors can interoperate (as long as they follow the same layer rules).
  - Changes/updates in one layer don’t force changes in other layers (good modularity).
  - Encourages competition (vendors can innovate at one layer).
  - Provides a common language to talk about networking functions and capabilities.
- Two main reference models:
  - **OSI Reference Model** (7 layers)
  - **TCP/IP Reference Model** (4 layers)

---

#### 3.5.2 The OSI Reference Model

Seven layers (top → bottom):

1. **Application (Layer 7)**  
   - Interfaces directly with user applications.  
   - Provides services like HTTP, SMTP, FTP, DNS, etc.

2. **Presentation (Layer 6)**  
   - Data format and representation (encryption, compression, character sets).  
   - Ensures the data is in a usable format for the application.

3. **Session (Layer 5)**  
   - Starts, manages, and ends dialogs (sessions) between applications.  
   - Handles dialog control and synchronization.

4. **Transport (Layer 4)**  
   - Segments data, ensures end-to-end delivery.  
   - Reliability, flow control, error recovery (e.g. TCP).

5. **Network (Layer 3)**  
   - Logical addressing and routing between networks (IP).  
   - Decides the best path through the network.

6. **Data Link (Layer 2)**  
   - Moves frames across a single link or LAN.  
   - MAC addressing, framing, error detection on the link.

7. **Physical (Layer 1)**  
   - Actual bits on the wire/fiber/air.  
   - Electrical/optical signalling, connectors, media, physical topologies.

> OSI layers are often referred to by **number** (Layer 1, Layer 2, etc.) as well as by name.

---

#### 3.5.3 The TCP/IP Protocol Model

Four layers (top → bottom):

1. **Application**  
   - What the user sees: web, email, file transfer, etc.  
   - Includes many protocols: HTTP, HTTPS, DNS, SMTP, FTP, etc.  
   - Also handles some encoding and dialog control that OSI would put in Session/Presentation.

2. **Transport**  
   - Process-to-process delivery between hosts.  
   - Main protocols:
     - **TCP** – reliable, connection-oriented.
     - **UDP** – unreliable, connectionless, low overhead.

3. **Internet**  
   - Chooses the best path through the network.  
   - Logical addressing and routing (IPv4, IPv6, ICMP, routing protocols, etc.).

4. **Network Access**  
   - How data is actually placed on the physical network.  
   - Combines OSI’s Data Link + Physical functions.  
   - Includes Ethernet, WLAN, and other link-layer technologies.

---

#### 3.5.4 OSI and TCP/IP Model Comparison

- **Layer mapping:**

  - **TCP/IP Application** ⟷ OSI **Application + Presentation + Session**  
  - **TCP/IP Transport** ⟷ OSI **Transport**  
  - **TCP/IP Internet** ⟷ OSI **Network**  
  - **TCP/IP Network Access** ⟷ OSI **Data Link + Physical**

- **Similarities**
  - Both models use **layers** to describe networking functions.
  - Both highlight **Transport** and **Network/Internet** as key for end-to-end communication.
  - Both are used as reference points when discussing protocols and troubleshooting.

- **Differences**
  - OSI separates Presentation and Session; TCP/IP rolls them into the Application layer.
  - OSI splits Data Link and Physical; TCP/IP combines them as Network Access.
  - OSI is mostly a **theoretical** model; TCP/IP grew directly from the **real protocol suite** used on the internet.

---

#### 3.5.5 Packet Tracer – Investigate the TCP/IP and OSI Models in Action

- Goal: Use **Packet Tracer Simulation mode** to watch how data is encapsulated and de-encapsulated across the network while fetching a web page. :contentReference[oaicite:0]{index=0}  

- **Scenario**
  - A **Web Client** requests a page from **www.osi.local** on a **Web Server**.
  - Simulation mode shows each step as animated PDUs moving between devices.

- **Key tasks**
  - Switch from **Realtime** to **Simulation** mode and filter for **HTTP** events.
  - Generate HTTP traffic by browsing to `www.osi.local` from the Web Client.
  - Step through events with **Capture/Forward** and open each PDU:
    - View **OSI Model** tab: see which layers are active and what each one is doing.
    - View **Outbound / Inbound PDU Details**: see headers for Ethernet, IP, TCP, HTTP, DNS, etc.
  - Observe:
    - How data is **encapsulated** as it moves down the stack (Application → Transport → Internet → Network Access).
    - How it is then **de-encapsulated** at the destination.
    - How **DNS** resolves `www.osi.local` to an IP address.
    - How **TCP** sets up (ESTABLISHED) and tears down the connection.
    - Which **ports** are used (e.g. HTTP, DNS).

- **Big idea**
  - The lab visually ties together:
    - OSI vs TCP/IP layers,
    - PDU names and headers,
    - and how real protocols (HTTP, TCP, IP, Ethernet, DNS) cooperate to deliver a simple web page.

---

### 3.6 Data Encapsulation

Encapsulation is how data is prepared for transmission across the network.  
Each layer adds its own header (and sometimes trailer), turning the original message into smaller, well-labeled units that can travel efficiently and be reassembled correctly.

---

#### 3.6.1 Segmenting Messages

A single large communication (video, email with big attachments, etc.) is **not** sent as one huge stream of bits.

**Segmentation**

- The message is divided into smaller pieces (segments) before transmission.
- Each segment can be sent separately, possibly over different paths.
- At the destination, segments are reassembled into the original message.

**Benefits**

- **Increased speed** – Because the data stream is split into packets, large amounts of data can be sent without one conversation monopolizing the link. Many different conversations can share the same network (multiplexing).
- **Increased efficiency** – If a single segment is lost, only that segment needs to be retransmitted instead of the entire original message.

---

#### 3.6.2 Sequencing

Once a message is segmented, the pieces must be kept in order.

- Each segment is given a **sequence number**.
- The receiver uses sequence numbers to:
  - Detect missing segments.
  - Reassemble the data in the correct order.

> In TCP, sequencing is what allows out-of-order segments to be rebuilt into the original data stream.

---

#### 3.6.3 Protocol Data Units (PDUs)

As data moves **down** or **up** the protocol stack, its form and name change.  
At each layer, a new header (and sometimes trailer) is attached, creating a different **Protocol Data Unit (PDU)**:

- **Data** – Generic term for the PDU at the **application layer**.
- **Segment** – PDU at the **transport layer** (TCP/UDP header + data).
- **Packet** – PDU at the **network layer** (IP header + segment).
- **Frame** – PDU at the **data link layer** (frame header + packet + frame trailer).
- **Bits** – PDU at the **physical layer** (electrical/optical/radio signals on the medium).

> If the transport header is **TCP**, the transport PDU is called a **segment**.  
> If the transport header is **UDP**, it is often called a **datagram**.

---

#### 3.6.4 Encapsulation Example (Server → Client)

Example: a web server sending a web page to a client.

1. **Application layer** (HTTP) creates the web page data.
2. **Transport layer** (TCP) adds its header → creates a **TCP segment**.
3. **Network layer** (IP) adds an IP header → creates an **IP packet**.
4. **Data link layer** (Ethernet) adds a frame header and trailer → creates an **Ethernet frame**.
5. **Physical layer** converts the frame into **bits** and sends them across the medium.

Each lower layer treats the PDU from the layer above as **data** and wraps it with its own control information.

---

#### 3.6.5 De-encapsulation Example (Client → Application)

At the receiving host, the process is reversed:

1. **Physical layer** receives the **bits** and reconstructs the **Ethernet frame**.
2. **Data link layer** checks the frame (e.g., FCS), strips its header/trailer, and passes the **IP packet** up.
3. **Network layer** reads the IP header, delivers the packet to the correct host, removes the IP header, and passes the **TCP segment** up.
4. **Transport layer** (TCP) uses ports and sequence numbers to reassemble the correct data stream, then passes the **application data** up.
5. **Application layer** (e.g., web browser) interprets the data and displays the web page.

This reverse process is **de-encapsulation**: headers/trailers are removed layer by layer until only the original application data remains.

---

## 3.7 Data Access

In the previous sections you saw how data is **segmented, encapsulated and addressed**.  
This topic focuses on **how addresses at different layers** are used to get data from a source device to its final destination.

On a typical Ethernet/IP network, **two OSI layers are responsible for delivering data end-to-end**:

- **Layer 3 – Network layer (IP)**  
  Logical addressing (IPv4/IPv6) used to deliver packets between networks.

- **Layer 2 – Data Link layer (Ethernet, WLAN, …)**  
  Physical / MAC addressing used to move frames from **one NIC to the next** on the local link.

---

### 3.7.1 Addresses

To move data across the network, each layer adds its own “addressing info”:

| OSI Layer        | What is added / used                                                                 |
|------------------|--------------------------------------------------------------------------------------|
| **Physical (L1)**| Timing, synchronization, voltage/light/wave patterns (no real address fields)       |
| **Data Link (L2)**| **Source & destination MAC addresses** – who sends and who receives the frame on this link |
| **Network (L3)** | **Source & destination IP addresses** – original sender and final receiver          |
| **Transport (L4)**| **Source & destination port numbers** – which application/process is talking       |
| **Upper layers** | Encoded application data (HTTP request, email, file data, etc.)                     |

> **Important:**  
> - Layer 3 addresses = **where the packet is going globally**.  
> - Layer 2 addresses = **who handles the frame next on this local network segment**.

---

### 3.7.2 Layer 3 Logical Address

A **logical address** is an address that is independent of the underlying hardware. On IP networks this is the **IP address**.

Example from the course:

- **PC1**: `192.168.1.110`  
- **Web Server**: `172.16.1.99`  
- Routers in between: `R1`, `R2`

PC1 sends an IP packet to the Web Server. Inside that packet:

- **Source IP**: `192.168.1.110` – “I am the original sender”
- **Destination IP**: `172.16.1.99` – “This is the final receiver”

These two IP addresses **stay the same along the whole path** from PC1 to the Web Server, no matter how many routers are in between.

#### Structure of an IP address

An IPv4 address has **two logical parts**:

1. **Network portion** (IPv4) / **Prefix** (IPv6)  
   - Identifies the **network**.  
   - All devices on the same network share this part.

2. **Host portion** (IPv4) / **Interface ID** (IPv6)  
   - Identifies the **individual device** on that network.  
   - Must be unique **within that network**.

The **subnet mask** (IPv4) or **prefix length** (IPv6, e.g. `/64`) defines **where the split occurs** between network and host portion.

---

### 3.7.3 Devices on the Same Network

Now consider PC1 sending data to an **FTP server on the same IPv4 network**.

Example addresses:

- **PC1**
  - IPv4: `192.168.1.110`
  - MAC: `AA-AA-AA-AA-AA-AA`
- **FTP Server**
  - IPv4: `192.168.1.9`
  - MAC: `CC-CC-CC-CC-CC-CC`

Because the **network part of the IPv4 address is the same** (`192.168.1.x`):

- PC1 knows the server is **local**, not remote.
- PC1 can send frames **directly** to the server’s MAC address (no router needed).

Inside the frame:

- **Data Link header**
  - Destination MAC = `CC-CC-CC-CC-CC-CC` (FTP server)
  - Source MAC      = `AA-AA-AA-AA-AA-AA` (PC1)
- **Network (IP) header**
  - Source IP       = `192.168.1.110`
  - Destination IP  = `192.168.1.9`
- **Payload**
  - TCP segment, FTP data, etc.

---

### 3.7.4 Role of the Data Link Layer Addresses – Same IP Network

On a **single Ethernet LAN**, Layer 2 is responsible for getting frames from one NIC to another.

- **Source MAC address**
  - MAC of the **sending NIC** (here: PC1).
  - Burned into the NIC by the manufacturer (can be overridden but conceptually “physical”).

- **Destination MAC address**
  - MAC of the **receiving NIC** (here: FTP server).

For local traffic:

1. PC1 creates an IP packet for `192.168.1.9`.
2. PC1 checks: “Is `192.168.1.9` on my network?”  
   Yes → no router needed.
3. PC1 looks up the server’s MAC address (e.g. using **ARP**).
4. PC1 builds an Ethernet frame with:
   - **Src MAC** = PC1 MAC
   - **Dst MAC** = FTP server MAC
   - Payload    = IP packet
5. The switch forwards the frame to the port where the FTP server is connected.

Result: the frame goes **PC1 → Switch → FTP server** without leaving the local network.

---

### 3.7.5 Devices on a Remote Network

Now imagine PC1 wants to talk to a **web server on a different network**:

- **PC1**: `192.168.1.110`
- **Web Server**: `172.16.1.99`
- **Default gateway (R1)**: `192.168.1.1`
- Another router **R2** between R1 and the server.

Because the network portions differ (`192.168.1.x` vs `172.16.1.x`):

- PC1 **cannot reach the server directly** on the local link.
- PC1 must send the frame to its **default gateway (R1)** instead.

On the first hop (PC1 → R1):

- **IP header**
  - Source IP      = `192.168.1.110` (PC1)
  - Destination IP = `172.16.1.99` (Web Server) ← note: *final target already set*
- **Ethernet header**
  - Source MAC     = PC1 MAC (`AA-AA-AA-AA-AA-AA`)
  - Destination MAC= R1’s interface MAC on this LAN (`11-11-11-11-11-11`)

R1 receives the frame, strips the L2 header, **keeps the IP header**, decides the next hop, then builds a new frame to send towards R2:

- IP header: **unchanged**
  - Source IP      = `192.168.1.110`
  - Destination IP = `172.16.1.99`
- New Ethernet header for link R1 → R2:
  - Source MAC     = R1’s outgoing interface MAC
  - Destination MAC= R2’s interface MAC (`22-22-22-22-22-22`)

This pattern repeats until the frame reaches the web server’s LAN.

> **Key idea:**  
> - **IP addresses stay the same from end to end.**  
> - **MAC addresses change at every hop** (every different physical network).

---

### 3.7.6 Role of the Network Layer Addresses

Layer 3 (IP) provides **end-to-end delivery between networks**.  
Using our remote‐network example:

- **Source IPv4 address**:  
  - `192.168.1.110` (PC1) – original sender.

- **Destination IPv4 address**:  
  - `172.16.1.99` (Web Server) – final receiver.

At every router:

1. The router **examines the destination IP**.
2. It consults its **routing table** to choose the best next hop.
3. It encapsulates the packet in a new Layer 2 frame appropriate for the outgoing interface.

Because the network parts of the source and destination IP addresses are different:

- The packet must cross **multiple Layer 3 networks**.
- Only routers (Layer 3 devices) can **forward** the packet between those networks.

Meanwhile, Layer 2:

- Only ensures delivery of the frame **over a single link** (one hop).
- Uses MAC addresses of the **current sender** and **current next hop**.

---

#### 3.7.7 Role of the Data Link Layer Addresses – Different IP Networks

When the **source and destination are on different IP networks**, the Layer-2 frame **cannot**
be sent directly to the final device. Instead, it must first go to the **default gateway**.

Example in the figure:

- **PC1**
  - IP: `192.168.1.110`
  - MAC: `AA-AA-AA-AA-AA-AA`
- **R1 (default gateway)**
  - IP: `192.168.1.1`
  - MAC: `11-11-11-11-11-11`
- **R2**
  - IP: `172.16.1.1`
  - MAC: `22-22-22-22-22-22`
- **Web Server**
  - IP: `172.16.1.99`
  - MAC: `AB-CD-EF-12-34-56`

For the **first hop** (PC1 → R1):

- **Layer 3 (IP header)**
  - Source IP: `192.168.1.110` (PC1)
  - Destination IP: `172.16.1.99` (Web Server – final target)
- **Layer 2 (Ethernet frame header)**
  - Source MAC: `AA-AA-AA-AA-AA-AA` (PC1 NIC)
  - Destination MAC: `11-11-11-11-11-11` (R1 NIC)

Key ideas:

- The **IP addresses already point all the way to the web server**, even though it’s on a
  different network.
- The **Ethernet frame** only cares about delivering the packet to the **next hop**  
  (here: the default gateway R1).
- Once R1 receives the frame, it strips off the old Layer-2 header and builds a **new frame**
  with its own MAC as the source and the next hop’s MAC as the destination.

So:
- **Layer 3 addresses = end-to-end**
- **Layer 2 addresses = link-by-link (hop-by-hop)**

---

#### 3.7.8 Data Link Addresses (Host to Router, Router to Router, Router to Server)

This section walks through how the **Layer 2 header changes at every hop**, while the  
**Layer 3 header stays the same** from PC1 to the Web Server.

##### Host to Router (PC1 → R1)

- **L3 Source IP:** `192.168.1.110` (PC1)  
- **L3 Destination IP:** `172.16.1.99` (Web Server)

- **L2 Source MAC:** PC1 NIC  
- **L2 Destination MAC:** R1 NIC (default gateway)

PC1 wraps the IP packet in an Ethernet frame destined for the router’s NIC, not the server.

##### Router to Router (R1 → R2)

R1 receives the frame, removes the old L2 header, examines the IP header, and forwards it
towards the next router R2.

- **L3 Source IP:** `192.168.1.110` (unchanged)  
- **L3 Destination IP:** `172.16.1.99` (unchanged)

- **L2 Source MAC:** R1 outgoing interface  
- **L2 Destination MAC:** R2 incoming interface

Again, only the **Ethernet header is replaced**; the IP addresses stay the same.

##### Router to Server (R2 → Web Server)

R2 repeats the process and forwards the packet to the final destination network.

- **L3 Source IP:** `192.168.1.110`  
- **L3 Destination IP:** `172.16.1.99`

- **L2 Source MAC:** R2 NIC  
- **L2 Destination MAC:** Web Server NIC

The web server finally receives a frame addressed directly to its own MAC.

##### Hop-by-Hop vs End-to-End (Summary Table)

| Hop              | L2 Source MAC      | L2 Destination MAC   | L3 Source IP      | L3 Destination IP |
|------------------|--------------------|----------------------|-------------------|-------------------|
| PC1 → R1         | PC1 MAC            | R1 MAC               | 192.168.1.110     | 172.16.1.99       |
| R1 → R2          | R1 outgoing MAC    | R2 MAC               | 192.168.1.110     | 172.16.1.99       |
| R2 → Web Server  | R2 MAC             | Web Server MAC       | 192.168.1.110     | 172.16.1.99       |

- **L3 (IP) stays constant** from sender to receiver.
- **L2 (MAC) is rewritten** at every hop to match the NICs on that specific link.

---

#### 3.7.9 Lab – Install Wireshark

Goal: get Wireshark ready so you can capture and inspect real traffic.

High-level steps:

1. **Download** Wireshark from the official site for your OS.
2. **Run the installer** and accept the defaults (including installing the capture driver
   like Npcap/WinPcap on Windows).
3. After installation, **launch Wireshark**.
4. You should see a list of network interfaces (Wi-Fi, Ethernet, etc.) ready for capture.

This lab is mostly about setup so future labs can focus on packet analysis.

---

#### 3.7.10 Lab – Use Wireshark to View Network Traffic

This lab has two parts and focuses on **ICMP (ping) traffic** and how **IP + MAC addresses**
appear in captured frames.

##### Part 1 – Capture & Analyze Local ICMP (same LAN)

1. On Windows, run:

   ```bash
   ipconfig /all
   ```

   and note:
   - Your **IPv4 address**
   - Your **NIC description**
   - Your **MAC (Physical) address**

2. Ask a teammate for their **IP address** on the same LAN.

3. Open **Wireshark**, start a capture on the correct interface.

4. In the filter bar, type:

   ```text
   icmp
   ```

   and apply the filter so only ping packets are shown.

5. In a command prompt, ping your teammate’s IP:

   ```bash
   ping 192.168.1.x
   ```

6. Back in Wireshark, select one of the **ICMP Echo Request** frames and expand:
   - **Ethernet II** to see:
     - Source MAC → your PC’s MAC
     - Destination MAC → teammate’s MAC
   - **Internet Protocol** to see:
     - Source IP → your IP
     - Destination IP → teammate’s IP
   - **ICMP** to see the type (echo request/reply).

Concepts to note:

- On a **local network**, the frame’s **destination MAC is the MAC of the actual target host**.
- Your PC learns that MAC address using ARP / local discovery before sending the frame.

##### Part 2 – Capture & Analyze Remote ICMP (different network)

1. Start a new capture in Wireshark (you can discard the previous one).
2. From a command prompt, ping some public domains, for example:

   ```bash
   ping www.yahoo.com
   ping www.cisco.com
   ping www.google.com
   ```

3. DNS will translate each name into an IP address – note those IPs.

4. In Wireshark, look at the ICMP request frames for each ping:

   - **IP header**
     - Destination IP = public IP of Yahoo / Cisco / Google
   - **Ethernet header**
     - Destination MAC **is not** the web server’s MAC.
     - Destination MAC = your **default gateway’s MAC** (the local router).

Key conclusions:

- For **remote destinations**, the **MAC address in your frame always belongs to your
  default gateway/router**, because the first hop is to the router.
- You can see the **real MACs of local hosts**, but never the MAC of remote hosts — each
  router along the path replaces the frame with one that uses MAC addresses valid on its
  current link.

---

#### 3.7.11 Check Your Understanding – Data Access

- Final quiz for this section with **6 questions**.
- Focus points you should be able to explain from memory:
  - Difference between **Layer 2 (MAC)** and **Layer 3 (IP)** addressing.
  - How addresses look when devices are on the **same network** vs a **remote network**.
  - Why **MAC addresses change hop-by-hop**, while **IP addresses stay end-to-end**.
  - The role of the **default gateway** in reaching remote networks.
  - How tools like **Wireshark** reveal this behavior in real traffic.

If you can sketch the path PC1 → R1 → R2 → Web Server and label **L2 and L3 addresses at
each hop**, you’re in a good place for this quiz.
