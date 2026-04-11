# Room 3- Careers in Cyber - TryHackMe

**Completed:** xx April 2026  
**Difficulty:** Easy | **Time:** ~30min
**Room:** [Careers in Cyber](https://tryhackme.com/room/careersincyber)

**Spoiler warning** — This write-up contains **zero answers**.

---

## Overview
This room is a short but solid intro to the different career paths in cybersecurity. It basically shows the two main sides — defensive (blue team) and offensive — and explains what a typical day looks like for a Security Analyst, Security Engineer, and Penetration Tester. I went through all five tasks, answered the questions about unfilled jobs, IDS systems, engagements, and even did the career quiz at the end. I learned that you don’t need a special background to start, there are over 3.5 million open positions, and each role has clear progression routes like moving from analyst to threat hunting or from pentesting to red teaming. It was useful to see how defensive roles (analyst/engineer) connect with the SOC and threat hunting direction I’m interested in, while pentesting gave me a better idea of the offensive side. Overall it’s a nice high-level overview before jumping into the more technical rooms.

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/03-careers-in-cyber-completion-badge.png)

---

## Personal, handwritten notes from the room (redacted - no answers visible)
**TASK 1 - INTRODUCTION**
In this first task they gave a quick intro to why cybersecurity is a good career choice. I learned there are over 3.5 million unfilled roles, the pay is decent even at entry level, and the field changes all the time so you keep learning. It also said you don’t need a special background – if you like solving problems and being curious you can fit somewhere. It felt like a nice easy start to the room.

**TASK 2 - SECURITY ANALYSIS**
This task explained what a Security Analyst actually does on the blue team. They monitor networks and devices, investigate alerts like weird logins from another country, and decide what needs to be done. I liked the example because it showed real-life situations they deal with. It also said this role is one of the most in-demand and you can later specialise in threat hunting or incident response.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/03-careers-in-cyber-task-2.png)
**TASK 3 - SECURITY ENGINEERING**
Here they described Security Engineers as the people who build and maintain the actual security systems. They gave a good example with the Intrusion Detection System (IDS) being like a security camera for the network. A typical day involves designing systems, keeping up with new hacker techniques, and documenting everything. It made me see how this role is more about creating the defences rather than just reacting to alerts.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/03-careers-in-cyber-task-3.png)
**TASK 4 - PENETRATION TESTING**
This one covered penetration testing, also called pentesting or ethical hacking. The tester tries to break into systems in a controlled way under an official engagement to find weaknesses before real attackers do. I learned they write reports and give advice on how to fix things. It also mentioned you can later move into red teaming which sounds more advanced and full-scale.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/03-careers-in-cyber-task-4.png)
**TASK 5 - INTERACTIVE: CAREER QUIZ**
The last task was a short interactive quiz to see which cybersecurity role might suit me. I clicked through it and it gave me "Incident Responder" as an output of my profile analysis. It was a simple way to wrap up the room and think about where I might fit in the future. Overall the whole room gave me a clear high-level picture of the main career paths without going too deep.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/pre-security-pathway/03-careers-in-cyber-task-5.png)

---

## Further Learning & Professional Context
*Supplemental analysis generated through AI-assisted research*

---

### Core Concepts
1. **Work role** — a defined area of cybersecurity work with clear responsibilities, used to describe what someone actually does in practice.
2. **Competency area** — a cluster of related knowledge and skills that supports performance in a particular cybersecurity domain.
3. **Proficiency level** — the expected depth of capability for a role, showing how much independence and judgment a person should have.
4. **Career pathway** — a structured route of roles and skills that helps someone grow from beginner to specialist.
5. **Skill gap** — the difference between current ability and the ability needed for a target role.
6. **Threat intelligence** — analyzed threat information that gives context for decision-making and defensive action.
7. **Log management** — the process of generating, transmitting, storing, analyzing, and disposing of log data.
8. **Incident response playbook** — a documented set of steps for handling a specific type of security event consistently.
9. **Vulnerability assessment** — the formal evaluation of weaknesses in a system so they can be prioritized and fixed.
10. **Risk assessment** — the process of identifying, estimating, and prioritizing risks so controls can be chosen wisely.

