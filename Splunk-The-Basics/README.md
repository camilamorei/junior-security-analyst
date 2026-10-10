# Splunk: The Basics

## Overview

This room introduces Splunk, a platform used to search, monitor, and analyze machine-generated data. It covers the main Splunk components, interface navigation, and the process of ingesting and searching log data.

Splunk is widely used in Security Operations Centers (SOCs) to investigate security events, identify suspicious activity, and support incident response.

## Learning Objectives

- Understand the main components of Splunk.
- Navigate the Splunk web interface.
- Learn how data is added to Splunk.
- Upload and search log data.
- Use basic Search Processing Language (SPL) queries to analyze events.
- Understand how Splunk can support security investigations.

## Main Splunk Components

Splunk environments can use different components to collect, process, and search machine data.

- Splunk Forwarder: Collects and forwards data from a source machine to a Splunk instance.
- Splunk Indexer: Processes and stores incoming data, making it searchable.
- Splunk Search Head: Provides the interface used to search, analyze, and visualize indexed data.

These components work together to make log analysis and security monitoring possible.

## Navigating Splunk

The Splunk web interface provides access to search tools, data ingestion settings, and other features.

The Search and Reporting application is used to run SPL queries and investigate events.

The Add Data section provides options for ingesting data, including uploading files and monitoring files or network ports.

## Adding Data

The room introduced the process of uploading a log file into Splunk.

The main steps were:

1. Open the Add Data section.
2. Select the Upload option to import a local file.
3. Select the log file.
4. Configure the source type, such as JSON.
5. Select or configure the destination index.
6. Review the settings and complete the ingestion process.
7. Open Search and Reporting to query the imported events.

For the practical exercise, VPN connection logs were uploaded into the `VPN_Logs` index.

## Searching and Analyzing VPN Logs

Search Processing Language (SPL) is used to search and analyze data in Splunk.

### Count all events

```spl
index=VPN_Logs
| stats count
```

### Find events associated with a username

```spl
index=VPN_Logs
| spath
| search UserName="Maleena"
| stats count
```

### Identify the username associated with an IP address

```spl
index=VPN_Logs
| spath
| search Source_ip="107.14.182.38"
| stats values(UserName) as UserName count
```

### Count events from countries other than France

```spl
index=VPN_Logs
| spath
| search Source_Country!="France"
| stats count
```

### Count VPN events associated with an IP address

```spl
index=VPN_Logs
| spath
| search Source_ip="107.3.206.58"
| stats count
```

The `index` field limits the search to a specific index. The `search` command filters events, `stats` calculates results, and `spath` extracts fields from structured data such as JSON when necessary.

## Key Takeaways

- Splunk can collect and analyze machine-generated data.
- Forwarders, indexers, and search heads have different roles in a Splunk environment.
- Data must be ingested into Splunk before it can be searched.
- Indexes help organize and retrieve ingested events.
- SPL makes it possible to filter events, count records, and investigate activity involving users, IP addresses, and geographic locations.
- SIEM tools like Splunk help security analysts investigate logs and detect potentially suspicious behavior.

## Skills Practiced

- Splunk interface navigation
- Log ingestion and data configuration
- Basic SPL queries
- JSON field extraction
- Event filtering and counting
- VPN log analysis
- Introductory SIEM investigation

## Conclusion

This room provided a foundation for using Splunk as a SIEM tool. By exploring its components, navigating the interface, ingesting VPN logs, and running basic SPL searches, I practiced the initial steps involved in analyzing security events.

These skills provide a starting point for more advanced Splunk investigations, detection engineering, and incident response.
