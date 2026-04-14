# Room 6- OSI Model - TryHackMe [🔗](https://tryhackme.com/room/osimodelzi)

**Completed:** xx March 2026  
**Difficulty:** Easy | **Time:** ~30-60min
**Room:** [Become a Defender](https://tryhackme.com/room/osimodelzi)

**Spoiler warning** — This write-up contains **zero answers**.

## Overview

This room is a straightforward introduction to the OSI model and how networking is actually structured layer by layer. I went through all the tasks, answered the questions about each layer, and finished with the OSI dungeon game where I managed to beat the staff high score with 18.59 seconds. I learned what each of the seven layers does, from the Physical layer handling cables and electrical signals all the way up to the Application layer that we interact with every day in browsers and email clients. It also covered important details like TCP vs UDP on the Transport layer, MAC addresses on the Data Link layer, and how encapsulation works as data moves down the stack. The room wasn’t too heavy and the practical game helped reinforce the order of the layers. Overall I think this is a decent foundation before jumping into more technical networking topics like packets and frames.

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/06-OSI-model-completion-badge.png)

---

## Personal, handwritten notes from the room (redacted - no answers visible)

---

**TASK 1 - WHAT IS OSI MODEL?**

This task gave a clear overview of what the OSI model actually is and why it matters in networking. I learned that it’s a seven-layer framework that standardises how devices send, receive and understand data, so completely different hardware and software can still talk to each other. The room showed the full diagram with Layer 7 at the top down to Layer 1 at the bottom, and explained the idea of encapsulation. It was useful to see that this model is the reason networks work even when devices are made by different companies. Overall it set a good foundation before diving into the individual layers.
![Task 1 - redacted](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/06-OSI-model-task-1.png)

**TASK 2 - LAYER 1 - PHYSICAL**

In this task they explained Layer 1, which is all about the actual physical hardware and electrical signals. I learned that this is the lowest layer and it deals with things like cables, bits (0s and 1s) and the physical connection between devices. It was simple but important to understand that without this layer nothing else would work. The examples with ethernet cables made it easy to picture. This one helped me see the real hardware side of networking that we usually don’t think about.


**TASK 3 - LAYER 2 - DATA LINK**

This task covered Layer 2 and focused on physical addressing with MAC addresses. I learned that the Data Link layer adds the MAC address so the data knows exactly which device it should go to on the local network. It also explained that MAC addresses are burned into the network card and can be spoofed. The NIC (Network Interface Card) was mentioned as the hardware that holds the MAC address. It was interesting to see how this layer works right above the physical cables.


**TASK 4 - LAYER 3 - NETWORK**

Here they explained Layer 3, the Network layer, and how routing happens. I learned that this layer uses IP addresses to decide the best path for data to travel across different networks. They mentioned protocols like OSPF and RIP that help choose the shortest or most reliable route. It was useful to understand that routers are Layer 3 devices because they work with IP addresses. This task started to show how data actually moves between different networks.
![Task 4 - redacted](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/06-OSI-model-task-4.png)

**TASK 5 - LAYER 4 - TRANSPORT**

This task was about Layer 4 and the two main protocols: TCP and UDP. I learned that TCP is reliable with error checking and guarantees delivery, while UDP is faster but doesn’t care if packets get lost. They gave good examples like email using TCP and video streaming using UDP. The table comparing advantages and disadvantages made it clear when to use each one. This was one of the more useful tasks because these protocols come up a lot in real networking.
![Task 5 - redacted](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/06-OSI-model-task-5.png)

**TASK 6 - LAYER 5 - SESSION**

In this task they explained Layer 5, which manages the connection between devices. I learned that the Session layer creates, maintains and closes sessions, and can use checkpoints so only lost data needs to be resent. It was interesting to see that sessions are unique to each connection. This layer felt a bit more abstract than the lower ones but it makes sense for keeping communication stable.


**TASK 7 - LAYER 6 - PRESENTATION**

This task covered Layer 6, the Presentation layer. I learned that it acts like a translator, converting data into a format that the application layer can understand, and also handles encryption like HTTPS. It standardises how data looks so different software can still read it correctly. The email client example helped me understand why two different programs can still show the same message. This one showed how the model makes everything compatible.


**TASK 8 - LAYER 7 - APPLICATION**

The last theory task explained Layer 7, the Application layer. I learned that this is the layer we actually interact with, like browsers, email clients or file transfer programs. It’s where protocols like DNS and HTTP live, and it provides the user interface for data. This felt the most familiar because it’s the part we see every day. It was a good way to finish the theory part of the room.


**TASK 9 - PRACTICAL - OSI GAME**

In this practical I played the OSI dungeon game where you have to climb the layers in the correct order to escape. I managed to beat the staff high score of 19 seconds with my time of 18.59. It was a fun way to test if I remembered the order of the layers. The game was simple but effective for reinforcing what I just learned. This was a nice hands-on end to the room.
![Task 9 - redacted](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/06-OSI-model-task-9-score.png)

