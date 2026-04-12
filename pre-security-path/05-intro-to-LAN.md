# Room 5- Intro to LAN - TryHackMe

**Completed:** xx April 2026  
**Difficulty:** Easy | **Time:** ~30min
**Room:** [Intro to LAN](https://tryhackme.com/room/introtolan)

**Spoiler warning** — This write-up contains **zero answers**.

---

## Overview
This room is a straightforward introduction to how local area networks actually work. It covers the main LAN topologies, subnetting, how devices identify each other with ARP, and how DHCP automatically assigns IP addresses. I went through all the tasks, answered the questions, ran the interactive labs where I had to break different topologies and spoof a MAC address to get the flag, and did a few basic commands. I learned the advantages and disadvantages of Star, Bus and Ring topologies, why subnetting is important for security and organisation, how ARP maps IP addresses to MAC addresses, and the four-step DHCP process. It was useful to see these concepts explained clearly with diagrams and the practical parts helped me understand how they work in real scenarios. Overall I think this is a good foundation before moving on to more advanced networking like the OSI model.


**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/05-Intro-to-LAN-completion-badge.png)

---

## Personal, handwritten notes from the room (redacted - no answers visible)

**TASK 1 - INTRODUCING LAN TOPOLOGIES
In this task they explained the main types of LAN topologies like Star, Bus and Ring. I learned that Star is the most common today because it’s reliable and easy to add devices, even though it costs more with extra cabling and switches. Bus topology is cheaper but has a single backbone cable so everything can slow down or break if that cable fails. Ring topology uses a loop and data travels in one direction, which makes troubleshooting easier but a single fault can take down the whole network. There was also a practical lab where I had to break the topologies to get the flag. It was useful to see the real advantages and disadvantages of each design.

**TASK 2 - A PRIMER ON SUBNETTING**
This task introduced subnetting and why we split networks into smaller pieces. I learned that subnetting is basically dividing a big network so different departments or use cases can have their own smaller networks, which helps with efficiency, security and control. They explained the three main parts of an IP address on a subnet: network address, host address and default gateway. It made sense why big places like offices use subnetting instead of one flat network. The examples with cafés having separate employee and guest networks were clear. This one gave me a decent understanding of how networks are organised in real environments.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/05-Intro-to-LAN-task-2.png)

**TASK 3 - ARP**
Here they covered ARP and how devices find each other on the network. I learned that ARP maps IP addresses to MAC addresses using requests and replies, and every device keeps a cache of these mappings. The process is simple: a device broadcasts an ARP request asking who has a certain IP, and the owner replies with its MAC address. They also mentioned that MAC addresses can be spoofed, which can bypass some security. It was interesting to see how this low-level protocol actually works behind the scenes. This is one of those things I’ll probably use a lot when doing network troubleshooting later.

**TASK 4 - DHCP**
This task explained how DHCP automatically assigns IP addresses to devices. I learned the full four-step process: Discover, Offer, Request and ACK. The device sends a DHCP Discover, the server offers an IP, the device requests it, and the server confirms with ACK. It’s much easier than manually configuring every device. This is how most networks in real life give out IPs without manual work. It was a short but clear task that connected well with the previous ones about IP addresses.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/05-Intro-to-LAN-task-4.png)

**TASK 5 - CONTINUE YOUR LEARNING: OSI MODEL**
The last task just pointed me to the next room called Intro to OSI Model to keep going. It felt like a natural next step after learning about LANs, subnetting, ARP and DHCP. Overall this room gave me a good foundation on how local networks are built and how devices communicate inside them. I think it was a useful room before moving into more advanced networking concepts. It wasn’t too heavy and the practical parts helped me understand the theory better.

---

## Further Learning & Professional Context
*Supplemental analysis generated through AI-assisted research*

---

### Core Concepts
1. **VLAN (Virtual Local Area Network)** — a logical way to split one physical LAN into separate broadcast domains, which improves control and limits unnecessary traffic. 
2. **Broadcast domain** — the set of devices that receive a Layer 2 broadcast, and VLANs are commonly used to create separate broadcast domains. 
3. **Collision domain** — a network segment where frame collisions can happen on a shared medium, which is one reason switching is preferred over older shared Ethernet designs. 
4. **Access port** — a switch port that carries traffic for only one VLAN, usually for end devices like laptops, printers, or servers. 
5. **Trunk port** — a switch port that can carry traffic for multiple VLANs at the same time, which is useful between switches and network devices.
6. **NAT (Network Address Translation)** — a mechanism that translates private IP addresses to public IP addresses so private networks can reach the internet. 
7. **CIDR notation** — a compact way to write IP networks, such as `/24`, where the suffix shows how many bits belong to the network portion.
8. **Routing table** — the local table a system uses to decide where packets should go next, including default and specific routes. 
9. **MTU (Maximum Transmission Unit)** — the largest frame or packet size a device or interface will accept before fragmentation may be needed.  
10. **Port mirroring / SPAN** — a feature that copies traffic from one port or VLAN to another port so analysts can inspect it with monitoring tools. 

