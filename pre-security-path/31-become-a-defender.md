# Room 31- Become a Defender - TryHackMe

**Completed:** 14 April 2026  
**Difficulty:** Easy | **Time:** ~30-60min
**Room:** [Become a Defender](https://tryhackme.com/room/becomeadefender)

**Spoiler warning** — This write-up contains **zero answers**.

## Overview
This was my final room in the Pre-Security learning path and, honestly, one of the most enjoyable and eye-opening modules I have completed on TryHackMe.

“Become a Defender” gave me a clear, practical introduction to defensive (Blue Team) security, showing how defenders focus on prevention, detection, mitigation, analysis, and continuous improvement while always thinking like an attacker.

Using the city analogy made everything "click" — I now better understand visibility, layered defenses, and how every part of an organization’s ecosystem (devices, servers, firewall, mail, etc.) must be protected.

The hands-on mapping and tool-placement tasks in the VM were simple yet surprisingly insightful, reinforcing the defender mindset of threat anticipation, risk prioritization, and constant adaptation.

As the last room of the entire path, it perfectly capped everything I learned: I gained massive knowledge, sharpened my skills, and — most importantly — truly enjoyed the journey.

Combined with my recent Coursera specialization “Cyber Security in the AI Era,” I finally see the broader picture as a beginner and feel excited to keep exploring the “hidden parts of the map.”

Purchasing a yearly subscription on TryHackMe was probably one of the best investments I’ve ever made. ⛳🚀


**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/31-become-a-defender-completion-badge.png)

## Personal, handwritten notes from the room (redacted - no answers visible)

**Task 1 - WHAT IS DEFENSIVE SECURITY?**

Def Security focuses on preventing, detecting, and mitigating potential attacks via gaining visibility into systems, identifying weak points and ensuring system AVAILABILITY AND PROTECTION, which aligns with CIA Triad (Confidentiality, Integrity, Availability).

Defenders, often referred to as the Blue Team, need to understand how attackers think, what they target, and how attacks typically unfold.

 

#**Task 2 - UNDERSTANDING YOUR ENVIRONMENT**


A) City Analogy

If defensive security were a building, it would translate to this picture:


1. What are you protecting (Systems and Infrastructure)?	
- Homes, buildings, people    ->  in Cyber Security, it's client servers, data, workstations, users

2. Can you see what you are protecting (Visibility)?
- Cameras, reports, patrols	-> in Cyber Security, it's Logs, network traffic, alerts

3. What classifies suspicious behaviour?	
- Locked door attempts, circling cars	-> in CyberSec, it's repeated logins, unusual IP addresses

4. How do you stop a threat?	
- Police, blocked roads, curfews    -> in CyberSec, it's Firewall rules, IP address blocking




B) What Can I Do as a Defender?

Once I understand the systems and how to protect them I should organize my work around foundational security concepts that applies to nearly all IT enviroments:

1)  Prevention: 
-  Putting security controls in place to stop attacks before they happen, such as firewalls, antivirus software, and regular patching.


2) Detection: 
-  Monitoring systems and networks to identify suspicious or malicious activity through logs, alerts, and security tools.


3) Mitigation: 
-  Taking action during an incident to limit damage, such as blocking traffic, isolating affected systems, or disabling compromised accounts.


4) Analysis: 
-  Investigating what happened, how it happened, and which systems were affected by reviewing logs and other evidence.


5) Response and Improvement: 
-  Recovering from the incident and improving defenses to reduce the risk of similar attacks in the future.



C) What is my scope?

Defenders don't protect the whole internet, but their focus is on their org or client - it includes devices used every day, APPs and Data host servers and networks.

Before creating a defence ecosystem and strategy, I have to understand existing systems and how they fit into the overall environment. 

If we would like to use CITY ANALOGY, our client or our system would be described as follows:


1) Employee Devices: 	
- Where users work and access company resources 
- Homes

2) Web Server	
- Hosts websites or applications accessed by users	
- Shop/Public buildings

3) Mail Server	
- Sends and receives email for the organisation	
- Post office

4) Firewall	
- Controls what traffic is allowed in or out	
- City gate

5) Internet	
- External networks not controlled by the organisation	
- Anything outside of the city




D) Mapping My City

In a VM, in this part of the room, I will explore a city that represents my client ecosystem, and I will have to investigate and map it.

![Task 2 - redacted](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/31-become-a-defender-task-2.png)

Outcome: The task was very easy and didn't take more than 2 minutes. Good to "install" fundamentals in my mind. 




**Task 3 - DEFENDING YOUR ENVIRONMENT**

A) The Defender Mindset

In order to be successful in blue team security, I need to not only UNDERSTAND MY SYSTEM but also UNDERSTAND THE ATTACKER AND THINK LIKE THEM.

I need to look at my system not as a single entity, but a chain of connected entities that a hacker wants to exploit by pivoting from one to another.

