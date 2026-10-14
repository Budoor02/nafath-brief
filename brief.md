Version: NAFATH-V4

Track: AI

## Overview
A national service provider depends on software, AI models, mobile applications, data, and internet connectivity to deliver reliable services. Each area introduces security risks that can affect the wider system. Secure configuration helps keep passwords and other secrets out of source code. AI security examines how attackers may manipulate model inputs or training data. Mobile security standards help teams verify that applications protect sensitive information. In networking, RPKI helps validate the origin of internet route announcements, although it cannot prevent every routing attack. Vulnerability management is also essential, as the Log4Shell flaw in Apache Log4j demonstrated how a weakness in a widely used component can expose systems to serious risk. A Software Bill of Materials (SBOM) helps organizations identify software components and investigate exposure to known vulnerabilities. This also raises an important AI security question: how can providers detect adversarial attacks on AI models?

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
BGP route hijacking happens when a network announces a route that it is not authorized to originate, potentially diverting internet traffic. Resource Public Key Infrastructure (RPKI) helps reduce this risk through Route Origin Validation, which checks route announcements against signed authorizations from prefix holders. Network operators can use the validation result to apply routing policies to invalid announcements. However, origin validation does not verify every part of the AS path, so it cannot prevent all routing attacks.

Resource: RFC Editor - RFC 6811: BGP Prefix Origin Validation - https://www.rfc-editor.org/rfc/rfc6811.html

## Cybersecurity
Log4Shell (CVE-2021-44228) is a critical remote-code-execution vulnerability in Apache Log4j 2, a Java logging library. Under vulnerable conditions, an attacker could send crafted input that may cause the affected system to execute malicious code. The vulnerability received a CVSS score of 10.0, the highest severity rating. Organizations should identify affected systems, upgrade to a fixed Log4j version suitable for their environment, and investigate signs of exploitation.
Resource: Apache Logging Services — Security - https://logging.apache.org/log4j/2.x/security.html

## Data
A Software Bill of Materials (SBOM) is a structured inventory of the components used to build a software product. NTIA identifies seven minimum data fields: supplier name, component name, component version, other unique identifiers, dependency relationships, SBOM author, and timestamp. These details help organizations identify affected components when a vulnerability is disclosed and assess where action may be needed. An SBOM improves supply-chain visibility, but it does not by itself guarantee that software is secure.

Resource: NTIA — The Minimum Elements For a Software Bill of Materials (SBOM) - https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom

## Misconception in My Track
A common misconception is that a machine-learning model is secure if it achieves high accuracy on ordinary test data. High accuracy on clean examples does not show whether a model can resist deliberately manipulated inputs or poisoned training data. Evasion attacks target model inputs at prediction time, while poisoning attacks affect training data or the training process. Security testing should therefore include relevant adversarial scenarios and controls for data integrity, not only standard accuracy measurements. NIST’s taxonomy explains these attack categories and why they require distinct mitigations.

Supporting resource section: NIST — Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations, Section 4.5, "Tradeoffs Between the Attributes of Trustworthy AI"- https://csrc.nist.gov/pubs/ai/100/2/e2023/final

## Open Question
How can a national service provider detect adversarial attacks on AI models while protecting user privacy and keeping essential services reliable?
