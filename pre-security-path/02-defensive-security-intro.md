# Room 2- Defensive Security Introduction - TryHackMe

**Completed:** 23 March 2026  
**Difficulty:** Easy | **Time:** ~10–15 min  
**Room:** [Defensive Security Intro](https://tryhackme.com/room/offensivesecurityintro)

**Spoiler warning** — This write-up contains **zero answers**.

## Overview
This room is the defensive side of what we just did in Offensive Security Intro. It’s basically the other half of cybersecurity: instead of breaking stuff, I am the one trying to protect it. Short, clear, and a perfect follow-up to the first room - I get my hands on SOC dashboard simulator and I go through first very basic training scenarios.

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/02-defensive-security-completion-badge.png)

## Personal, handwritten notes from the room (redacted - no answers visible)
**Task 1 – THINK LIKE A DEFENDER**

Super simple start. They explain that defensive security has two main jobs:

A) Stop bad stuff from happening: "attack systems to find flaws."
B) When it does happen, detect it fast and respond properly: "detect and respond to attack."

Which team focuses on defensive security? Blue Team.
 
Red Team = attackers, Blue Team = defenders.




**Task 2 – DETECT SUSPICIOUS ACTIVITY**

This task breaks down the main areas of Blue Team work.

I start the SOC dashboard in a VM machine and I need to find which IP is generating suspicious traffic.

I really like how the dashboard looks and all the action that is taking place on the screen.

I got the IP, and I can proceed to the next task.

![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/02-defensive-security-task-2.png)



**Task 3 – IDENTIFY THE ATTACK**
Opened the monitoring dashboard and went straight to the “URL Discovery Attempts” list.
Looked at the latest entry and copied the URL the attacker was trying to reach.

The task was pretty straightforward. You see the logs and actually understand what the attacker is looking for. Good practice for real SOC work.

![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/02-defensive-security-task-3.png)

**Task 4 – STOP THE ATTACK**

Reviewed the security actions Joe had already done, then added the attacker’s IP to the firewall rule.

Simple but satisfying - just like this whole room.

Blocking the IP in real time felt like actually doing the job- kind of defensive actions that I want to be involved in the future.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/02-defensive-security-task-4.png)

---

## Further Learning & Professional Context
*Supplemental analysis generated through AI-assisted research*

---

### Core Concepts
1. **Alert triage** — the process of sorting and prioritizing alerts so analysts spend time on the most likely real incidents first.
2. **False positive** — an alert that matches a rule but turns out to be harmless activity rather than a real threat. 
3. **Baseline** — a model of normal activity used to make unusual behavior easier to detect.
4. **Indicator of Compromise (IOC)** — an artifact such as an IP address, domain, file hash, or URL that can help identify malicious activity.
5. **Log correlation** — combining related events from different sources to build a clearer picture of what happened during an incident.
6. **Enrichment** — adding context such as reputation, geolocation, or threat intelligence to raw alert data so investigators can judge impact faster. 
7. **Escalation** — handing a case to a senior analyst or another team when the evidence, severity, or scope goes beyond first-line handling.
8. **Incident response playbook** — a documented procedure for investigating and containing a known attack pattern in a consistent way.
9. **Packet capture (PCAP)** — recorded network traffic that analysts can inspect to understand what a host actually sent or received.
10. **Detection rule** — logic that turns observed behavior into an alert, often written in a portable format such as Sigma.

