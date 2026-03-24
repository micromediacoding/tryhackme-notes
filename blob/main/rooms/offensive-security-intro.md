# offensive-security-intro - TryHackMe

**Completed:** 23 March 2026  
**Difficulty:** Easy | **Time:** ~10–15 min  
**Room:** [Offensive Security Intro](https://tryhackme.com/room/offensivesecurityintro)

**Spoiler warning** — This write-up contains **zero answers**. It only describes the high-level steps and lessons learned.

## Overview
My very first TryHackMe room! I hacked a fake banking web app (FakeBank) in a safe, legal lab environment. The goal was to think like an ethical hacker, find a hidden weakness, and complete a task on the admin panel.

**Proof of Completion**  
![Room 100% completed](assets/images/offensive-security-intro/completion-badge.png)

## Screenshots (redacted - no answers visible)
![Task 1 & 2 - redacted](assets/images/offensive-security-intro/offensive-security-intro-task-1-2.png)

![Task 3 & 4 - redacted](assets/images/offensive-security-intro/offensive-security-intro-task-3-4.png)

## Walkthrough (no spoilers)
- Launched the FakeBank application in the browser.
- Used the terminal to run a directory brute-forcing tool (`dirb`) and discovered hidden pages (a very common real-world web vulnerability).
- Navigated to the newly found admin panel.
- Used the panel to perform an action that changed the account balance and triggered the success flag.

## What I Learned
- Offensive security means actively thinking like an attacker to find weaknesses **before** real hackers do.
- Many websites accidentally leave sensitive pages hidden — simple tools can find them instantly.
- Even basic web apps can have dangerous business-logic flaws (not just code bugs).
- Everything was done in a controlled TryHackMe lab — 100% legal and ethical.

## Tools Used
- `dirb` (directory brute-forcing)

## Next Steps
- Continue the Pre-Security learning path
- Move to Defensive Security Intro

## My profiles
- TryHackMe: [micro.media.coding](https://tryhackme.com/p/micro.media.coding)
- GitHub: [micromediacoding](https://github.com/micromediacoding)

---

*Write-up style follows my repository philosophy: reproducible, honest, and respectful to the community.*