**TASK 10 - CONTINUE YOUR LEARNING: PACKETS & FRAMES**
The final task just pointed me to the next room called Packets and Frames. It felt like a natural next step after finishing the OSI model. Overall this room gave me a clear picture of how networking is structured layer by layer. I think it was a good, steady introduction without being too overwhelming.


---

## Further Learning & Professional Context
*Supplemental analysis generated through AI-assisted research*

---

### Core Concepts
1. **Protocol Data Unit (PDU)** — the layer-specific unit of data, such as a segment, packet, or frame, that moves through a network stack. ([networklessons.com](https://networklessons.com/network-fundamentals/introduction-to-the-osi-model))
2. **Header** — metadata added by a protocol layer that helps identify, route, or process the data. ([cloudflare.com](https://www.cloudflare.com/learning/network-layer/what-is-a-packet/?utm_source=chatgpt.com))
3. **Payload** — the actual useful data carried inside a packet after the headers are removed. ([cloudflare.com](https://www.cloudflare.com/learning/network-layer/what-is-a-packet/?utm_source=chatgpt.com))
4. **Trailer** — extra data appended to the end of a frame or packet to support integrity checks and related control functions. ([cisco.com](https://www.cisco.com/c/dam/en/us/td/docs/switches/connectedgrid/cg-switch-sw-master/software/configuration/guide/prp/b_prp_ie2000u.html?utm_source=chatgpt.com))
5. **MTU (Maximum Transmission Unit)** — the largest packet size a network-connected device or path can accept without fragmentation issues. ([cloudflare.com](https://www.cloudflare.com/learning/network-layer/what-is-mtu/?utm_source=chatgpt.com))
6. **Fragmentation** — the process of breaking oversized packets into smaller pieces so they can fit the network path’s limits. ([cloudflare.com](https://www.cloudflare.com/learning/network-layer/what-is-mss/?utm_source=chatgpt.com))
7. **Socket** — the endpoint of network communication, usually described by an IP address and port combination. ([networklessons.com](https://networklessons.com/network-fundamentals/introduction-to-the-osi-model))
8. **Throughput** — the amount of data successfully delivered over a network in a given time period. ([networklessons.com](https://networklessons.com/network-fundamentals/introduction-to-the-osi-model))
9. **Latency** — the delay between sending data and receiving a response. ([learn.microsoft.com](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/tracert?utm_source=chatgpt.com))
10. **Jitter** — the variation in latency over time, which can make voice and video traffic unstable. ([learn.microsoft.com](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/pathping?utm_source=chatgpt.com))

### Reading resources
**Beginner**
- **Cisco Learning Network — OSI Model Reference Chart**: a clean visual summary of the seven layers and common examples for each layer. ([learningnetwork.cisco.com](https://learningnetwork.cisco.com/s/article/osi-model-reference-chart?utm_source=chatgpt.com))
- **Cloudflare Learning Center — What is a packet?**: a beginner-friendly explanation of packet structure, including headers and payloads. ([cloudflare.com](https://www.cloudflare.com/learning/network-layer/what-is-a-packet/?utm_source=chatgpt.com))

**Technical**
- **Wireshark User’s Guide**: the official manual for capturing, viewing, and filtering packets in detail. ([wireshark.org](https://www.wireshark.org/docs/wsug_html_chunked/))

### Career insights
This room matters later because almost every cybersecurity role depends on being able to map real traffic or logs back to the right layer of the stack. ([nist.gov](https://www.nist.gov/itl/applied-cybersecurity/nice/nice-framework-resource-center/getting-started))
For SOC work, OSI thinking helps you decide whether a problem is at the host, transport, routing, or application layer before you waste time on the wrong fix. ([networklessons.com](https://networklessons.com/network-fundamentals/introduction-to-the-osi-model))
For security engineering and pentesting, it gives you a shared language for debugging controls, validating exposure, and understanding where protections actually sit. ([nist.gov](https://www.nist.gov/itl/applied-cybersecurity/nice/nice-framework-resource-center/getting-started?utm_source=chatgpt.com))
The NICE Framework exists partly to give the cybersecurity workforce a common language for work roles, tasks, knowledge, and skills, so OSI literacy fits directly into that broader professional vocabulary. ([nist.gov](https://www.nist.gov/itl/applied-cybersecurity/nice/nice-framework-resource-center/getting-started))
The more naturally you can think in layers, the faster you can move from memorizing concepts to reading packet traces and explaining what happened. ([wireshark.org](https://www.wireshark.org/docs/wsug_html_chunked/))

### Professional Tools
- **Wireshark (start early, especially for SOC)** — the standard packet-capture and packet-analysis tool for learning how traffic behaves and for investigating real network evidence. ([wireshark.org](https://www.wireshark.org/docs/wsug_html_chunked/))
- **`ping` (start early, especially for SOC)** — the primary TCP/IP command for checking reachability, connectivity, and name resolution. ([learn.microsoft.com](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ping?utm_source=chatgpt.com))
- **`tracert` / `pathping` (start early)** — path-tracing tools that help you see routing hops, latency, and packet loss between two endpoints. ([learn.microsoft.com](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/tracert?utm_source=chatgpt.com))
- **`netstat` (start early, especially for SOC)** — a quick host-triage command that shows active TCP connections, listening ports, and routing statistics. ([learn.microsoft.com](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/netstat?utm_source=chatgpt.com))
- **Nmap (start early once you are comfortable with scanning concepts)** — an open-source tool for network discovery and security auditing, useful for seeing what hosts and services are actually exposed. ([nmap.org](https://nmap.org/book/man.html?utm_source=chatgpt.com))
- **`tcpdump` (start early if you use Linux)** — a command-line packet capture tool that is useful for fast, lightweight traffic inspection. ([wireshark.org](https://www.wireshark.org/docs/wsug_html_chunked/))
- **Wireshark display filters (start early)** — the filtering system that lets you narrow captures to the packets that matter instead of staring at raw noise. ([wireshark.org](https://www.wireshark.org/docs/wsug_html_chunked/ChWorkDisplayFilterSection.html?utm_source=chatgpt.com))

### Learning path
This room sits in TryHackMe’s **Pre Security** path, which includes **Intro to LAN**, **OSI Model**, **Packets & Frames**, and **Extending Your Network** in the networking sequence. ([tryhackme.com](https://tryhackme.com/path/outline/presecurity?utm_source=chatgpt.com))
It comes after the LAN basics and before packet/frame detail, so it acts as the bridge between “how local networks work” and “how data is actually represented on the wire.” ([tryhackme.com](https://tryhackme.com/path/outline/presecurity?utm_source=chatgpt.com))
Your notes line up with that flow: the room is clearly designed to prepare you for packet-level thinking in the next step. ([tryhackme.com](https://tryhackme.com/room/osimodelzi?utm_source=chatgpt.com))

### Critical Operational Pitfalls
- **Memorizing the layer order without mapping it to evidence** — avoid this by using packet captures and real traffic examples to identify which layer is actually failing. ([wireshark.org](https://www.wireshark.org/docs/wsug_html_chunked/))
- **Confusing OSI with TCP/IP as if they were the same model** — avoid this by remembering that OSI is a reference framework and TCP/IP is the practical Internet protocol stack. ([networklessons.com](https://networklessons.com/network-fundamentals/introduction-to-the-osi-model))
- **Blaming the wrong layer too quickly** — avoid this by checking the lower layers first when connectivity fails and the higher layers when the network is reachable but the application is not. ([learn.microsoft.com](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ping?utm_source=chatgpt.com))
- **Ignoring MTU and fragmentation problems** — avoid this by checking whether packet size exceeds the path’s limit when traffic behaves strangely or disappears. ([cloudflare.com](https://www.cloudflare.com/learning/network-layer/what-is-mtu/?utm_source=chatgpt.com))
- **Capturing packets from the wrong place** — avoid this by making sure the capture point is actually seeing the traffic you want to study, then use Wireshark filters to reduce noise. ([wireshark.org](https://www.wireshark.org/docs/wsug_html_chunked/ChapterCapture.html?utm_source=chatgpt.com))
- **Overtrusting `ping` as proof that everything works** — avoid this by following up with `tracert`, `pathping`, and packet analysis, because reachability alone does not prove the service is healthy. ([learn.microsoft.com](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ping?utm_source=chatgpt.com))

### Prerequisites check
The main knowledge gaps to close next are packet structure, MTU/fragmentation, and the habit of mapping issues to the correct layer instead of guessing. ([cloudflare.com](https://www.cloudflare.com/learning/network-layer/what-is-a-packet/?utm_source=chatgpt.com))
It also helps to be comfortable with basic command-line networking tools and with opening a capture file in Wireshark. ([learn.microsoft.com](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ping?utm_source=chatgpt.com))
If those ideas still feel fuzzy, the next packet-focused room is the right place to reinforce them. ([tryhackme.com](https://tryhackme.com/room/packetsframes?utm_source=chatgpt.com))

---

**Methodology Note:** This section uses GPT-5.4 Thinking-Mini to provide a structured analysis of industry context, career pathways, and extended resources. Questions were formulated based on room content, and responses were validated against official documentation and industry sources.

**Generation Details:**
- Model: GPT-5.4 Thinking-Mini
- Date: 2026-04-12
- Prompt Framework: coming soon

---

## Next Steps
- I will reinforce my knowledge - read about the most important concepts and terms I learned in this room
- I will do research to study the OSI Model, ways to protect it, the way threat actors want to attack it, common mistakes in defense, and vulnerabilities, the most respected and considered "trade-mark-in-industry" tools used to protect each layer
- I am moving into the next room - [*Room 7 - Packets & Frames*](https://tryhackme.com/room/packetsframes)

## My profiles
- TryHackMe: [EchoHound](https://tryhackme.com/p/EchoHound)
- GitHub: [micromediacoding](https://github.com/micromediacoding)

---

*Write-up style follows my repository philosophy.*
