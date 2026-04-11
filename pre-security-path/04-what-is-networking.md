# Room 4- What is Networking? - TryHackMe

**Completed:** xx April 2026  
**Difficulty:** Easy | **Time:** ~30min
**Room:** [What is Networking?](https://tryhackme.com/room/whatisnetworking)

**Spoiler warning** — This write-up contains **zero answers**.

---

## Overview

This room is a straightforward introduction to the very basics of networking. It explains what a network actually is, how the Internet is just a huge collection of smaller networks connected together, and how devices identify themselves using IP and MAC addresses. 

I went through all the tasks, answered the questions about public/private networks, ran the MAC spoofing lab, and did a few simple ping commands to see how ICMP works. 

I learned the difference between private and public IP addresses, why MAC addresses can be spoofed, and that ping is one of the most basic but useful tools for checking connectivity. It was a nice, calm way to start understanding networking fundamentals without jumping straight into complicated stuff. 

Overall I think this is a solid foundation before moving on to the Intro to LAN room.

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/04-what-is-networking-completion-badge.png)

---

## Personal, handwritten notes from the room (redacted - no answers visible)

**Task 1 - WHAT IS NETWORKING**
In this first task they explained the basic idea of what a network actually is. I learned that networks are just things connected together, whether it’s people, transport systems or computers. In computing it’s the same concept — devices linked so they can communicate and share stuff. It was a simple but clear start, showing how networks are everywhere in daily life.

**Task 2 - WHAT IS THE INTERNET**
Here they moved on to explain the Internet as one huge network made up of lots of smaller private networks joined together. I understood that Alice acts like a translator between friends who speak different languages, which is similar to how devices talk across networks. They also mentioned the history from ARPANET to Tim Berners-Lee creating the World Wide Web in 1989. It helped me see the difference between private and public networks.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/04-what-is-networking-task-2.png)

**TASK 3 - IDENTIFYING DEVICES ON A NETWORK**
This task covered how devices identify themselves on a network using IP addresses and MAC addresses. I learned that IP addresses can change and are like temporary labels, while MAC addresses are permanent like fingerprints and can even be spoofed. There was a practical lab where I had to spoof a MAC address to get access to the hotel Wi-Fi simulation. It was interesting to see how MAC spoofing works in real scenarios.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/04-what-is-networking-task-3.png)

**TASK 4 - PING (ICMP)**
In this part I learned about the ping tool and how it uses ICMP packets to test connections between devices. I ran a few ping commands on the target machine to check response times and confirm the connection. It was useful to see the basic syntax and what the output looks like. This is a simple but important tool I’ll definitely use a lot later.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/04-what-is-networking-task-4.png)

**TASK 5 - CONTINUE YOUR LEARNING: INTRO TO LAN**
The last task just pointed me to the next room called Intro to LAN to keep learning. It felt like a natural bridge to go deeper into local networks after the basics. Overall the whole room gave me a decent high-level understanding of networking fundamentals without overwhelming me. I think it was a good starting point before jumping into more technical stuff.

---

## Further Learning & Professional Context
*Supplemental analysis generated through AI-assisted research*

---

### Core Concepts
1. **Subnet** — a smaller, segmented part of a larger network that helps organize devices and reduce unnecessary traffic.
2. **Subnet mask** — the value used to separate the network part of an IP address from the host part so routers can forward traffic correctly.
3. **Default gateway** — the router a host uses when it needs to reach a device on another network.
4. **Router** — a device that connects networks and chooses where traffic should go between them.
5. **Switch** — a device that connects multiple devices inside a LAN so they can communicate with each other efficiently.
6. **DNS (Domain Name System)** — the service that translates human-readable names into IP addresses.
7. **DHCP (Dynamic Host Configuration Protocol)** — the protocol that automatically gives devices IP addresses and related settings such as subnet mask and default gateway.  
8. **NAT (Network Address Translation)** — the process of translating private IP addresses into public ones so a private network can reach the internet. 
9. **Bandwidth** — the maximum amount of data a network link can carry at a given time.
10. **Latency** — the time it takes for data to travel from one point on a network to another.  

