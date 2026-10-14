Version: NAFATH-V4

Track: AI

## Overview
A national service provider depends on software, AI models, mobile applications, data, and internet connectivity to deliver reliable services. Each area can introduce security risks that can affect the wider system. Secure configuration helps keep passwords and other secrets out of source code. AI security examines how attackers may manipulate model inputs or training data. Mobile security standards help teams verify that applications protect sensitive information. In networking, RPKI helps validate the origin of internet route announcements, although it cannot prevent every routing attack. Vulnerability management is also essential, as the Log4Shell flaw in Apache Log4j demonstrated how a weakness in a widely used component can expose systems to serious risk. A Software Bill of Materials (SBOM) helps organizations identify software components and investigate exposure to known vulnerabilities. Together, these practices improve visibility, reduce avoidable risks, and support a more secure technology supply chain.

## Software
The Twelve-Factor App methodology recommends storing configuration in environment variables rather than directly in application code. This includes deployment-specific settings and sensitive values such as API keys. Keeping configuration separate allows the same codebase to run in different environments without embedding secrets in source files. It also reduces the risk of exposing credentials when code is shared or published. Access to secrets should still be controlled, and environment variables must be managed securely.
Resource: The Twelve-Factor App — III. Config - https://12factor.net/config

## AI
Adversarial machine-learning attacks target an AI system to influence its behavior. An evasion attack changes an input at prediction time, causing a trained model to produce an incorrect result. A poisoning attack manipulates training data or the training process, potentially affecting what the model learns. For example, altered images may mislead a deployed classifier, while poisoned examples may weaken future predictions. Defenses must address both input robustness and training-data integrity.
Resource: NIST — Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2023/final

## Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) gives teams a structured way to assess mobile app security. It covers areas such as sensitive-data storage, cryptography, authentication, network communication, and privacy. Teams can use MASVS to define the security controls an app should meet, then use the OWASP Mobile Application Security Testing Guide (MASTG) to test whether those controls are implemented correctly. This makes security checks more consistent and easier to document.
Resource: OWASP — Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/

## Networking

## Cybersecurity

## Data
## Misconception in My Track

## Open Question
