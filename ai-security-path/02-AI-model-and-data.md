# Room 2 - AI Models & Data - TryHackMe [🔗](https://tryhackme.com/room/aimodelsdata)

**Started:** 21:43, 14 April 2026

**Completed:** xx:yy, x April 2026 

**Difficulty:** Easy | **Time:** ~60min

**Room:** [AI Models & Data](https://tryhackme.com/room/aimodelsdata)

**Spoiler warning** — This write-up contains **zero answers**.

---

## Overview

This room is all about the data side of AI models and the security risks that come from how those models are built and trained. I went through every task, read the explanations carefully, answered the questions, and finished with a strong practical lab in Task 6 where I had to audit a real model card and find all six red flags. I learned how training data is actually collected, why poor data provenance creates big problems, and how things like web scraping or synthetic data can introduce PII and hidden vulnerabilities. It also covered the inheritance problem when companies fine-tune pre-trained models and the black box nature of these models, plus why model cards are important but still have gaps. The practical task in Task 6 was really the strongest part for me — it forced me to actively look for red flags like missing provenance, self-issued licenses, and suspicious weight differences after pruning or quantisation, and I had to do it properly across three attempts before getting 6/6.
Here’s what stood out for me:

**- Training data mostly comes from web scraping, licensed datasets, synthetic data, or internal corpora, and poor provenance makes it hard to know where the data really came from or if it was modified.
- PII and sensitive credentials can easily end up baked into model weights through large-scale scraping, which creates privacy and extortion risks later.
- Overfitting, pruning, quantisation and federated learning all introduce their own security weaknesses that aren’t always caught during validation.
- The inheritance problem means that when you fine-tune a pre-trained model you also inherit all its hidden flaws, biases and backdoors from the original training data you never controlled.
- Models are essentially black boxes made of billions of floating-point numbers with no clear record of how they were built, so model cards are the main (but imperfect) way to add transparency.
- Auditing a model card means checking things like training data sources, intended use, evaluation results, known limitations, bias assessment and licensing — and spotting when any of those are missing or suspicious.**

This room wasn’t super technical but it connected a lot of dots for me on why data quality and model transparency matter from a cybersecurity point of view. The practical model card audit at the end was genuinely useful and made the whole room feel more hands-on. I saved the full interaction with the TryHackMe AI and my model card assessment as a PDF and added it to the repo. I think this is solid knowledge to build on before I start the more hands-on AI security labs.

**Proof of Completion**  
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/ai-security-pathway/02-ai-models-and-data-completion-badge.png)


---

## Personal, handwritten notes from the room (redacted - no answers visible)

**TASK 1 - INTRODUCTION**

This room will be oriented on AI models and data, and how things like the training data specification or good/poor data management/choice can affect the vulnerability of individual systems or organisations.

According to THM, after this room, I will understand:

* where AI data comes from, and what are the risks of poor data provenance
* How to recognise how Personally Identifiable Information and sensitive credentials are embedded in model weights through large-scale web scraping
* How key model decisions (overlifting, quantisation, federated learning) introduce specific security risks
* inheritance problem and what happens when organisations unknowingly fine-tune pre-trained models
* Why trained models are black boxes, and what model cards do/fail to address this

**TASK 2 - TRAINING DATA**

1. Where does data come from?

In previous rooms, I learned that before an AI model can be trained, data must be collected and cleared, but COLLECTED BY WHOM AND FROM WHERE?

LLM training requires a large amount of text (GPT-3 needed 570GB). In that case, sources are not “hand-picked” - there are 4 pipelines that exist:

A) Web scraping - it’s an automated crawl of public internet content (news, forums, blogs, social media, etc.) 
Trust profile - Low: no curator, no version control, content changes after collection

B) Licensed datasets - Data purchased or agreed with platforms (e.g., OpenAI + Reddit, Meta’s own social posts) 
Trust profile - Medium: terms often unclear; original users rarely consented to AI training use

C) Synthetic data - it’s an AI-generated content used to train further AI systems 
Trust profile - Variable: growing fast; ~12% of fine-tuning datasets now contain LLM-generated content

D) Internal corpora - those are company knowledge bases, support transcripts, and clinical notes used for fine-tuning 
Trust profile - Higher: organisation has direct control, but also direct liability if mishandled

The most used training dataset is Common Crawl. DeepSeek-V2, DeepSeek-V3, LLaMA4 and GPT-3 were trained on it.

1. The Problem of Provenance

Data provenance is the ability to answer 3 training data-related questions:

* Where did it come from?
* When was it collected?
* Has it been modified since?