### Reading resources
**Beginner**
- [Microsoft Learn — Security operations overview](https://learn.microsoft.com/en-us/security/operations/overview): a clear introduction to SecOps and the Detect / Respond / Recover cycle.
- [CISA NICCS](https://niccs.cisa.gov/): an official cybersecurity training and career resource hub that is useful for exploring SOC-related learning paths and roles.
**Technical**
- [NIST SP 800-61 Rev. 2 — Computer Security Incident Handling Guide](https://csrc.nist.gov/pubs/sp/800/61/r2/final): the standard reference for incident handling, including preparation, detection, analysis, containment, eradication, and recovery.

### Career insights
This room matters later because SOC and DFIR work are built around the same loop: detect, investigate, contain, and document.
It also teaches the analyst mindset of turning raw logs into evidence, which is a core skill in threat hunting and incident response.
The earlier you become comfortable with alerts, indicators, and dashboards, the faster you can separate noise from a real attack.
That habit transfers directly into SOC roles, where speed, accuracy, and clean escalation all matter.
Later, the same thinking supports blue-team tooling, detection engineering, and continuous improvement of defenses.  

### Professional Tools
- **Microsoft Sentinel / SIEM (start early)** — a cloud-native SIEM that centralizes detection, investigation, response, and proactive hunting, making it one of the first tools a SOC analyst should learn.
- **Sysmon (start early)** — a Windows telemetry tool that records process creation, network connections, and file-related activity, which makes it extremely useful for host-based investigations.
- **Wireshark (start early)** — a packet analyzer used to inspect network traffic in detail, which helps beginners learn what “normal” and “suspicious” traffic look like.
- **Sigma (start early)** — an open detection rule format for log files that helps analysts write portable detections and think in rule logic rather than vendor-specific syntax. 
- **MITRE ATT&CK Navigator (start early)** — a web-based tool for visualizing defensive coverage and mapping activity to ATT&CK techniques.  
- **MISP (start early once IOC basics are clear)** — a threat-intelligence platform for collecting, storing, distributing, and sharing indicators and threat data.   
- **Suricata (after networking basics)** — an open-source network analysis and threat-detection engine that becomes more useful once you are comfortable with packets and protocols. 

### Learning path
This room sits in TryHackMe’s **Pre Security** path and acts as the bridge from general cybersecurity basics into defensive operations. 
The path sequence also places it after **Offensive Security Intro** and before **Careers in Cyber**, so it shifts the focus from attacking systems to defending them. 
TryHackMe also frames this room as the starting point for topics such as threat intelligence, SOC work, DFIR, malware analysis, and SIEM, so it is a gateway room rather than an isolated topic. 
That makes it a natural handoff from learning how attacks happen to learning how defenders observe, analyze, and stop them. 

### Critical Operational Pitfalls
- **Treating one suspicious IP as the whole story** — avoid this by correlating the IP with the user, host, time, alert history, and related telemetry before acting. 
- **Blocking or remediating before validating** — avoid this by confirming the alert with evidence and, when possible, following a playbook or escalation path first. 
- **Ignoring false positives** — avoid this by tuning detections and documenting benign patterns so analysts do not waste time on repeated noise.   
- **Forgetting to preserve evidence** — avoid this by saving logs, timelines, packets, and relevant artifacts before making disruptive changes whenever the situation allows. 
- **Poor documentation and handoff** — avoid this by recording what was seen, what was done, and why, so the next analyst can continue the case without guessing.  
- **Not using time carefully** — avoid this by normalizing timestamps and checking clock drift, because investigations often fail when events are compared without consistent time handling.  

### Prerequisites check
The main gaps to close next are network fundamentals, especially IPs, ports, DNS, and HTTP/HTTPS, because defensive monitoring makes much more sense when you can read traffic and logs comfortably. 
It also helps to understand the incident-handling lifecycle and the difference between an alert, an incident, and a false positive.  
A good next step is practicing with logs and basic packet captures until you can explain what happened without guessing. 

---

**Methodology Note:** This section uses GPT-5.4 Thinking-Mini to provide structured analysis of industry context, career pathways, and extended resources. Questions were formulated based on room content, and responses were validated against official documentation and industry sources.

**Generation Details:**
- Model: GPT-5.4 Thinking-Mini
- Date: 2026-04-11
- Prompt Framework: coming soon

---

## Next Steps
- I need to review Supplemental analysis that I prepared for this room to deepen my knowledge
- I want to find out what defensive cybersecurity tools and mindset I should implement at the beginning of my journey. I would really like to put my hands on some basic tools, like tools for monitoring network traffic in my device, or some other tools that I can use to train defensive cybersecurity abilities using my home rig
- I am already thinking about [CyberBlueSoc Home Lab](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/home-lab-preparation/CyberBlueSOC%20Your%20Blue%20Team%20Security%20Lab%20Installation%20%26%20User%20Guide.pdf)

## My profiles
- TryHackMe: [EchoHound](https://tryhackme.com/p/EchoHound)
- GitHub: [micromediacoding](https://github.com/micromediacoding)

---
