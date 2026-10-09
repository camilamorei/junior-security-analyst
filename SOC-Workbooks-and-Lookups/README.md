# SOC Workbooks and Lookups

## Overview

This room explores how SOC analysts use workbooks, asset inventories, identity inventories, and network diagrams to investigate security alerts. It focuses on gathering context, following structured investigation procedures, and making informed decisions during alert triage.

## Learning Objectives

- Understand the purpose of SOC investigation workbooks
- Learn how to use identity and asset inventories
- Understand how network diagrams support security investigations
- Learn the stages of a structured investigation workflow
- Practice building workbooks through an interactive interface

## Tasks Completed

### Task 1: Introduction

Reviewed the role of workbooks and lookup resources in SOC investigations and learned how they help analysts investigate alerts consistently.

### Task 2: Assets and Identities

Learned the difference between identity inventory and asset inventory and how each supports alert triage.

Identity inventory provides information about users, service accounts, roles, permissions, and locations.

Asset inventory provides information about systems and devices, including hostnames, IP addresses, operating systems, owners, and purposes.

Key concepts:
- User and service account identification
- Host and server identification
- Access permissions and business context
- Asset ownership and purpose

### Task 3: Network Diagrams

Studied how network diagrams help analysts understand network topology, subnet relationships, exposed services, and suspicious communication between systems.

The investigation scenario involved a potential VPN brute-force attack followed by internal network scanning.

Key concepts:
- VPN services and exposed ports
- Internal and external IP addresses
- Network segmentation and subnets
- Suspicious network reconnaissance
- True Positive and False Positive classification

### Task 4: Workbooks Theory

Learned how SOC workbooks, also known as playbooks, runbooks, or workflows, provide structured procedures for investigating and responding to security alerts.

The investigation process was divided into three stages:

1. Enrichment: Gather additional context using threat intelligence, identity inventories, and asset lookups.
2. Investigation: Analyze the collected information and relevant security logs to determine whether the activity is suspicious.
3. Escalation: Escalate alerts to senior analysts or contact the relevant parties when further investigation is required.

BambooHR was presented as an example of an identity inventory source.

### Task 5: Workbook Practice

Practiced building investigation workbooks using an interactive interface by arranging investigation steps in the correct order.

This exercise demonstrated how structured workflows can help analysts follow consistent procedures and avoid missing important investigation steps.

### Task 6: Conclusion

Reviewed the importance of using existing lookup resources and maintaining investigation workbooks to improve the efficiency and consistency of SOC operations.

## Key Takeaways

- Identity inventories provide context about users, roles, and access permissions.
- Asset inventories help identify the purpose, ownership, and configuration of systems.
- Network diagrams help explain communication paths and relationships between subnets.
- Threat intelligence and lookups support the enrichment stage of alert triage.
- Workbooks provide repeatable procedures for investigating suspicious activity.
- Structured investigations help reduce errors and support evidence-based verdicts.
- Escalation ensures that complex or high-risk alerts receive appropriate attention.

## Skills Practiced

- SOC alert enrichment
- Identity and asset lookups
- Network diagram analysis
- Subnet identification
- Security alert investigation
- Workbook and playbook workflows
- True Positive and False Positive classification
- SOC investigation documentation

## Tools and Resources

- TryHackMe interactive SOC workbook interface
- Identity inventory concepts
- Asset inventory concepts
- Network diagrams
- Threat intelligence resources
- SOC investigation workflows

## Conclusion

This room improved my understanding of how SOC analysts gather contextual information and use structured workbooks to investigate security alerts. Combining identity lookups, asset inventories, network diagrams, and repeatable investigation procedures helps analysts make more informed decisions and handle alerts consistently.

Room: SOC Workbooks and Lookups  
Platform: TryHackMe