Answer to all 3 nowadays is - we don’t fully know. Models are trained on datasets of datasets, some of them poorly recorded. Some of them were misclassified. Tuning to those is risky.

ML-BOM, a documented inventory of dataset sources, licenses, PII categories, and filtering decisions, is an attempt to answer this problem. Adoption is still early, and most orgs using third-party models today have nothing close to one.

1. PII (personally identifiable information) in the Pipeline

One of the consequences of poorly managed and low-quality data training is that personal data lands in models and it’s really hard to remove.
Official bodies, like EU GDPR, suggest “data  minimisation” but it sit opposite to “more data is always better” doctrine that is driving pre-training of models.

Weak model or a model with bugs and vulnerabilities may be abused by threat actors in order to extort sensitive data

1. A model Engineer

The data supply chain is real and exploitable - orgs start to see it now - unaudited data contaminated with PII or manipulated upstream can cause harmful model behaviour which may lead to serious consequences.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/ai-security-pathway/02-ai-models-and-data-task-2.png)

**TASK 3 - BUILDING THE MODEL**

1. Epochs and Overfitting

Epochs are a complete pass of the algorithm through the entire data set (nowadays, many data sets). The model sees the same dataset and adjusts the parameters.

More epochs/training not always leads to better model, as too long may shifts model towards memorising data instead of pattern learning - which is called OVERFITTING.

Overfitting models will perform well on own data, but fail on outside data.
It’s a security concern, because through overfitting, a model can memorise sensitive data, which it can later reproduce as a prompt.

1. Model Validation

Part of the data is held on the side and called VALIDATION SET.
At regular intervals, the model is trained on this type of unseen dataset to assess its performance.
If training accuracy keeps climbing but validation accuracy plateaus or drops, that’s overfitting in real time.

Model Validation is quality measure in ML lifecycle from cybsec perspective - models that are not validates create security risk because their behaviour is unpredictable.
It also leads to anomalies and biases being undetected until model is depoloyed which may leads to consequences.

1. Post-Training Optimisation: Pruning and Quantisation

Once the model is trained, it usually goes through compression processes. The most common ones are Pruning and Quantisation. Both create security risks.

a) Pruning removes parameters that contribute little to predictions, shrinking the model, which may lead to significant model behaviour change that will be spotted post-deployment.

b) Quantisation reduces numerical precision of weights (example: 32-bit to 8-bit floats) in order to cut memory requirements. Test before deployment may fail to detect backdoors in defences because of that.

1. Federated Learning

Is a method of decentralisation of model learning and training. For example, if hospital wants to train its model, it doesn’t want to risk sensitive data of patients - therefore it uses federated learning to decentralize the process and outsource the data elsewhere.

The risk are data corruption as third unresponsible entities, or entities with bad intentions may affect data.

Example may be poisoned local updates from threat actors - which may affect the model or affect the hospital operations itself.

**TASK 4 - THE INHERITANCE PROBLEM**

It’s a term that describes type of “penalty” that companies inherit, when they “tune” (upgrade, add data, modify) pre-trained model.

They will inherit all the flaws of that model, with a base that was shaped by process, not controlled by organisation, on data not audited by organisation and without knowledge of the data chain supply. (biases baked during pre-training, unexpected behaviours caused by base model actions, not durable safety alignments in base model)

Fine-tuning disadvantages later appear in these forms:

a) safety alignment erosion
b) attack surface increases because of model specialisation
c) flow in the base model related to security backdoors, problematic training data and other anomalies

Fine-tuning is a powerful tool to leverage to optimise services and lower the cost, but it brings a lot of risks to the table.

An example of fine-tuning is when a hospital adds additional parameters to its pretrained model in order to make it more efficient in understanding medical terms and tasks.

Fine-tuning changes models TASK SPECIFIC BEHAVIOUR, TONE AND DOMAIN KNOWLEDGE but it’s ceaps BASE MODEL WEIGHT UNCHANGED.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/ai-security-pathway/02-ai-models-and-data-task-4.png)

**TASK 5 - THE BLACK BOX PROBLEM**

1. Model Cards.

You can only SAMPLE the model - YOU CANNOT AUDIT IT.

What it means is that, once you create a model, it cannot be disassembled like any other code - it’s created from billions of floating-point numbers (cumulative result of training), and they carry no record of how they were created, modified or what data was used.

Entirely trusting any model is risky. You can only know how the model MAY act on the same prompts as you sampled, but you don’t know how it will behave with prompts you didn’t think of, created by threat actors.

