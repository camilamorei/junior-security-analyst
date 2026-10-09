# Introduction to EDR

## Overview

This room introduces Endpoint Detection and Response (EDR), a security solution used by Security Operations Center (SOC) analysts to monitor endpoints, detect suspicious activity, and investigate potential security incidents.

The room covers EDR architecture, endpoint telemetry, detection capabilities, and alert investigation through a simulated EDR console.

## Key Topics

### 1. What Is EDR?

Endpoint Detection and Response (EDR) continuously monitors endpoint activity to identify suspicious behavior and provide detailed information for security investigations.

Unlike traditional antivirus solutions, EDR provides broader visibility into endpoint activity, helping analysts understand how processes, files, network connections, and other system events are related.

### 2. EDR vs. Antivirus

Traditional antivirus solutions primarily focus on identifying and blocking known malware. EDR provides additional monitoring and investigation capabilities, allowing analysts to examine suspicious behavior and reconstruct events.

Key differences include:

- Continuous endpoint monitoring
- Detailed process and activity visibility
- Investigation of suspicious behavior
- Detection of threats that may evade traditional antivirus
- Support for incident investigation and response

### 3. EDR Architecture

EDR solutions use endpoint components to collect telemetry and send relevant information to a central platform.

The agent, also known as a sensor, collects endpoint activity and provides data that analysts can use to investigate detections.

### 4. EDR Telemetry

EDR telemetry provides visibility into endpoint activity, including:

- Process creation and execution
- File activity
- Network connections
- Windows Registry activity
- Parent and child process relationships
- Suspicious command execution

This information helps analysts understand what happened on an endpoint and identify potentially malicious activity.

### 5. Detection Capabilities

EDR platforms use different detection methods to identify potential threats, including:

- Behavioral detection
- Indicators of Compromise (IOC) matching
- Anomaly detection
- Threat intelligence
- Machine learning
- Mapping activity to the MITRE ATT&CK framework

IOC matching compares observed activity against known indicators associated with malicious activity. Behavioral detection identifies suspicious actions or sequences of events.

### 6. Alert Investigation

The practical exercise involved investigating alerts in a simulated EDR console.

The investigation focused on identifying:

- A tool launched by CMD.exe to download a payload
- The absolute path of a downloaded file
- The location of a suspicious executable
- A URL associated with a possible data exfiltration attempt
- Threat intelligence information associated with a process

This exercise demonstrated how endpoint telemetry and alert context help analysts investigate suspicious activity.

## Key Takeaways

- EDR provides deeper endpoint visibility than traditional antivirus alone.
- Agents, also called sensors, collect endpoint telemetry.
- Process relationships help analysts understand how suspicious activity started.
- Network connections, Registry activity, and file events are valuable sources of evidence.
- IOC matching and behavioral detection help identify potential threats.
- Alert investigation requires correlating multiple pieces of endpoint evidence.

## Skills Practiced

- Understanding EDR architecture
- Identifying endpoint telemetry sources
- Understanding detection techniques
- Investigating process execution and file paths
- Examining network activity
- Using threat intelligence context
- Performing initial SOC alert triage

## Conclusion

This room provided an introduction to Endpoint Detection and Response and its role in security operations. Understanding EDR telemetry and detection capabilities is an important foundation for investigating endpoint alerts and developing practical SOC analyst skills.

## Resources

- TryHackMe: Introduction to EDR
- MITRE ATT&CK: https://attack.mitre.org/
