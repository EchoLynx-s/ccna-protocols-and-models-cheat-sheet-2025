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