MODEL CARDS were created to tackle this problem - an artefact, structured description document that is ment to accompany the model, explaining how it was build and what may be it flaws.
Concepted was introduced by Google researchers in 2019

Good MODEL CARD - like Google Gemma should inform me about:

* Training Data - what sources were used, filtering methodology, gaps and biases in model
* Intended use - purpose of model determined during DESIGN PHASE
* Evaluation results - performance data across different conditions and demographics
* Known limitations - circumstances under which the model underperforms
* Bias assessment - when/why model drifts toward bias
* License - what you are permitted to do with the model
1. The Gaps

The problem is that even well described model can have flaws… in the description itself, like descriptions of food from labels in real life.

There is no legal obligation YET (I am sure it’s just matter of time there will be) to provide model cards and Data Provenance Initiative emphasizes that there is still a lot to do in this matter.

From a cyberSec perspective, the lack of a model card is a WARNING SIGN. It means LACK OF COMPETENCY and TRANSPARENCY from the company using a model WITHOUT A CARD.

Model Card is also an audit trail, a strong shield, proof of good intentions from a company in case it will get into trouble because the model there were using becomes corrupted and causes problems.

Terms: Model weights, floating-point numbers in AI, model card, Data Provenance Initiative, AI supply chain.

**TASK 6 - PRACTICAL**

In the practical task, I am performing audit of AI model card.

I need to find 6 red flags related to that model card. It’s a great practical exerscise because before I didn’t know about:

a) model card
b) where to look for it
c) what to look at closely when I read it
d) what are the potential red flag

Now I know all of those.

I found all the red flags and I understand logic - why those were red flags.

**1) First attempt (4 rights qualitative scores)

Self-issued license, fine-tuned from other models, trained on public data, from which part is very questionable and creates high risk, low evaluation score -

and last one that I am most proud about, it took me a little bit to find it - THE DIFFERENCE IN WEIGHT BETWEEN BASE MODEL AND MODEL DECLARED BY COMPANY.

The declared weight of files in the base model (tuned model), is different to the weight presented and declared by the company as files (the company model is smaller, they shrinked it, we don’t know what they took out, maybe their actions reduced the overall model security and defenses).

After marking the right issues (6 issues with model card) it turns out that although I find the right issues I scored their severity improperly - 4 out of 6 on the first attempt, and I need to score 5 properly (in qualitative scale - low,medium,high).

2) Second attempt - 5 right scores (I am going for 6)

3) Third attempt - 3 attempt, 6/6

