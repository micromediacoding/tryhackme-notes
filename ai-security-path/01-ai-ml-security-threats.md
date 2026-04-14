# Room 1- AI/ML Security Threats - TryHackMe
[🔗](https://tryhackme.com/room/aimlsecuritythreats)

**Started:** 23:31, 13 April
**Completed:** 11:58, 14 April 2026  
**Difficulty:** Easy | **Time:** ~60min
**Room:** [AI/ML Security Threats](https://tryhackme.com/room/aimlsecuritythreats)

**Spoiler warning** — This write-up contains **zero answers**.

---
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/ai-security-pathway/01-ai-ml-security-threats-completion-badge.png)
---

## Overview
This room is all about AI and Machine Learning in the context of cybersecurity - both how attackers are already using it and how defenders can fight back with it. I went through every task, read the explanations, answered the questions, and completed the practical section where I used the TryHackMe AI assistant to analyse logs, detect phishing, generate threat hunting ideas and create regex patterns. 

I learned the full chain from basic AI definitions through ML, Deep Learning, neural networks and LLMs all the way to real-world threats like prompt injection, data poisoning and deepfakes. The room also covered defensive AI, the IBM Cost of a Data Breach Report, and why companies that adopt AI security save serious money. 

Overall it gave me a clear picture of how fast this field is moving and why I need to understand both sides if I want to work in threat hunting or defensive security.

Here’s what stood out for me:

- AI is the broad field of machines doing human-like tasks, while Machine Learning is the subset where models learn from data without explicit programming. -
- Deep Learning is a more advanced form of ML that uses neural networks and can handle massive unlabelled datasets on its own. -
- LLMs like GPT are built on transformer neural networks and use techniques like attention and RLHF to generate human-like text. - 
- Attackers can abuse AI through prompt injection, data poisoning, model theft, model drift and privacy leakage. -
- AI can also enhance traditional attacks - generating better malware, deepfakes for social engineering, or more convincing phishing emails. -
- On the defensive side, AI is already being used for anomaly detection, automated triage, log analysis and faster incident response (tools like Splunk, Microsoft Defender, CrowdStrike and SentinelOne were mentioned). -
- The room stressed that we need to secure our own AI models with RBAC, encryption, monitoring and standards like ISO/IEC 27090. -

This room wasn’t overly technical, but it connected a lot of dots, at least for me. I think it’s a really useful high-level overview before I start diving deeper into practical AI security labs.

Since I have been leveraging the capabilities of several AIs for months now - including using 5 AIs simultaneously every day - Grok, ChatGPT, Perplexity, Gemini and Antropic to chain their research - it seems to me that knowledge from this pathway may be crucial for me, even critical, considering the direction of technological development and the development of events in the world.

It also reinforced why I want to focus on defensive cybersecurity - the defensive potential of AI looks massive if done right. I saved the full interaction with the TryHackMe AI from the practical task as a PDF and added it to the repo.

---

## Personal, handwritten notes from the room (redacted - no answers visible)

**Task 1 - INTRODUCTION**

The world around us is quickly changing, and the implementation of AI in our lives will require a lot of adaptation from every industry.
New models of AI are being developed at a rapid pace and will require new approaches and methodologies from the cybersecurity industry, too.

TryHackMe informs that in this module, I will learn:

A. What is AI/ Machine Learning (ML)?

B. How can it be used in our industry?

C. How will it affect my role?

D. How is AI being leveraged by Attackers?

They emphasize that the room is intended to be an entry point to the AI topic, and the learning objectives will be:

-  Understanding AI, ML, and their impact on the cybersecurity industry.

-  Understanding Deep Learning (DL) and neural networks, and how they have made the applications of AI, we see today, possible. 

-  Understanding how adversaries use AI to enhance existing attacks and take. Advantages of AI Model vulnerabilities.

-  Understanding the key role AI will play in defending against AI.



**Task 2 - THE BUILDING BLOCKS OF AI**

1. What is Artificial Intelligence?

A term refers to computer system or machine that is able to carry tasks independently, task that would need human reasoning, comprehension, creativity or problem solving.
The terms is broad, it dates back to 1950 and at this point of technological advancement it's not longer just a simple definition.

2. Machine Learning.

One of the most significant advancements in AI came with ML - Machine Learning - which is computers ability to learn data without given instructions, comparable to humans brain. Over the time, algorithms got better.

In short the process of machine learning looks like this:

Defining Problem -> Data Collection -> Algorithm Selection + Model -> Data Cleaning -> Feature Engineering -> Model Evaluation + Training -> Model Deployment -> Model Monitoring

I will try to memoraize this cycle, although with amount of DATA I HAVE TO store at the moment😅 it may be tought.


3. Machine Learning Algorithms

ML algorithms are methods used to learn patterns from data and ML models a trained results/outputs of these algorithms.

Algorithms consist 3 key commponents:

A) Decision process,
B) Model Optimisation Process
C) An Error Function


