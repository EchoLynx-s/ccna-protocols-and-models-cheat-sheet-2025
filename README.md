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