I love that task, now I know basics of the AI model assessment and the basics of Model Card Assesments - what should I look for, what is suspicious, what should be check. What may be just slightly dangerous and what carries huge potential risk.
![Room 100% completed](https://github.com/micromediacoding/tryhackme-notes/blob/main/assets/images/ai-security-pathway/02-ai-models-and-data-task-6.png)

TASK 7 - CONCLUSION

This was a great room which teached me a lot about how to assess potential AI model. It also explained the difference between the base-model and fine-tuned model, risks related to turning base-model into fine-tuned model, characteristics of good/bad model and how to determine them.**

I am adding list of key concepts and terminology that I need to research about in order to reinforce what I just learned:

Data Provenance, common crawl, sbom, ml-dbom, truffle security, eu gdpr, llaMA4, web scraping, licensed ai dataset, synthetic ai data. internal corpora, trained model, fine-tuining, pre-training, model-building, PII, AI training data, AI model card, model card audit, model card red flags, ai model assesment (training data, intendfded use, evaluation results, known limitations, bias assessment, license) - longer note on that last one

---

## Further Learning & Professional Context
*Supplemental analysis generated through AI-assisted research*

---

### Core Concepts
1. **Data lineage** — the documented path showing where a dataset came from, how it changed, and where it was used.
2. **Dataset versioning** — saving stable snapshots of training data so model results can be reproduced and audited later.
3. **Sampling bias** — distortion caused when the collected data does not represent the real-world population the model will face.
4. **Label noise** — incorrect, inconsistent, or low-quality labels that reduce model reliability and can hide weak spots.
5. **Class imbalance** — a situation where one outcome appears far more often than others, which can skew predictions and evaluations.
6. **Train/validation/test split** — the practice of separating data into different sets so performance is measured on unseen examples rather than memorized ones.
7. **Reproducibility** — the ability to recreate a model’s behavior from the same code, data, and configuration.
8. **Model governance** — the policies and controls used to manage model risk, approval, oversight, and ongoing accountability.
9. **Audit trail** — a record of decisions, changes, and checks that shows how a model or dataset evolved over time.
10. **Artifact signing** — verifying that a model file, dataset, or package has not been changed since it was approved.

### Reading resources
**Beginner**
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) — a clear, practical overview of how organizations should think about AI risk and trustworthiness.
- [Google Model Cards for Model Reporting](https://arxiv.org/abs/1810.03993) — the original paper that introduced model cards and explains why documentation matters.

**Technical**
- [NIST AI RMF 1.0 PDF](https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf) — the main technical framework for mapping, measuring, and managing AI risk across the lifecycle.

### Career insights
This room matters later because almost every AI security problem starts with data quality, data provenance, or a missing audit trail.
For defenders, it builds the habit of checking what went into a model before trusting what comes out of it.
For security engineers and AI governance roles, it reinforces the need for documentation, validation, and lifecycle control.
For SOC and detection work, the mindset carries over: trust evidence, verify sources, and never assume the system is transparent just because it is useful.
The bigger career lesson is that AI security is as much about process and accountability as it is about technical performance.

### Professional Tools
- **DVC (start early)** — a data and model version control tool that helps track datasets, experiments, and pipelines, which is valuable whenever reproducibility matters.  
- **Great Expectations (start early)** — a data validation framework that checks whether training or evaluation data meets expectations before a model uses it.
- **OpenLineage (start early)** — an open standard for tracking data lineage, which is useful when you need to know where data and jobs came from.
- **MLflow Model Registry (start early)** — a model management system that tracks versions, lineage, metadata, and lifecycle state across development and deployment.
- **Model Card Toolkit (start early)** — a toolkit for generating model cards so teams can document intended use, limitations, and evaluation results consistently.
- **NIST AI RMF Playbook (start early)** — a practical companion to the AI RMF that helps map AI risks to concrete governance actions.
- **OpenRefine (useful early for data cleanup)** — a lightweight tool for cleaning and normalizing messy data before it becomes part of a training pipeline.
- **Weights & Biases (useful once you begin experiments)** — an experiment tracking platform that helps compare runs, capture metadata, and spot training issues faster.

### Learning path
This room fits naturally after the AI threats overview because it explains the data and model foundations that those threats exploit.
It goes deeper into how models are built, documented, and assessed, which makes the earlier attack concepts easier to understand in practice.
The next step is usually more operational: securing the model lifecycle, testing for misuse, and applying governance and monitoring in real environments.
So this room acts as the bridge between “AI can be attacked” and “here is how the attack surface is created and controlled.”

### Critical Operational Pitfalls
- **Assuming more data always means better models** — avoid this by checking whether the data is representative, clean, and legally usable.
- **Ignoring provenance** — avoid this by tracking source, timestamp, transformation steps, and ownership for every major dataset.
- **Trusting pretrained models without review** — avoid this by treating base models as inherited risk until they are evaluated and documented.
- **Skipping version control for data and models** — avoid this by storing immutable snapshots so you can reproduce results and investigate failures.
- **Treating model cards as marketing material** — avoid this by reading them as risk documents and comparing them against actual artifacts and evaluations.
- **Not validating after fine-tuning or compression** — avoid this by re-running evaluation after any major change such as pruning, quantization, or domain adaptation.
- **Leaving sensitive data in training corpora** — avoid this by filtering, minimizing, and controlling access before training begins.
- **Failing to monitor after deployment** — avoid this by watching for drift, regressions, and unexpected changes in real-world behavior.

### Prerequisites check
The main knowledge gaps to close next are data lineage, reproducibility, and the difference between a model description and the underlying training evidence.
It also helps to understand basic software version control, because model and dataset control works best when the workflow feels familiar.
If you are not yet comfortable reviewing an artifact for missing sources, weak evaluation, or unclear license terms, that is the next skill to build.
A little more practice with AI governance and model documentation will make the next rooms much easier to assess critically.

---

**Methodology Note:** This section uses GPT-5.4 Thinking-Mini to provide a structured analysis of industry context, career pathways, and extended resources. Questions were formulated based on room content, and responses were validated against official documentation and industry sources.

**Generation Details:**
- Model: GPT-5.4 Thinking-Mini
- Date: 2026-04-15
- Prompt Framework: coming soon

---

## Next Steps
- 
- 
- I am moving into the next room - [*Room XXX - NAME*](https://tryhackme.com/room/packetsframes)

## My profiles
- TryHackMe: [EchoHound](https://tryhackme.com/p/EchoHound)
- GitHub: [micromediacoding](https://github.com/micromediacoding)