Algorithms fall into four main categories:

A) Supervised learning - depends on LABELED DATA to train models for classification and regression tasks like house price predicition or spam email identification

B) Unsupervised - works with unlabeled datato discover hidden patterns

C) Semi-supervised - combines elements of Supervised and unsupervised

D) Reinforcement learning - mimics human learning (rewards for correct decision, punishment/penalty for wrong one) allowing AI to refine its actions over time to achieve the best outcome.



4. NEURAL NETWORKS AND DEEP LEARNING

Neural Networks are attempt to enable computers to think like humans by mimicig how human brain works and to mimic human reasoning.

So:
A) Brain process info through interconnected neurons
B) Neurons uses synapses to communicate - they are connections
C) The network of neurons learns by adjusting the strength of these connections


THM presents a diagram that represents AI type of neural network with:

A) Input layer - receives raw data
B) Hidden layer - processes and refines the input data
C) Output layer - produces the final prediction

Each connection has a weight, detrmining it's importance (for example in email body text may have more importance than subject).


Deep Learning and Machine Learning are often confused, but the main difference is that Machine Learning works on labelled data and Deep Learning can take labelled or unlabelled datasets, the algorithm decides which data to use and therefore produces output without human intervention.

DL is possible through leveraging neural networks and grinding through large unlabelled datasets of it's choice.

Some people considered it "scalable ML".

The idea of neural networks has been around for decades but it's rapid technological advancement and mass digitization of information in recent years that lead to such a progress in Ai capabilities.

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/ai-security-pathway/01-ai-ml-security-threats-task-2.png)


**Task 3 - LLMs**

