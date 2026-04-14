# Room 1- AI/ML Security Threats - TryHackMe
[🔗](https://tryhackme.com/room/aimlsecuritythreats)

**Completed:** xx April 2026  
**Difficulty:** Easy | **Time:** ~60min
**Room:** [AI/ML Security Threats](https://tryhackme.com/room/aimlsecuritythreats)

**Spoiler warning** — This write-up contains **zero answers**.

---

## Overview
It will be written once room is completed.

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/misc/coming_soon.png)

---

## Personal, handwritten notes from the room (redacted - no answers visible)

**Task 1 - INTRODUCTION**

The world around is quickly changing and implementation of AI in our lives will need a lot of adaptation from every industry.
New models of AI are developed in rapid speed and will new approach and methodology from cybersecurity industry too.

TryHackMe informs that in this module I will learn:

A. What is AI/ Machine Learning (ML)?
B. How can it be used in our industry?
C. How will it affect my role?
D. How is AI being leveraged by Attackers?

they emphasize that room is inteded to be entry point to AI topic and the learning objectives will be:

-  Understanding AI, ML, and their impact on the cyber security industry.
-  Understanding Deep Learning (DL) and neural networks, and how they have made the applications of AI, we see today, possible. 
-  Understanding how adversaries use AI to enhance existing attacks and take. advantage of AI Model vulnerabilities.
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
C) The network of neurons learns by adjusting strenght of these connections


THM presents diagram which represents AI type of neural network with:

A) Input layer - recieves raw data
B) Hidden layer - process and refines the input data
C) Output layer - produces the final predicition

Each connection has a weight, detrmining it's importance (for example in email body text may have more importance than subject).


Deep Learning and Machine learning gets very often confused, but the main difference is that Machine Learning works on labelled data and Deep Learning can take labbaled or unlabelled datasets, algorithm decides which data to use and therefore produces output without human intervention.

DL is possible through leveraging neural networks and grinding through large unlabelled datasets of it's choice.

Some people considered it "scalable ML".

The idea of neural networks has been around for decades but it's rapid technological advancement and mass digitisation of information in recent years that lead to such a progress in Ai capabilities.



**Task 3 - LLMs**

Intrudction of ML -> Introduction of DL and neural networks -> Large Language Modules (LLM's) come into play.

ChatGPT was a main trigger of that progress - it has ability to generate human-like text responses to human queries begin a new era in technology and new race - who is gonna develop best AI?

LLMs are DL based AI models the generate output based in the input, actively predicting next word in a sequence. So what happens when I query chat bot, for example:

"Sometimes I think AI may outsmart ...."

This quote would be fed into LLM and the model will try to predict the final word - in this case the final word may be "rat" or "dolphin" or "orca" but probably (I am not LLM) the right final word in that case will be "humans", for vast amount of reasons that AI will be able to process in split of a second thanks to immerse processing capabilities and access to infinite-like amount of data in relation to human being. 


LLMs are first trained in pre-training phase where they process vast amount text, like GPT-3 which was pre-trained with amount of text THAT WOULD TAKE HUMAN 2600 YEARS OF NON-STOP READING.

GPT-4 was fed with even more amount of data and empowered by DL.

LLM's leverage DL methodology - they process vast amount of unlabelled data, using BILLIONS OF PARAMETERS in short amount of time enabling them to understand and generate human-like output.

This PARAMETERS are fined-tuned automatically as the model processes text, while adjusting based on predicition accuracy to improves its own response quality.
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
Advancement of hardware, especially latest advancement of GPU, make this process possible through enabling masses of parallel operations of massive datasets while using advanced neutral networks, specifically type of networks that are called TRANSFORMER NEURAL NETWORKS.                      

2017s Google publication "Attention is all you need" (I need to find the original and upload it to my github as well as some analysis of that document done by cybersecurity and IT experts) introduced transformer neural networks which enabled to processing parallel text instead of word-by-word analysis.

This model improved CONTEXTUAL UNDERSTANDING, thanks to ability to assign "attention" to key words by encoding them into numerical values and calculating "attention" scores. It greatly improved the accuracy of the models helping them in the interpretation of ambiguous references, like distinguishing whether "it" in this sentence refers to "the dealer" or "the car".

The dealer approved the car purchase, it was financially stable.

After pre-training, humans add a step called REINFORCEMENT LEARNING FROM HUMAN FEEDBACK.
In this step model review the predictions and any that would be considered unhelpful by a us or have issues are flagged and the parameters are adjusted accordingly in a real time.

Once trained and reinforced, model can be used in various task, like translating, chatbot, calculator - model constantly tries to predict next word as a response, and so on, until the user has complete response.

LLMS are powering generative AI (ChatGPT and LLaMA) which can create various content not only text like images and music but those results are possible thanks to years of research and innovation, not instant development.


Key concepts of this room were:

A) Artificial Intelligence (AI) constitutes the comprehensive discipline that includes every system designed to replicate human intelligence. 

B) Machine learning (ML) serves as a core subset of AI, enabling it to identify and learn patterns directly from data without requiring explicit programming instructions. 

C) Deep learning (DL) represents a more advanced and focused subset of machine learning that employs neural networks to analyze massive datasets through intricate, layered processes entirely autonomously, functioning in essence as a highly scalable evolution of machine learning. 


D) Large Language Models (LLMs), such as those exemplified by GPT, are sophisticated deep learning architectures constructed on neural networks - specifically transformer models -engineered to comprehend and generate text that closely mirrors human language.


This room was brilliant! To concept and definitions that I need to reinforce:

AI, ML, DL, RLHF, LLM, LLaMA, ML algorithm, Machine learning lifecycle, scalable ML, AI pre-training, neural networks, transofmer neural networks, 



**Task 4 - AI SECURITY THREATS**

In this room I will be introduced to how threat actors use AI - from methodology to tools.

MITRE ATT&CK Framework will be helpful here and thanks to what I learned during course "Cybersecurity in AI era" by Uni of Meryland on Coursera, I know the basics and how to navigte it.

1) VULNERABILITIES IN AI MODELS

- Prompt Injections - prompts are used to instruct models and a prompt injection happens when threat actors ovverride original model with their own instructions for malicious purposes such a generating harmful content or accessing/disclosing information it shoudln't

- Data poisoning - occurs when threat actors manipulates corpus/training data used to train AI, for example, they could mainpulate training data used to train AI so it will fail to recognise spam emails, allowing email to bypass AI filter

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

**Task 5 - DEFENSIVE AI**
⌛




**Task 6 - PRACTICAL**
⌛




**Task 7 - CONCLUSION**
⌛
