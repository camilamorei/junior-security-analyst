# Junior Security Analyst Intro

## Introduction

This room introduces the role of a Junior Security Analyst and the daily activities performed inside a Security Operations Center (SOC).

The room provides an overview of how a SOC team works, the responsibilities of different security roles, and how a Junior Security Analyst handles security alerts and escalates suspicious activity.

## Learning Objectives

* Understand the role of a Junior Security Analyst
* Learn how a Security Operations Center (SOC) operates
* Understand the responsibilities of different SOC roles
* Learn how security alerts are investigated
* Practice escalating suspicious activity
* Understand the basic process of blocking a malicious IP address

## Task 1: Junior Security Analyst Journey

The first task introduces the Junior Security Analyst role.

A Junior Security Analyst, also known as a SOC Level 1 Analyst, is part of the first line of defense in an organization.

Typical responsibilities include:

* Monitoring security alerts
* Investigating suspicious activity
* Escalating complex incidents
* Working with other security teams
* Continuously learning about new threats and defensive techniques

The Junior Security Analyst works as part of the Security Operations Center (SOC).

## Task 2: Security Operations Center

A SOC is made up of multiple roles that work together to protect an organization.

### Senior Analyst

The Senior Analyst helps Junior Analysts with difficult cases and handles more complex security incidents after the initial investigation.

### SOC Engineer

The SOC Engineer maintains security tools and configures alerts and detection systems used by analysts.

### SOC Manager

The SOC Manager coordinates the SOC team, monitors its overall performance, and reports results to management.

### Incident Responder

The Incident Responder is called when a major security incident occurs and is responsible for responding to serious incidents.

## Task 3: A Day in the Life of a Security Analyst

This task provides a practical introduction to the daily workflow of a Security Analyst.

The lab contains a simulated security environment with several components:

* SIEM Dashboard
* IP Hunter
* Escalation
* Firewall

The SIEM dashboard contains security alerts with different severity levels. Critical alerts require investigation and may need to be escalated.

During the investigation, a suspicious IP address was identified in multiple critical alerts involving unauthorized login attempts and a successful SSH login.

The suspicious IP was:

```text
221.181.185.159
```

The alert was then escalated to the appropriate senior analyst before the IP was blocked through the firewall.

## What I Learned

This room introduced the basic workflow of a Junior Security Analyst:

```text
Security Alert
      ↓
Initial Investigation
      ↓
Identify Suspicious Activity
      ↓
Escalate When Necessary
      ↓
Take Defensive Action
      ↓
Monitor the Result
```

It also showed how different SOC roles work together during the investigation of a security event.

## Key Takeaways

* A SOC is responsible for monitoring and defending an organization's environment.
* Junior Security Analysts are usually responsible for the initial investigation of alerts.
* Critical alerts require careful investigation and appropriate escalation.
* Senior Analysts help with complex security cases.
* SOC Engineers maintain and configure security tools.
* Incident Responders handle major security incidents.
* Blocking a malicious IP can be one of the defensive actions taken during an investigation.

## Conclusion

The Junior Security Analyst Intro room provided a practical introduction to working in a SOC environment.

The lab demonstrated how an analyst can investigate alerts, identify malicious activity, escalate an incident, and take defensive action using security tools.

This room serves as an introduction to the responsibilities and workflow that will be explored in greater depth throughout the Junior Security Analyst learning path.