Introduction of ML -> Introduction of DL and neural networks -> Large Language Modules (LLM's) come into play.

ChatGPT was a main trigger of that progress - it has the ability to generate human-like text responses to human queries begin a new era in technology and new race - who is gonna develop best AI?

LLMs are DL based AI models the generate output based in the input, actively predicting next word in a sequence. So what happens when I query chat bot, for example:

"Sometimes I think AI may outsmart ...."

This quote would be fed into LLM and the model will try to predict the final word - in this case the final word may be "rat" or "dolphin" or "orca" but probably (I am not LLM) the right final word in that case will be "humans", for vast amount of reasons that AI will be able to process in split of a second thanks to immerse processing capabilities and access to infinite-like amount of data in relation to human being. 


LLMs are first trained in pre-training phase where they process vast amount text, like GPT-3 which was pre-trained with amount of text THAT WOULD TAKE HUMAN 2600 YEARS OF NON-STOP READING.

GPT-4 was fed with even more amount of data and empowered by DL.

LLMs leverage DL methodology - they process vast amount of unlabelled data, using BILLIONS OF PARAMETERS in short amount of time enabling them to understand and generate human-like output.

These PARAMETERS are fined-tuned automatically as the model processes text, while adjusting based on predicition accuracy to improves its own response quality.
Model beings by generating random word to finish the text, for example:

"Sometimes I think AI may outsmart STONE"

The guess is then compared with what final word actually was, and the parameters are fine-tuned to make possible to predict what was the right word, until the model can accurately predict the correct word to end the sentence (and less likely to choose the incorrect words) using an algorithm called backpropagation:

Sometimes I think AI may outsmart...

[possible outputs, example]
1. Humans (65%)
2. Killer whales (15%)
3. Dolphins (10%)
4. Chimpanzees (5%)
5. Octopuses (3%)
6. Wolves (2%)


At the current stage of technological advancement, when we querry to LLM, this process may be happening trillions of times, over and over, until it cannot only predict the end of training data but also raw unseen data.
Advancement of hardware, especially the latest advancement of GPU, make this process possible through enabling masses of parallel operations of massive datasets while using advanced neutral networks, specifically type of networks that are called TRANSFORMER NEURAL NETWORKS.                      

2017s Google publication "Attention is all you need" (I need to find the original and upload it to my github as well as some analysis of that document done by cybersecurity and IT experts) introduced transformer neural networks which enabled to processing parallel text instead of word-by-word analysis.

This model improved CONTEXTUAL UNDERSTANDING, thanks to ability to assign "attention" to key words by encoding them into numerical values and calculating "attention" scores. It greatly improved the accuracy of the models helping them in the interpretation of ambiguous references, like distinguishing whether "it" in this sentence refers to "the dealer" or "the car".

The dealer approved the car purchase, it was financially stable.

After pre-training, humans add a step called REINFORCEMENT LEARNING FROM HUMAN FEEDBACK.
In this step, model review the predictions and any that would be considered unhelpful by a us or have issues are flagged and the parameters are adjusted accordingly in a real time.

Once trained and reinforced, model can be used in various task, like translating, chatbot, calculator - model constantly tries to predict next word as a response, and so on, until the user has complete response.

LLMS are powering generative AI (ChatGPT and LLaMA), which can create various content not only text like images and music but those results are possible thanks to years of research and innovation, not instant development.


Key concepts of this room were:

A) Artificial Intelligence (AI) constitutes the comprehensive discipline that includes every system designed to replicate human intelligence. 

B) Machine learning (ML) serves as a core subset of AI, enabling it to identify and learn patterns directly from data without requiring explicit programming instructions. 

C) Deep learning (DL) represents a more advanced and focused subset of machine learning that employs neural networks to analyze massive datasets through intricate, layered processes entirely autonomously, functioning in essence as a highly scalable evolution of machine learning. 


D) Large Language Models (LLMs), such as those exemplified by GPT, are sophisticated deep learning architectures constructed on neural networks - specifically transformer models -engineered to comprehend and generate text that closely mirrors human language.


This room was brilliant! The concepts and definitions that I need to reinforce:

AI, ML, DL, RLHF, LLM, LLaMA, ML algorithm, Machine learning lifecycle, scalable ML, AI pre-training, neural networks, transformer neural networks, 



**Task 4 - AI SECURITY THREATS**

In this room I will be introduced to how threat actors use AI - from methodology to tools.

MITRE ATT&CK Framework will be helpful here and thanks to what I learned during course "Cybersecurity in AI era" by Uni of Meryland on Coursera, I know the basics and how to navigte it.

1) VULNERABILITIES IN AI MODELS

- Prompt Injections - prompts are used to instruct models and a prompt injection happens when threat actors ovverride original model with their own instructions for malicious purposes such a generating harmful content or accessing/disclosing information it shoudln't

- Data poisoning - occurs when threat actors manipulate corpus/training data used to train AI, for example, they could mainpulate training data used to train AI so it will fail to recognise spam emails, allowing email to bypass AI filter

- Model Theft - happens when threat actors get access to AI model (by querying the API of the ML model they want to steal) which they could use or steal. They could use output to create a clone with similar features to original

- Privacy Leakage - happens when we deal with the possible revealing of sensitive information (possibly confidential) by AI model to third parties - example may be leak by AI dealing with private medical data of patients

- Model Drift - is a potential scenario in which a model's performance drifts over time due to changes in environment or data. Monitoring AI is very important in that case



2) Enhanced Attacks

- Malware - with capabilities of generative AI devs can generate code instantly - so as threat actors, which leads to possible instant malware generation, which simplifies task for attackers.