### Reading resources
**Beginner**
- [Cloudflare Learning Center — What is a subnet?](https://www.cloudflare.com/learning/network-layer/what-is-a-subnet/) — a clear, beginner-friendly explanation of subnetting and subnet masks. 
- [Microsoft Learn — Understand TCP/IP addressing and subnetting basics](https://learn.microsoft.com/en-us/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting) — a practical intro to IP networks and subnetting concepts from an official source. 

**Technical**
- [Microsoft Learn — Guidance for troubleshooting TCP/IP communication](https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/troubleshoot-tcp-ip-communication-guidance) — a structured troubleshooting guide that shows how networking problems are diagnosed step by step. 
### Career insights
Networking is one of the foundations of almost every cybersecurity role, because alerts, logs, and traffic all depend on understanding how devices talk to each other.  
For SOC analysts, this room matters because many investigations begin with “What subnet is this on?”, “Where is the traffic going?”, or “Is the problem DNS, routing, or the host itself?” 
For security engineers, LAN segmentation concepts help when designing controls that reduce blast radius and make monitoring cleaner. 
For penetration testers, LAN behavior explains how discovery, routing, and local trust relationships can be abused or validated. 
The earlier this becomes second nature, the faster you move from guessing to evidence-based troubleshooting and defense.  

### Professional Tools
- **Wireshark (start early)** — an open-source packet analyzer that lets you capture and inspect traffic, which is ideal for learning what ARP, DHCP, and normal LAN communication look like. 
- **`ipconfig` (start early, especially for SOC)** — shows current TCP/IP settings and refreshes DHCP and DNS settings, making it one of the first commands worth learning on Windows.   
- **`nslookup` (start early, especially for SOC)** — diagnoses DNS infrastructure and helps you confirm whether name resolution is working as expected. 
- **`tracert` (start early)** — traces the path to a destination using ICMP and TTL, which helps separate local problems from upstream routing issues.
- **`arp` (start early)** — displays and modifies the ARP cache, which is useful when validating local IP-to-MAC behavior or checking for stale entries. 
- **`route` (start early once basics feel comfortable)** — displays and modifies the local IP routing table, which helps explain why traffic takes a particular path.
- **`netstat` (start early)** — shows active TCP connections, listening ports, Ethernet statistics, and routing information, which makes it useful for host triage.
- **`netsh` (start early on Windows-heavy paths)** — lets you view and modify network settings and troubleshoot issues locally or remotely, which is very handy in SOC and IT support work.
- **Nmap (use early in labs, after basics)** — a free and open-source tool for network discovery and security auditing, which helps you see what hosts and services are actually exposed.

### Learning path
This room sits in TryHackMe’s **Pre Security** path and builds the networking foundation that comes after broad “what is networking?” concepts.
It naturally leads into **OSI Model**, because LAN design, subnetting, ARP, and DHCP make more sense once you start mapping them to layers and protocols. 
In that sense, this room is the bridge between “I know what a network is” and “I can reason about how traffic actually moves on a local network.”
### Critical Operational Pitfalls
- **Treating a subnet as a security boundary by itself** — avoid this by pairing subnetting with VLANs, ACLs, routing controls, and monitoring.
- **Confusing broadcast domains with subnets** — avoid this by remembering that VLANs and broadcast boundaries are related but not identical to IP subnetting. 
- **Assuming ping proves full connectivity** — avoid this by checking DNS resolution, routing, and application-level behavior with `nslookup`, `tracert`, and logs.  
- **Ignoring stale or suspicious ARP state** — avoid this by checking the ARP cache and, in managed environments, protecting against ARP abuse with switch controls such as Dynamic ARP Inspection.  
- **Overlooking DHCP lease behavior and conflicts** — avoid this by remembering that DHCP can renew, reassign, and conflict-check addresses, so the current IP may not stay static. 
- **Forgetting to inspect the routing table before changing settings** — avoid this by checking routes first, especially when traffic seems to “disappear” between subnets.  
- **Capturing or analyzing traffic from the wrong point in the network** — avoid this by using port mirroring/SPAN or the right capture point so you see the packets that actually matter.  

### Prerequisites check
The main knowledge gaps to close next are subnet masks, CIDR notation, and how routing decisions are made for local versus remote destinations. 
It also helps to be comfortable with Windows command-line networking tools before moving on, especially `ipconfig`, `nslookup`, `tracert`, `arp`, and `netstat`. 
If OSI layer terminology still feels fuzzy, the next room on **OSI Model** is the right follow-up.  

---

**Methodology Note:** This section uses GPT-5.4 Thinking-Mini to provide a structured analysis of industry context, career pathways, and extended resources. Questions were formulated based on room content, and responses were validated against official documentation and industry sources.

**Generation Details:**
- Model: GPT-5.4 Thinking-Mini
- Date: 2026-04-11
- Prompt Framework: coming soon

---

## Next Steps
- I need to XXX
- I have to YYY
- Example:"" I am preparing everything for  [Cybersecurity 101 learning path](https://tryhackme.com/hacktivities?tab=paths) on TryHackMe ""

## My profiles
- TryHackMe: [EchoHound](https://tryhackme.com/p/EchoHound)
- GitHub: [micromediacoding](https://github.com/micromediacoding)
