# AI, ML, DL, LLMs, Security, and Risk — Research Notes

A structured research note for cybersecurity and AI study.

---

## Table of Contents

1. [How to read this document](#how-to-read-this-document)
2. [Foundations](#foundations)
3. [Model architecture](#model-architecture)
4. [Machine learning categories](#machine-learning-categories)
5. [Machine learning lifecycle](#machine-learning-lifecycle)
6. [MITRE ATLAS and AI threats](#mitre-atlas-and-ai-threats)
7. [Enhanced AI attacks](#enhanced-ai-attacks)
8. [AI safety, governance, and standards](#ai-safety-governance-and-standards)
9. [Operational security notes](#operational-security-notes)
10. [Quick summary](#quick-summary)
11. [References](#references)

---

## How to read this document

The goal is to keep the topic organized from the simplest ideas to the most operational ones:

* **Foundations** explain what AI, ML, DL, and LLMs are.
* **Model architecture** explains how neural networks and transformers work.
* **Machine learning categories** explain how models learn.
* **Lifecycle** explains how ML systems are built and maintained.
* **Threats** explain how AI systems are attacked or misused.
* **Safety and standards** explain how to secure and govern AI.
* **Operational notes** cover useful technical details you may see in labs and real environments.

---

# Foundations

## Core terms

**AI (Artificial Intelligence)**
The broad field of systems that perform tasks associated with human intelligence, such as reasoning, perception, prediction, and language generation.

**ML (Machine Learning)**
A subset of AI where systems learn patterns from data rather than being explicitly programmed for every rule.

**DL (Deep Learning)**
A subset of ML that uses multi-layer neural networks to learn complex patterns.

**LLM (Large Language Model)**
A model trained on large text datasets to generate, summarize, translate, classify, or answer language-based prompts.

**LLaMA / Llama**
Meta’s family of foundation models.

**RLHF (Reinforcement Learning from Human Feedback)**
A training method that uses human preference feedback to improve model behavior and alignment.

**Pre-training**
The large initial training stage where a model learns general patterns from broad data before specialization.

**Scalable ML**
ML systems designed to handle more data, more users, and more model complexity without breaking the pipeline.

**Contextual understanding**
The ability of a model to use surrounding tokens, prior messages, and nearby context to produce a relevant output.

**Neural network**
A model made of connected layers that transform inputs into outputs.

**Transformer neural network**
A neural-network architecture based on attention, and the main architecture behind modern LLMs.

## Recommended research links

* [What is AI? — Google Cloud](https://cloud.google.com/learn/what-is-artificial-intelligence)
* [AI vs ML — Google Cloud](https://cloud.google.com/learn/artificial-intelligence-vs-machine-learning)
* [What is deep learning? — Google Cloud](https://cloud.google.com/discover/what-is-deep-learning)
* [What is an LLM? — Google Cloud](https://cloud.google.com/ai/llms)
* [Llama research — Meta AI](https://ai.meta.com/research/publications/llama-open-and-efficient-foundation-language-models/)
* [RLHF paper — OpenAI](https://cdn.openai.com/papers/Training_language_models_to_follow_instructions_with_human_feedback.pdf)
* [Transformer paper](https://arxiv.org/abs/1706.03762)

---

# Model architecture

## Neural network layers

A standard neural network has three major layer groups:

* **Input layer**: receives raw input data.
* **Hidden layers**: transform the data through learned weights and activations.
* **Output layer**: produces the prediction, class, score, or generated response.

## Why transformers matter

Transformers changed modern AI because they handle context well and scale efficiently. Instead of relying only on recurrence, they use attention to weigh which parts of the input matter most.

## Important concepts to know

* **Weights**: learned internal values that affect decisions.
* **Biases**: extra learned values that shift outputs.
* **Activation functions**: introduce non-linearity.
* **Parameters**: the learned numerical state of the model.
* **Inference**: using the trained model to produce an output.
* **Fine-tuning**: adapting a pretrained model to a specific task.
* **Embedding**: a numeric representation of text or other input.

---

# Machine learning categories

## The four major learning types

### 1. Supervised learning

Uses labeled data. The model learns from input-output examples.

### 2. Unsupervised learning

Uses unlabeled data to find structure, clusters, or hidden patterns.

### 3. Semi-supervised learning

Uses a small labeled set plus a larger unlabeled set.

### 4. Reinforcement learning

Learns through trial, error, and reward.

## Helpful comparison

| Category        | Data type       | Main idea                      | Example use                  |
| --------------- | --------------- | ------------------------------ | ---------------------------- |
| Supervised      | Labeled         | Learn from correct answers     | Spam classification          |
| Unsupervised    | Unlabeled       | Find hidden patterns           | Clustering users             |
| Semi-supervised | Mixed           | Use limited labels efficiently | Medical or security datasets |
| Reinforcement   | Feedback/reward | Learn by interaction           | Game agents, control systems |

---

# Machine learning lifecycle

## The standard lifecycle

1. **Define the problem**
   Decide what the model should do and what success looks like.

2. **Data collection**
   Gather the data required for training, validation, and testing.

3. **Data cleaning**
   Remove errors, duplicates, bad labels, outliers, and inconsistent formatting.

4. **Feature engineering**
   Convert raw information into useful model inputs.

5. **Algorithm selection + model building**
   Choose the model type and build the training pipeline.

6. **Training**
   Fit the model to the data.

7. **Model evaluation**
   Measure accuracy, precision, recall, F1, robustness, and error patterns.

8. **Deployment**
   Put the model into a production environment.

9. **Monitoring**
   Track performance, drift, bias, failures, cost, and abuse.

10. **Iteration**
    Improve the model using new data, feedback, and monitoring results.

## Why monitoring matters

A model can work well at launch and then degrade later because the world changes, the data shifts, or attackers start manipulating the input stream. That is why scalable ML is not just training; it is also observability, governance, and retraining.

## Useful lifecycle terms

* **Training data**: the data used to teach the model.
* **Validation data**: data used to tune model choices.
* **Test data**: unseen data used to estimate final performance.
* **Drift**: the model sees data that no longer matches the original distribution.
* **Skew**: train and production data differ too much.
* **MLOps**: the operational discipline for ML systems.

---

# MITRE ATLAS and AI threats

## MITRE ATLAS

**MITRE ATLAS** stands for **Adversarial Threat Landscape for AI Systems**. It is a knowledge base of tactics and techniques used against AI-enabled systems.

### Official link

* [MITRE ATLAS](https://atlas.mitre.org/)

## Main AI vulnerability classes

### Prompt injection

Crafted input tries to override instructions or manipulate the model’s behavior.

### Indirect prompt injection

Malicious instructions are hidden in external content that the model later reads.

### Data poisoning

Training or fine-tuning data is corrupted to influence model behavior.

### Model theft / model extraction

Attackers try to copy the behavior or capabilities of a model.

### Data leakage

The model reveals sensitive information from training data, prompts, memory, logs, or connected systems.

### Model drift

Performance degrades as real-world data changes.

### Insecure output handling

A downstream application trusts model output without validating it first.

### Denial of service / resource exhaustion

The model or its hosting application is overloaded by expensive or repeated requests.

### Tool abuse in agentic AI

An AI agent uses connected tools or permissions in unsafe ways.

### Memory poisoning

Persistent memory or long-term state is contaminated by malicious content.

### Goal hijacking

The model’s intended objective is redirected by an attacker.

## Best research links

* [OWASP Top 10 for Large Language Model Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
* [OWASP Gen AI Security Project](https://genai.owasp.org/)
* [OWASP LLM Prompt Injection Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html)
* [OWASP LLM01: Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/)
* [OWASP LLM10: Model Theft](https://genai.owasp.org/llmrisk2023-24/llm10-model-theft/)

---

# Enhanced AI attacks

AI makes classic attacks cheaper, faster, and more believable.

## Attack categories to remember

* **Phishing**: AI improves grammar, targeting, and scale.
* **Spear phishing**: AI can personalize messages more convincingly.
* **Vishing**: AI voice systems can imitate people.
* **Deepfakes**: synthetic audio/video that impersonates real individuals.
* **Malware development support**: AI can help write, modify, or refactor malicious code.
* **Social engineering**: AI helps create convincing pretexts and scripts.
* **Misinformation / disinformation**: AI scales content generation.
* **Credential abuse**: attackers can automate password and account targeting.
* **Agent abuse**: AI systems can be tricked into performing unsafe actions.

## Good reference links

* [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework)
* [NIST AI RMF resources](https://airc.nist.gov/airmf-resources/airmf/)
* [IBM Cost of a Data Breach Report 2025](https://www.ibm.com/reports/data-breach)
* [OpenAI RLHF paper](https://cdn.openai.com/papers/Training_language_models_to_follow_instructions_with_human_feedback.pdf)

---

# AI safety, governance, and standards

## What “AI safety” means in practice

AI safety is not only about stopping harmful content. It also means securing the full system:

* model weights
* prompts
* fine-tuning data
* embeddings
* tool permissions
* logs
* APIs
* output handling
* access control
* monitoring
* governance

## What to secure first

### 1. The data

Protect training data, prompts, RAG sources, memory, logs, and exports.

### 2. The model

Restrict access to weights, checkpoints, and deployment endpoints.

### 3. The application layer

Validate inputs and outputs, limit tools, and sandbox actions.

### 4. The runtime environment

Monitor ports, traffic, authentication attempts, and system logs.

### 5. The governance layer

Make policies, approvals, and ownership explicit.

## Important AI standards and frameworks

* [NIST AI RMF 1.0](https://www.nist.gov/itl/ai-risk-management-framework)
* [ISO/IEC 42001:2023](https://www.iso.org/standard/42001)
* [ISO/IEC 23894:2023](https://www.iso.org/standard/77304.html)
* [ISO/IEC 22989:2022](https://www.iso.org/standard/74296.html)
* [ISO/IEC 23053:2022](https://www.iso.org/standard/74438.html)
* [OWASP Top 10 for LLMs](https://owasp.org/www-project-top-10-for-large-language-model-applications/)

## Notes on developing standards

Some standards are still evolving. When you study them, treat them as emerging guidance rather than fixed final doctrine.

---

# Operational security notes

## DoH port

**DNS over HTTPS (DoH)** commonly runs over **TCP 443** because it is carried inside HTTPS traffic.

## Windows ephemeral port range

The default Windows dynamic client port range is **49152–65535**.

## SYN flood timeout

There is not one universal “SYN flood timeout” setting. In practice, you will see controls around:

* SYN backlog
* TCP retries
* syncookies
* connection rate handling

On Linux, syncookies help reduce SYN-flood pressure.

## SSH login logs

SSH authentication events are usually recorded in system logs such as:

* `/var/log/auth.log`
* journald

## SSH attempts

Repeated SSH attempts are often visible as failed login entries in the authentication log. That makes SSH logs a useful source for brute-force or intrusion detection.

## Reference links

* [Microsoft: Default dynamic port range for TCP/IP](https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/default-dynamic-port-range-tcpip-chang)
* [Microsoft: DNS over HTTPS server](https://learn.microsoft.com/en-us/windows-server/networking/dns/enable-dns-over-https-server)
* [Ubuntu sshd man page](https://manpages.ubuntu.com/manpages/focal/en/man8/sshd.8.html)
* [Linux kernel ip-sysctl documentation](https://docs.kernel.org/networking/ip-sysctl.html)

---

# Quick summary

* **AI** is the umbrella.
* **ML** is a subset of AI.
* **DL** is a subset of ML.
* **LLMs** are deep-learning models specialized for language.
* **Transformers** are the core architecture behind modern LLMs.
* **AI threats** include prompt injection, poisoning, theft, leakage, and agent abuse.
* **AI safety** means securing the full system, not just the model.
* **Standards** such as NIST AI RMF, ISO/IEC 42001, and ISO/IEC 23894 help create a governance structure.
* **Operational monitoring** still matters: logs, ports, auth attempts, and traffic patterns remain critical.

---

# References

## Core AI and ML

* [Google Cloud: What is AI?](https://cloud.google.com/learn/what-is-artificial-intelligence)
* [Google Cloud: AI vs ML](https://cloud.google.com/learn/artificial-intelligence-vs-machine-learning)
* [Google Cloud: What is deep learning?](https://cloud.google.com/discover/what-is-deep-learning)
* [Google Cloud: What is an LLM?](https://cloud.google.com/ai/llms)
* [Meta AI: Llama](https://ai.meta.com/research/publications/llama-open-and-efficient-foundation-language-models/)
* [Transformer paper](https://arxiv.org/abs/1706.03762)
* [OpenAI: RLHF paper](https://cdn.openai.com/papers/Training_language_models_to_follow_instructions_with_human_feedback.pdf)

## Threats and security

* [MITRE ATLAS](https://atlas.mitre.org/)
* [OWASP Gen AI Security Project](https://genai.owasp.org/)
* [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
* [OWASP Prompt Injection Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html)
* [IBM Cost of a Data Breach Report 2025](https://www.ibm.com/reports/data-breach)

## Standards and governance

* [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework)
* [NIST AI RMF resources](https://airc.nist.gov/airmf-resources/airmf/)
* [ISO/IEC 42001:2023](https://www.iso.org/standard/42001)
* [ISO/IEC 23894:2023](https://www.iso.org/standard/77304.html)
* [ISO/IEC 22989:2022](https://www.iso.org/standard/74296.html)
* [ISO/IEC 23053:2022](https://www.iso.org/standard/74438.html)

## Operational references

* [Windows dynamic port range](https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/default-dynamic-port-range-tcpip-chang)
* [DoH on Windows Server](https://learn.microsoft.com/en-us/windows-server/networking/dns/enable-dns-over-https-server)
* [Ubuntu sshd man page](https://manpages.ubuntu.com/manpages/focal/en/man8/sshd.8.html)
* [Linux kernel networking docs](https://docs.kernel.org/networking/ip-sysctl.html)