- DeepFakes - generates authentication problems. THM pitches a scenario in which secretary recieves a video of her superior/boss telling her to disclose confidential information - in pre-AI era it would be almost sure that HER BOSS FROM VIDEO IS ACTUALLY HER BOSS, but nowadays, thanks to deepfake, someone can generate a video with her human that will look, sound and behave like the her superior which may leads to disclousure of confidential data. Another example they give are deepfake video interviews which leads to fake job offers.

- Phishing - remains one of the most common initial access methods used by attackers. It involves deceptive emails that appear legitimate, but they contain malicious content designed to exploit users. Companies have long trained their workforce to spot "red flags" such as suspicious links and grammatical errors, which often arise from mass production or non-native English. This education has improved detection rates over time. 
However, generative AI now lets attackers create detailed, fluent, and personalized phishing emails with almost zero effort, regardless of their writing capabilities.
Because of that, these messages have become significantly harder to identify through instinct alone - they are just to perfect, and sometimes perfect means "imperfectly perfect".

Models like GPT include safeguards against generating malicious content such as phishing emails or malware but attackers frequently bypass them using prompt engineering.


This was another great room - it's 3:30 at night and I would really love to continue but I must sleep in order to... continue tomorrow.

Key concepts and definitions I need to revise later:
- MITRE ATLAS Matrix
- Vulnerabilities in AI Models (data poisoning, model theft, privacy leakage, model drift, prompt injection and more
- enhanced attacks (malware, phishing, deepfakes)

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/ai-security-pathway/01-ai-ml-security-threats-task-4.png)


**Task 5 - DEFENSIVE AI**


1. IBM Cost of Data Breach Report.

AI used by threat actors became a significant offense tools - but luckily - "the good side" can also leverage power of AI in defensive cybersecurity.

Last years, IBM's "Cost of a Data Breach Report 2025 - The AI Oversight Gap" not only suggested, but proved that companies that impelemented defensive AI saved $2.2 million dolar in expenses due to data breach.

Reports emphasizes that average cost of data breach is $4.88 million and the time it takes to IDENTIFY and CONTAIN the breach in terms of AI adaptation was reduced by 108.

Report clearly suggests that companies should embrace AI.


2. Our Ability to analyse

AI is perfect in large data analysis and it should be leverage to do it.

It specializes in recognizing and contecting the patterns - which is perfect tool for defensive cybersecurity. Network traffic analysing is a perfect examples, where the task is to analyse large quanities of data in a real time and find anomalies - AI does it perfectly.

Examples of such a products that already exist on market are SPLUNK and MICROSOFT DEFENDER - I just also research additional names like CrowdStrike Falcon, SentinelOne Singularity, Darktrace - they will be added to post analysis of this room.


3. Our ability to predict.

AI is perfect at - if we look at automation as a sequence of "if-then" we start to understand it may be so useful in defensive cybersecurity.

For example, during code development, thanks to field called DevSecOps (is a role that ensures that right security methodology is integrated from early stage).

Example of such an automation by THM is "if code is pushed to main, then trigger this pipeline".

Another example is - thanks to AI ability to predict and recognize patterns, we can recognize PHISHING EMAILs easier to tackle hackers that try to use AI TO WRITE PHISHING EMAIL.


4. Our ability to summarise/digest.

Thank to power of AI we can aquire and analyse large quantities of data faster, provide incident report and other essential artifacts faster and in more effective way.

In pratice, 1000 of pages of report can be analysed by AI within seconds/minutes.


5. Our ability to investigate

We can feed AI with logs and identifitty what is going, what is the issue, and how to tackle it - basically AI is helping us with INCIDENT TRIAGE.
For example, it can thing about potential avenues attackers would take that we wouldn't have thought of.


6. SECURE AI.

We need to remember about securing our AI models - there should be security measures implemented at every stage of the process - from development to servicing clients online.

IBM report mentions that only 24% of GenAi are secured - this is very dangerous situation, because if we don't secure our AI and it gets into hands of threat actors that can use it vast capabilities and turn it against us.

Ways to maintain safe envirotment for our AI:

