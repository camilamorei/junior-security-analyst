# SOC Metrics and Objectives

## Overview

This room explores the key metrics used by Security Operations Center (SOC) teams to measure performance, evaluate alert handling, identify operational problems, and improve threat detection and response.

It covers internal SOC metrics, Service Level Agreements (SLAs), and practical scenarios involving alert delays, false positives, and analyst workload.

## Key Topics

### 1. Key SOC Metrics

- **Alert Count (AC):** Measures the total number of alerts received by the SOC.
- **False Positive Rate (FPR):** Measures the proportion of alerts incorrectly classified as threats.
- **Alert Escalation Rate (AER):** Measures the proportion of alerts escalated to higher-level analysts.
- **Threat Detection Rate (TDR):** Measures the proportion of threats successfully detected by the SOC.

### 2. Triage Metrics

- **Mean Time to Detect (MTTD):** Average time between the beginning of an attack and its detection.
- **Mean Time to Acknowledge (MTTA):** Average time between an alert being generated and an analyst beginning triage.
- **Mean Time to Respond (MTTR):** Average time required for the SOC to respond to a threat and prevent further damage.
- **SOC Availability:** Defines the hours during which the SOC operates, such as 8/5 or 24/7.

These metrics can be incorporated into Service Level Agreements (SLAs) to establish expectations for detection, acknowledgment, and response times.

### 3. Improving SOC Metrics

Common problems and potential improvements include:

- **High False Positive Rate:** Review detection rules, exclude trusted activity when appropriate, and automate repetitive alert triage.
- **High MTTD:** Review detection rule execution frequency and verify that logs are collected without unnecessary delays.
- **High MTTA:** Improve real-time notifications and distribute alerts more evenly among analysts.
- **High MTTR:** Escalate threats promptly, document response procedures, and prepare playbooks for common attack scenarios.

### 4. Practical Scenarios

The practical exercises focused on identifying problematic metrics and assigning appropriate improvement tasks and responsibilities.

Scenarios included:

- Reducing response delays by documenting procedures for credential rotation and assigning research tasks to experienced analysts.
- Improving threat detection speed by reviewing SIEM detection schedules and involving the responsible SOC engineer.
- Reducing false positives caused by system activity and IT noise by reviewing detection rules and assigning remediation tasks to the appropriate team members.

## Key Takeaways

- SOC metrics help evaluate operational efficiency and identify weaknesses in security monitoring.
- A high volume of alerts does not necessarily indicate a high number of genuine threats.
- Excessive false positives can increase analyst workload and cause alert fatigue.
- Timely detection, acknowledgment, and response are essential to limiting the impact of security incidents.
- Improving SOC performance requires collaboration between L1 analysts, L2 analysts, SOC engineers, and management.
- Metrics should be monitored continuously and used to guide practical improvements.

## Skills Practiced

- Understanding SOC performance metrics.
- Calculating false positive rates.
- Differentiating MTTD, MTTA, and MTTR.
- Understanding SLAs and SOC availability.
- Identifying alert triage and response bottlenecks.
- Recommending improvements to SIEM detection rules and notification systems.
- Assigning remediation tasks to appropriate SOC team members.

## Conclusion

This room provided an introduction to the metrics used to evaluate SOC performance and the processes used to improve threat detection and incident response. Understanding these measurements helps SOC analysts identify operational weaknesses, communicate problems effectively, and contribute to a more efficient security operations team.

## Resources

- [TryHackMe](https://tryhackme.com/)
- [NIST Computer Security Incident Handling Guide (SP 800-61 Rev. 2)](https://csrc.nist.gov/pubs/sp/800/61/r2/final)
