# Lab 1 - Cyber Threat Intelligence Report Mapping to MITRE ATT\&CK

## Group members

* Daniela Slavutin

## Source CTI Report

* **Link:** [The Smishing Deluge: China-Based Campaign Flooding Global Text Messgaes](https://unit42.paloaltonetworks.com/global-smishing-campaign/)

## Attack Summary

The executive summary describes a massive smishing campaign led by a threat group know as the "Smishing Triad". Investigations indicate the attackers operate from China and utilize thousands of temporary domains registered in Hong Kong. The campaign impersonates international services across critical sectors such as banking, cryptocurrency platforms, e-commerce, healthcare and law enforcement. 

Using social engineering via deceptive SMS messages (often faking urgent package deliveries or unpaid tolls) the attackers create a false sense of urgency to trick victims into clicking malicious links. The operation functions as a highly scalable Phishing-as-a-Service ecosystem, constantly rotating domains and infrastructure to evade detection. Ultimately, the goal is to steal highly sensitive information, including National Identity Numbers, home addresses, payment details and login credentials.

## Attack Diagram

![The PhaaS ecosystem of the Smishing Triad](https://unit42.paloaltonetworks.com/wp-content/uploads/2025/10/word-image-251216-161931-2-1495x1536.png)

*(Figure from the report detailing the attack supply chain and ecosystem)*

## MITRE ATT\&CK Mapping

| Tactic | Technique (ID \& Link) | Observed Behavior from Report |
| :--- | :--- | :--- |
| **Reconnaissance** | [Gather Victim Identity Information (T1589)](https://attack.mitre.org/techniques/T1589/) | Threat actors utilize data broker to acquire lists of target phone numbers. |
| **Reconnaissance** | [Active Scanning (T1595)](https://attack.mitre.org/techniques/T1595/) | Threat actors employ liveness scanners to actively verify which target phone numbers are valid and active before sending the malicious messages. |
| **Initial Access** | [ Phishing via Service (T1566.003)](https://attack.mitre.org/techniques/T1566/003/) | The threat actors tailored the SMS messages to the victims to compel immediate action. Using social engineering techniques to create a sense of urgency, legal jargon, and targeted personal information. |
| **Crediential Access \& Collection** | [GUI Input Capture (T1056.002)](https://attack.mitre.org/techniques/T1056/002/) | The threat actors created landing pages mimicking banks, e-commerce, customs and deliveries and government agencies sites. |

## Insights

Analyzing this report, it showed how effortlessly attackers can deploy massive, industrialized smishing campaigns and exploit human psychology. Drawing from real-world SOC experience\* analyzing phishing alerts, it is evident that while threat infrastructures constantly evolve, the primary attack vector remains human manipulation. Therefore, continuous and practical security awareness education (especially for non technical users) is a critical line of defense to increase vigilance. However, it must be layered with robust technical controls (Defense in Depth) to mitigate inevitable human errors.

*\* Real world SOC experience spoken from Daniela's POV.*