- Securing AI Models - which is general terms that covers for example preventing unathorized access, use of RBAC (Role-Based Access Control and MFA (Multi-Factor Authentication)

- Privacy Protection - training data (sensitive very often) should be protected it's encrypted

- Implementation of AI Security standards - implementing frameworks and security standard like ISO/IEC 27090 during all stages of AI lifecycle (development, deployment, and maintenance)

- Model Monitoring - monitoring if model is not drifting from original that may create potential vulnerabilities and cost for our organization. Explainability tools - like SHAP and LIME - could help us with that task


That was very interesting room - in my opinion crucial one as I want to deal with defensive cybersecurity and I think AI can boost potential of defensive CyberSec dramatically if used properly.

I am stock market trader since 12 years - the way AI boosted my analysis and decision making capabilities cannot be described in words and I have hundreds of examples to defend this thesis.

Looking forward for more content related to this learning pathway, it's rocking so far.


**Task 6 - PRACTICAL**

This room demonstrated how to use an AI assistant in defensive security contexts. I tested it on four practical tasks: analysing an SSH failed login log, detecting a phishing email, generating threat hunting ideas, and creating a regex pattern for failed SSH attempts.

The final task was to retrieve three specific technical values (DoH port, SYN flood timeout, Windows ephemeral port range) using the AI and combine them into the room flag.

Having used AI tools intensively for months, I completed the entire room quickly and without difficulty.

I asked TryHackMe AI many more defensive cybersecurity questions extra questions, that I wasn't asked to prompt by website but I wanted to see the output, like:

 - Could you give me more details about this failed login attempt (data about the potential IP source)rce)? From where was the threat actor attacking? How many attackers were there? What critical systems were they trying to target? If a couple of systems, name them all and rank them. - 

- Give me guidance on how to investigate further? -

- "Would you like a sample set of commands or tools recommendations to facilitate this investigation?" - yes I would love to, give me all the data. -

- "Would you like sample scripts or specific command sequences for automation?" - Yes, please, do it - also mention to me which industries are most affected by this type of attacks and what they do to mitigate it. How would you classify this attack in terms of severity and potential threat in scale 1 to 10?" -

- Brilliant, do you think I should know anything else related to this topic? Is there anything else I should look into, maybe some resources to read, some courses, labs or task to do? - 


Of course, I also asked questions that I was ordered to in a task and I was able to succefully retrive flag.

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/ai-security-pathway/01-ai-ml-security-threats-task-6.png)

I prepared PDF of my whole prompt interaction and exchange with TryHackMe AI that is available [here to view](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/reasearch/AI%2C%20ML%2C%20DL%2C%20LLMs%2C%20and%20AI%20Security%20Research%20Map.pdf).



**Task 7 - CONCLUSION**

"Knowledge is a power" and AI seems to be our XXI century weaponized knowledge. It depends on us how we will use our weapon - to defend or to harm.
Cybersecurity focuses on defensive use of AI even if deployed in character of "red teaming" - the purpose is to test the systems and strengthen defense.

Here are some concept covered by this room which are supplemented by my choice of concepts and terminology that needs to be studied by me again to reinforce what I learned:

- Artificial Intelligence (AI) is the overarching field concerned with enabling machines/systems to mimic human behaviour.

- Machine learning (ML) is a subfield of AI in which a model can be fed and trained on input and used to make predictions.