### Reading resources
**Beginner**
- [Getting Started with the NICE Framework](https://www.nist.gov/itl/applied-cybersecurity/nice/nice-framework-resource-center/getting-started) — a strong starting point for understanding how cyber work roles, knowledge, and skills fit together.
- [NICCS Home / Career Tools](https://niccs.cisa.gov/) — a practical government resource for exploring cybersecurity careers and planning next steps.

**Technical**
- [NIST SP 800-61 Rev. 3 — Incident Response Recommendations and Considerations](https://csrc.nist.gov/pubs/sp/800/61/r3/final) — the best technical reference here for understanding how incident response is organized and improved.

### Career insights
This room matters later because it helps you choose a direction based on how you like to work, not just on job titles.
The NICE framework vocabulary makes it easier to map learning to real jobs and to understand what employers actually expect.
It also reduces wasted effort by showing which skills belong to which role.
That matters early, because a good career plan saves time on random cert chasing and unfocused labs.
It gives you a cleaner starting point for deciding whether you fit best in analysis, engineering, or testing.

### Professional Tools
- **SIEM platforms like Microsoft Sentinel (start early, especially for SOC)** — central tools for collecting and correlating logs, and one of the first things a SOC analyst should learn because investigations usually start there.
- **Ticketing / case-management systems (start early, especially for SOC)** — tools such as ServiceNow or Jira help track alerts, evidence, actions, and handoffs in a clean workflow.
- **EDR platforms like Microsoft Defender for Endpoint (start early, especially for SOC)** — endpoint tools that help detect, investigate, and respond to suspicious activity on hosts.
- **Wireshark (start early)** — a packet analyzer that teaches you how network traffic actually looks and helps you understand suspicious connections.
- **MISP (start early once IOC basics are clear)** — a threat-intelligence platform for storing, sharing, and enriching indicators and threat data.
- **Security Onion (good early lab tool)** — a defensive monitoring stack that combines several blue-team capabilities and is useful for hands-on practice.
- **Burp Suite (start when you choose the pentesting path)** — a web testing toolkit that becomes important if you move toward application security or penetration testing.
- **Nmap (start early if you like hands-on technical work)** — a network discovery and auditing tool that helps you understand hosts, services, and exposure.
- **Nessus (start early if you are interested in vulnerability management)** — a vulnerability scanner that helps find weaknesses before attackers do.

### Learning path
This room comes after the introductory cybersecurity topics and before the more role-focused parts of the learning journey.
It works as a bridge from “how cyber works” to “which cyber job fits me.”
The next step is usually to choose a path such as Security Analyst, Penetration Tester, or Security Engineering and then build depth in that direction.
That makes this room a useful transition point rather than a deep technical module.

### Critical Operational Pitfalls
- **Choosing a role only because it sounds impressive** — avoid this by comparing the day-to-day work with your strengths and preferences.
- **Trying to learn every path at once** — avoid this by picking one primary direction first and adding breadth later.
- **Skipping fundamentals** — avoid this by keeping networking, operating systems, and logging basics in your study plan.
- **Ignoring communication skills** — avoid this by practicing clear notes, concise reporting, and calm handoffs.
- **Overvaluing certifications without hands-on practice** — avoid this by pairing study with labs, tools, and small projects.
- **Not revisiting career fit over time** — avoid this by checking whether your interests are moving toward analysis, engineering, or testing as you gain experience.

### Prerequisites check
The main knowledge gaps to close next are basic networking, operating system basics, and simple log reading.
It also helps to know the difference between blue-team, red-team, and defensive monitoring work.
A little familiarity with security terms like vulnerability, threat, and risk will make the next rooms easier to understand.
Hands-on practice with tools and real scenarios will matter more than memorizing job titles.

---

**Methodology Note:** This section uses GPT-5.4 Thinking-Mini to provide a structured analysis of industry context, career pathways, and extended resources. Questions were formulated based on room content, and responses were validated against official documentation and industry sources.

**Generation Details:**
- Model: GPT-5.4 Thinking-Mini
- Date: 2026-04-11
- Prompt Framework: coming soon

---

## Next Steps
- I will try to review potential cybersecurity career pathways and roles using normal Google research, AI-backed research, using models from websites like TryHackMe and taking advice of industry leaders into account
- Once I know a little bit more and I am closer to defining which career path I want to pursue, I will start to prepare my homelab towards activities related to this career path
- I found useful [Infosec beginner-friendly materials about career paths and job roles in Cybersecurity](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/reasearch/INFOSEC%20%20cybersecurity-career-paths.pdf) that I am gonna thoroughly review 

## My profiles
- TryHackMe: [EchoHound](https://tryhackme.com/p/EchoHound)
- GitHub: [micromediacoding](https://github.com/micromediacoding)

---

*Write-up style follows my repository philosophy.*