For example, a compromised email of one co-worker can lead to a breach into the company's systems and network, which will lead to a cascading effect and more damage done. 



KEY DEFENDER PRINCIPLES are:

1) Threat anticipation: 
-  Review the systems you aim to protect and ask, "What if?" Imagine realistic paths an attacker may take to achieve their goal.

2) Attack awareness: 
-  Attacks typically follow recognisable stages. Studying common attack chains and frameworks is incredibly useful for defenders.

3) Risk prioritization: 
-  Not every part of your system carries equal risk. Defenders should identify high-value systems and targets.

4) Continuous adaptation: 
-  Defense is not a one-time set-up. Threats and attackers evolve, techniques change, and vulnerabilities emerge.



B) Available Defenses: Tools to Protect Your City

Defenders use various spectrum of tools to protect systems from threat actors. No single tool can protect us entirely, but a LAYERED DEFENSE SYSTEM.
Using city analogy, this is how protecting system (in very basic way) looks like:


1) Employee Devices	
-  What could go wrong? - Someone clicks a bad link or downloads unsafe software	
-  What can we do? - Antivirus to detect bad programs, regular software updates

2) Web Server	
-  What could go wrong? - Attackers try to break into the website	
-  What can we do? 0 Only allow safe traffic, Use secure communication                     

3) Mail Server	
-  What could go wrong? - Malicious or deceptive emails	
-  What can we do? - Spam filters, Scan attachments

4) Firewall	
-  What could go wrong? - Strangers from the internet try to break in	
- What can we do? - Firewall rules that control access, Block known troublemakers

5) The Outside Internet	
-  What could go wrong? - External threats come from here	
-  What can we do? - Restrict inbound traffic, Monitor for suspicious activity


C) Defending Your City

I am now told to open a VM, which I do -in this scenario, I need to drag "which tools" protect or are responsible for which part of my ecosystem (city). I try to defend my/client system using available tools.

![Task 3 - redacted](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/31-become-a-defender-task-3.png)

Outcome: That task wasn't actually that easy - I made a couple of mistakes. Some of the abilities to choose sounded "similar", but they are not for similar tasks. That is where the confusion came from.

Of course, I finished the task succesfull but I will have to review the functions of certain parts of my potential ecosystem.



**Task 4 - WHERE TO GO FROM HERE?**

That was incredibly engaging and fun module. I enjoyed it a lot. I will review it again. This is key terminology:

1) Key Terminology
- Blue Team: A group of cyber security defenders tasked with protecting systems and responding to threats
- Client Infrastructure: The networks, servers, devices, and applications belonging to an organization that need protection
- Visibility: The ability to see and monitor activity across systems to spot potential issues
- Threat: A potential danger, such as a hacker or malware, that could harm systems or data
- Prevention: Stopping threats before they can cause harm by blocking, restricting, or reducing opportunities for attack
- Detection: The process of identifying threats or suspicious activity in networks and systems
- Mitigation: Actions taken to reduce or stop the impact of a threat once it's identified
- Risk: The likelihood and potential impact of a threat successfully harming an organization

This was my last room - what an incredible journey it was. I think it may be one of the best ways to spend money I have ever spent in my life.
I gained a massive amount of knowledge, I raised my skills and capacities but most importantly, I enjoyed what I was doing, and I enjoyed learning all the things that I learned during this learning pathway.

Together with a freshly finished professional specialisation course on Coursera - Cyber Security in the AI Era by the University of Maryland, I start to see the broader picture, at least as much as a beginner can see.
I love to analyse systems, events, decisions and mechanisms, and the way everything works in a bigger picture - thanks to this pathway from TryHackMe, I can "see" more - "hidden part of the map" was explored - I am excited to see even more and expand my knowledge and skillset!! ⛳🚀

I prepared the whole document to help me learn more about red team/blue team cybersecurity. It has a list of 30 critical definitions, websites with the best articles to learn basic concepts of defensive and offensive security and a list of the most used tools in cybersecurity for many fields of cybersecurity, like system scanning, system defence, penetration testing, etc.

It will be uploaded to my TryHackMe GitHub repo in PDF version, under the name:

[Blue Team - Red Team - Research Analysis](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/reasearch/blue_red_team_research_analysis.md)

## Further Learning & Professional Context
*Supplemental analysis generated through AI-assisted research*

---

### Core Concepts
1. **Alert triage** — the process of sorting and prioritizing alerts so analysts spend time on the most likely real incidents first.
2. **False positive** — an alert or detection that matches a rule but turns out to be harmless activity, which is common in security monitoring.
3. **Baseline** — a model of normal behavior used to make unusual behavior easier to notice in logs and detections.
4. **Indicator of Compromise (IOC)** — an artifact such as an IP address, domain, file hash, or URL that can help identify malicious activity.
5. **Log correlation** — combining related events from different sources to build a clearer picture of what happened during an incident.
6. **Enrichment** — adding context such as reputation, geolocation, asset ownership, or threat intelligence to raw alert data.
7. **Escalation** — handing a case to a more senior analyst or another team when the evidence or impact goes beyond normal first-line handling.
8. **Incident response playbook** — a documented procedure that tells analysts how to investigate and respond consistently to a specific type of alert or incident.
9. **Packet capture (PCAP)** — recorded network traffic that analysts can inspect to understand what a host actually sent or received.
10. **Detection rule** — logic that turns observed behavior into an alert, often expressed in a SIEM-friendly format such as Sigma.