- Deep learning (DL) is then a subfield of ML. It no longer needs human interaction and can self-tech and process mass amounts of data, possible through the use of Neural Networks.
- DL has enabled the emergence of technologies like LLMs (and other generative AI), which, through the use of transformer neural networks and attention, can be queried in natural language, understand it and respond in a human-like, conversational fashion.
- AI is a dangerous weapon in the hands of an attacker. It has the potential to enhance existing cyber attacks like phishing and increase the attack surface by introducing AI vulnerabilities.
- While being dangerous in the hands of attackers, AI can be invaluable in the fight against AI cyber threats and should be adopted, but done so securely so vulnerabilities are not introduced.
- Concepts and key terminology to research (supplement AI research): AI, ML, DL, RLHF, LLM, LLaMA, ML algorithm, Machine learning lifecycle, scalable ML, AI pre-training, neural networks, transofmer neural networks, contextual understanding, neural network layers (input, hidden, output), 4 categories of algorithms (supervised, unsupervised, semi-supervised, reinforcment learning), machine learning proces explanation (Defining Problem -> Data Collection -> Algorithm Selection + Model -> Data Cleaning -> Feature Engineering -> Model Evaluation + Training -> Model Deployment -> Model Monitoring), MItre AI atlas, voulnerabilities in AI models (prompt injections, data poisoning, model theft, model drift, data leakage and others - mention which ones), enhanced ai attacks (malware, deepfakes, phishing, and others - mention which ones), compact bullet points of IBM Cost of Data Breach Report, AI safety/ securing (securing model, privacy protection, implementation of standards like ISo/IEC 27090 - mention other important AI standards, model monitoring, doh port, syn flood timeout, windows ephemeral port range, ssh login log, ssh attempt,

**Extra note [21:14, 14/04/2026]** - [research](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/reasearch/AI-risk-research-notes.md#model-architecture) with concept and terminology is ready, courtesy of ChatGPT. [🔗](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/reasearch/AI-risk-research-notes.md#model-architecture)
 
This was a great room full eye opening knowledge and examples. I reviewed the rest of the AI Security learning path released by TryHackMe, and it looks like a well-oiled war machine. What an insane quality of content, big respect to the authors. 

I am excited and looking forward to the next modules.

---

## Further Learning & Professional Context
*Supplemental analysis generated through AI-assisted research*

---

### Core Concepts
1. **Adversarial machine learning** — the study of attacks and defenses that target the behavior, outputs, or training process of AI/ML systems.
2. **Evasion attack** — an attack that manipulates inputs at inference time so a model makes the wrong prediction or decision.
3. **Membership inference attack** — an attack that tries to determine whether a specific record was part of a model’s training data.
4. **Model inversion attack** — an attack that attempts to reconstruct sensitive input features or private training data from model outputs.
5. **Shadow AI** — the unsanctioned use of AI tools or services outside organizational visibility, policy, or approval.
6. **Explainable AI (XAI)** — methods that help humans understand why a model produced a particular output or prediction.
7. **AI red teaming** — structured adversarial testing of an AI system to uncover flaws, unsafe behavior, and misuse paths.
8. **Model card** — a short transparency document that explains a model’s intended use, limitations, training context, and risks.
9. **AI Bill of Materials (AIBOM)** — a transparency record that helps track the components, dependencies, and provenance of an AI system.
10. **Secure AI lifecycle** — the practice of applying governance, security, testing, and monitoring across design, training, deployment, and maintenance.

### Reading resources
**Beginner**
- [IBM: What is Artificial Intelligence (AI)?](https://www.ibm.com/think/topics/artificial-intelligence) — a clear, beginner-friendly intro to what AI is and what it is trying to achieve.
- [IBM: What is Machine Learning?](https://www.ibm.com/think/topics/machine-learning) — a practical introduction to ML as the data-driven subset of AI.

**Technical**
- [NIST: Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-2e2023.pdf) — the strongest technical reference here for understanding adversarial ML concepts, attack classes, and terminology.

### Career insights
This room matters later because AI is no longer separate from security work; it is becoming part of attacks, defenses, monitoring, and governance at the same time.  
For SOC work, the big value is learning how AI changes triage, phishing analysis, alert validation, and threat hunting, especially when noisy data becomes too large for manual review alone.  
For security engineers and AI governance roles, the room builds the habit of thinking about risk across the full lifecycle, not only at deployment.  
For AI red teaming and defensive testing, it introduces the mindset needed to look for misuse paths, unsafe outputs, and hidden failure modes.  
The overall lesson is that future defenders will need both cybersecurity judgment and AI literacy to stay effective.

### Professional Tools
- **MITRE ATLAS** (start early for AI security) — a knowledge base of adversary tactics and techniques against AI-enabled systems, useful for learning how attackers think about AI targets.
- **OWASP Top 10 for LLM Applications** (start early) — a practical risk map for common LLM security failures, especially useful when you are learning how AI apps break.
- **NIST AI RMF Playbook** (start early) — a structured guide for managing AI risk across the lifecycle, which helps build a governance-first security mindset.
- **Microsoft Sentinel** (start early, especially for SOC) — a cloud-native SIEM that supports detection, investigation, response, and proactive hunting.
- **Splunk Enterprise Security** (start early, especially for SOC) — a widely used SIEM/SOC platform for centralizing security data, hunting threats, and speeding investigations.
- **Microsoft Defender for Endpoint** (start early, especially for SOC) — an endpoint security platform that helps detect, investigate, and respond to threats on devices.
- **SHAP** (use later, especially in AI engineering / model assurance) — an explainability library that helps you understand which features influenced a model’s output.
- **LIME** (use later, especially in AI engineering / model assurance) — an explainability method that approximates black-box model behavior with local, interpretable explanations.
- **OWASP AIBOM Generator** (use later, especially in AI supply chain work) — a transparency tool for creating AI bills of materials so you can track model components and dependencies.
- **OWASP GenAI Red Teaming Guide** (use later, especially in AI security testing) — a structured guide for testing GenAI systems for misuse, unsafe behavior, and integration weaknesses.

### Learning path
This room fits TryHackMe’s AI Security path as the first major step into AI-specific security threats and defenses.  
It bridges general AI/ML understanding with the practical question of how those systems fail, how attackers abuse them, and how defenders respond.  
The next step is deeper defensive AI work, especially adversarial testing, AI monitoring, and blue-team use cases.  
That makes this room a foundation rather than a finish line: it prepares you to think about AI as both a target and a security tool.

### Critical Operational Pitfalls
- **Treating AI output as truth** — avoid this by validating important answers against logs, source data, or human review.
- **Focusing only on prompt injection** — avoid this by also considering poisoning, privacy attacks, model theft, drift, and unsafe automation.
- **Deploying AI without governance** — avoid this by defining access control, approval workflows, logging, and ownership before production use.
- **Ignoring model monitoring after launch** — avoid this by checking performance drift, false positives, and abnormal output behavior over time.
- **Using sensitive data in prompts without controls** — avoid this by applying least privilege, data minimization, and approved handling rules.
- **Over-relying on AI for triage** — avoid this by using AI to assist analysis, not replace verification and judgement.
- **Skipping documentation** — avoid this by keeping model cards, AIBOMs, and test results current so teams know what was built and what can fail.

### Prerequisites check
The main knowledge gaps to close next are basic machine learning vocabulary, the difference between AI and security governance, and the idea that models can fail in ways attackers can exploit.  
It also helps to understand simple defensive workflow concepts such as triage, monitoring, validation, and escalation.  
If AI red teaming or AI governance feels abstract, reviewing the NIST AI RMF and OWASP LLM Top 10 will make the next rooms easier to follow.  
A small amount of hands-on practice with logs, phishing examples, and AI outputs will make the concepts stick much faster.

---

**Methodology Note:** This section uses GPT-5.4 Thinking-Mini to provide a structured analysis of industry context, career pathways, and extended resources. Questions were formulated based on room content, and responses were validated against official documentation and industry sources.

**Generation Details:**
- Model: GPT-5.4 Thinking-Mini
- Date: 2026-04-14
- Prompt Framework: coming soon

---

## Next Steps
- I will reinforce my knowledge - read about the most important concepts and terms I learned in this room
- I will do research to find other AI models, LLMS, and defensive AIs like Nuclei (a fast, customizable, template-based vulnerability scanner that I found out about yesterday)
- I am moving into the next room - [*Room 2 - AI Models & Data*](https://github.com/micromediacoding/tryhackme-notes/blob/main/ai-security-path/02-AI-model-and-data.md)

## My profiles
- TryHackMe: [EchoHound](https://tryhackme.com/p/EchoHound)
- GitHub: [micromediacoding](https://github.com/micromediacoding)

---

*Write-up style follows my repository philosophy.*
