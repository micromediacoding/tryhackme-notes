# Room 31- Become a Defender - TryHackMe

**Completed:** xx April 2026  
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
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/30-become-a-hacker-completion-badge.png)

## Personal, handwritten notes from the room (redacted - no answers visible)
                             Task 1 - WHAT IS DEFENSIVE SECURITY?

Def Security focuses on preventing, detecting, and mitigating potential attacks via gaining visibility into systems, identifying weak points and ensuring system AVAILABILITY AND PROTECTION, which aligns with CIA Triad (Confidentiality, Integrity, Availability).

Defenders, often referred to as the Blue Team, need to understand how attackers think, what they target, and how attacks typically unfold.

 

                       Task 2 - UNDERSTANDING YOUR ENVIRONMENT


A) City Analogy

If defensive security were a building, it would translate to this picture:


1. What are you protecting (Systems and Infrastructure)?	
- Homes, buildings, people    ->  in Cyber Security it's client servers, data, workstations, users

2. Can you see what you are protecting (Visibility)?
- Cameras, reports, patrols	-> in Cyber Security, it's Logs, network traffic, alerts

3. What classifies suspicious behaviour?	
- Locked door attempts, circling cars	-> in CyberSec it's Repeated logins, unusual IP addresses

4. How do you stop a threat?	
- Police, blocked roads, curfews    -> in CyberSec it's Firewall rules, IP address blocking




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

https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/31-become-a-defender-task-2.png

Outcome: The task was very easy and didn't take more than 2 minutes. Good to "install" fundamentals in my mind. 




                       Task 3 - DEFENDING YOUR ENVIRONMENT

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

That task wasn't actually that easy - I made a couple of mistakes. Some of the abilities to choose sounded "similar", but they are not for similar tasks. That is where the confusion came from.

Of course, I finished the task succesfull but I will have to review the functions of certain parts of my potential ecosystem.

                               Task 4 - WHERE TO GO FROM HERE

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

Blue-team-red-team-definitions-tools-ecosystem

![Task 1 & 2 - redacted](../assets/images/offensive-security-intro/offensive-security-intro-task-1-2.png)

![Task 3 & 4 - redacted](../assets/images/offensive-security-intro/offensive-security-intro-task-3-4.png)


**Proof of Completion**  
![Room 100% completed](../assets/images/offensive-security-intro/completion-badge.png)


## Walkthrough (no spoilers)
- Launched the FakeBank application in the browser.
- Used the terminal to run `dirb` and discovered hidden pages.
- Navigated to the newly found admin panel.
- Performed an action that triggered the success flag.

## What I Learned
- Offensive security = thinking like an attacker to find weaknesses first.
- Hidden pages are a real vulnerability.
- Even simple apps can have dangerous business-logic flaws.
- Everything here is 100% legal in a TryHackMe lab.

## Tools Used
- `dirb` (directory brute-forcing)

## Next Steps
- Continue Pre-Security path
- Move to Defensive Security Intro

## My profiles
- TryHackMe: [micro.media.coding](https://tryhackme.com/p/micro.media.coding)
- GitHub: [micromediacoding](https://github.com/micromediacoding)

---

*Write-up style follows my repository philosophy.*