### Reading resources
**Beginner**
- [Microsoft Learn — Security operations overview](https://learn.microsoft.com/en-us/security/operations/overview): a clear introduction to how SecOps detects, responds, and recovers during active attacks.
- [CISA NICCS](https://niccs.cisa.gov/): an official cybersecurity training and career resource hub that is useful for exploring SOC-related learning paths and roles.

**Technical**
- [NIST SP 800-61 Rev. 2 — Computer Security Incident Handling Guide](https://csrc.nist.gov/pubs/sp/800/61/r2/final): the standard reference for incident handling, including preparation, detection, analysis, containment, eradication, and recovery.

### Career insights
This room matters later because SOC and DFIR work are built around the same loop: detect, investigate, contain, and document.  
It also teaches the analyst mindset of turning raw logs into evidence, which is a core skill in threat hunting and incident response.  
The earlier you become comfortable with alerts, indicators, and dashboards, the faster you can separate noise from a real attack.  
That habit transfers directly into SOC roles, where speed and accuracy both matter.  
Later, the same thinking supports blue-team tooling, detection engineering, and continuous improvement of defenses.

### Professional Tools
- **SIEM platforms like Microsoft Sentinel (start early)** — SIEMs collect and correlate logs across systems, and they are one of the first tools a SOC analyst should learn because most investigations begin in a SIEM.
- **Sysmon (start early)** — a Windows telemetry tool that records process creation, network connections, and file-change events, which makes it extremely useful for early host-based investigations.
- **Wireshark (start early)** — a packet analyzer used to inspect network traffic at a detailed level, which helps beginners learn what “normal” and “suspicious” traffic look like.
- **Sigma (start early)** — an open detection rule format for log files that helps analysts write portable detections and think in rule logic rather than vendor-specific syntax.
- **MITRE ATT&CK Navigator (start early)** — a visualization tool for mapping detections and coverage to ATT&CK techniques, which is great for learning how attacks are categorized.
- **MISP (start early once IOC basics are clear)** — a threat-intelligence platform for collecting and sharing indicators and threat data, which becomes useful as soon as you start working with IOCs regularly.
- **Suricata (after networking basics)** — an open-source network threat detection engine that helps you detect and inspect suspicious traffic once you are comfortable with packets and protocols.

### Learning path
This room sits in TryHackMe’s **Pre Security** path and acts as the bridge from general cybersecurity basics into defensive operations.  
TryHackMe also positions it as the starting point for topics such as threat intelligence, SOC work, DFIR, malware analysis, and SIEM, so it is a gateway room rather than an isolated topic.

### Prerequisites check
The main gaps to close next are network fundamentals, especially IPs, ports, DNS, and HTTP/HTTPS, because defensive monitoring makes much more sense when you can read traffic and logs comfortably.  
It also helps to understand the incident-handling lifecycle and the difference between an alert, an incident, and a false positive.  
A good next step is practicing with logs and basic packet captures until you can explain what happened without guessing.

---

**Methodology Note:** This section uses GPT-5.4 Thinking-Mini to provide structured analysis of industry context, career pathways, and extended resources. Questions were formulated based on room content, and responses were validated against official documentation and industry sources.

**Generation Details:**
- Model: GPT-5.4 Thinking-Mini
- Date: 2026-04-10
- Prompt Framework: coming soon

---

## Next Steps
- I need to review the whole learning path and then book & pass the Sec0 Exam
- I am preparing everything for successfull start of  [Cybersecurity 101 learning path](https://tryhackme.com/hacktivities?tab=paths) on TryHackMe (I downloaded Joplin and Obsidian for notes, I am doing research about setting up your first home lab)
- I am preparing a template MD which I will use to create write-ups (room reports like this one) on regular basis, right after I finish a room (So far, I have been taking notes from the entire learning path and I am currently uploading them, but it takes a huge amount of time and I have to make a lot of corrections, the md template with ready-made headers which I will only supplement with content will improve the entire process and minimize wasted time).
- Part of my Room write-ups will be supplemental analysis generated through AI-assisted research (paragraph "Further Learning & Professional Context") related to the room that will be meant to support my learning process. I prepared a prompt that, in my opinion, is well structured to provide a user-friendly analysis of the studied topic.

## My profiles
- TryHackMe: [EchoHound](https://tryhackme.com/p/EchoHound)
- GitHub: [micromediacoding](https://github.com/micromediacoding)

---

*Write-up style follows my repository philosophy.*