### Reading resources
**Beginner**
- [Cloudflare Learning Center — What is a protocol?](https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/) — a simple, accurate introduction to how network communication rules work. 
- [Cloudflare Learning Center — What is DNS?](https://www.cloudflare.com/learning/dns/what-is-dns/) — a clear beginner explanation of how names become IP addresses.

**Technical**
- [Microsoft Learn — Guidance for troubleshooting TCP/IP communication](https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/troubleshoot-tcp-ip-communication-guidance) — a practical, official guide for diagnosing network connectivity problems step by step.

### Career insights
This room matters later because networking is the layer almost every security role depends on, from SOC work to cloud security and penetration testing.
When you can read subnets, gateways, DNS, and routing, security logs become much easier to interpret and investigate. 
It also helps you separate endpoint problems from network problems, which is a big part of incident triage and support escalation. 
For SOC analysts, this is especially useful because many alerts begin as “network weirdness” before anyone knows whether it is malicious or just broken connectivity.   
The better your networking basics, the faster you can move from guessing to evidence-based troubleshooting.
### Professional Tools
- **`ipconfig` (start early, especially for SOC)** — shows current TCP/IP settings and can refresh DHCP/DNS configuration, which makes it one of the first tools worth learning.  
- **`nslookup` (start early, especially for SOC)** — helps diagnose DNS infrastructure and confirm whether a domain is resolving the way you expect.   
- **`tracert` / `pathping` (start early)** — show the path to a destination and help reveal where latency or packet loss is happening along the route.  
- **`arp` (start early)** — displays and modifies the ARP cache, which is useful when you need to inspect local network resolution behavior. 
- **Wireshark (start early)** — a packet analyzer that lets you capture and inspect traffic in detail, which is excellent for learning how protocols really behave. 
- **`tcpdump` (start early if you use Linux)** — a command-line packet capture tool that is useful for fast, lightweight traffic inspection on Unix-like systems. 
- **`ping` (keep using early, but do not overtrust it)** — a basic reachability check, useful for quick verification but not enough to prove an application is healthy. 

### Learning path
This room fits into TryHackMe’s **Pre Security** path, which is meant to build core understanding of computers, networking, and the internet from the ground up.  
It comes right before deeper networking practice such as **Intro to LAN**, so it acts as the bridge from basic concepts to local-network structure and traffic flow.
That makes this room a foundation for the next networking rooms, and also for later blue-team or red-team work that depends on understanding how traffic actually moves.
### Critical Operational Pitfalls
- **Assuming ping means everything is fine** — avoid this by checking DNS, ports, routing, and application-level responses, not only ICMP reachability. 
- **Jumping straight to the internet when the issue is local** — avoid this by checking the host’s IP, gateway, and subnet first with tools like `ipconfig`.
- **Ignoring DNS failures** — avoid this by testing name resolution directly with `nslookup` before treating the problem as a generic connectivity issue. 
- **Forgetting route/path visibility** — avoid this by using `tracert` or `pathping` when the problem may be upstream or intermittent. 
- **Overlooking local resolution caches and tables** — avoid this by checking ARP and refreshing configuration when a device seems “connected” but still behaves strangely. 
- **Treating packet capture as optional** — avoid this by using Wireshark or `tcpdump` when you need proof of what actually traversed the network. 

### Prerequisites check
The main knowledge gaps to close next are subnetting, default gateways, DNS resolution, and the difference between local and routed traffic.  
It also helps to be comfortable with Windows command-line tools and basic packet-capture concepts before moving to the next networking room. 
If those ideas still feel fuzzy, **Intro to LAN** is the right next step. :contentReference[oaicite:36]{index=36}  

---

**Methodology Note:** This section uses GPT-5.4 Thinking-Mini to provide a structured analysis of industry context, career pathways, and extended resources. Questions were formulated based on room content, and responses were validated against official documentation and industry sources.

**Generation Details:**
- Model: GPT-5.4 Thinking-Mini
- Date: 2026-04-11
- Prompt Framework: coming soon



---

## Next Steps
- I need to definitely work around all the concepts and key definitions from this room
- Once I set up my future Home Lab, I will try to leverage this to train networking (local network, network monitoring etc.)

## My profiles
- TryHackMe: [EchoHound](https://tryhackme.com/p/EchoHound)
- GitHub: [micromediacoding](https://github.com/micromediacoding)

---

*Write-up style follows my repository philosophy.*
