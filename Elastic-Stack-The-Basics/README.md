# Elastic Stack: The Basics

## Overview

This room introduces the Elastic Stack (ELK), a collection of tools used to collect, process, store, search, analyze, and visualize large volumes of data.

Although the Elastic Stack is not a traditional SIEM solution, many Security Operations Center (SOC) teams use it for security monitoring, log analysis, and incident investigation.

The room focuses on the main Elastic Stack components, searching and filtering VPN logs, investigating failed connection attempts, and creating visualizations and dashboards with Kibana.

## Learning Objectives

- Understand the main components of the Elastic Stack.
- Explore Kibana and its main features.
- Search and filter logs using Kibana Query Language (KQL).
- Investigate VPN connection logs and identify anomalies.
- Create visualizations and dashboards for security monitoring.

## Elastic Stack Components

### Elasticsearch

Elasticsearch is a search and analytics engine that stores, searches, and analyzes data in JSON document format. It allows analysts to retrieve relevant information from large datasets.

### Logstash

Logstash is a data processing pipeline that collects data from different sources, transforms and normalizes it, and sends it to a destination.

A Logstash configuration consists of three main sections:

- Input: Defines where the data comes from.
- Filter: Processes, parses, or normalizes incoming data.
- Output: Specifies where the processed data is sent.

### Beats

Beats are lightweight agents installed on endpoints or servers to collect and forward specific types of data to Elasticsearch or Logstash.

Examples include:

- Winlogbeat: Collects Windows event logs.
- Filebeat: Collects and forwards log files.
- Packetbeat: Collects and analyzes network traffic.
- Metricbeat: Collects system and service metrics.

### Kibana

Kibana is a web-based interface used to search, analyze, and visualize data stored in Elasticsearch.

Its main features include:

- Discover: Search and investigate raw events.
- Visualizations: Represent data using tables, charts, and other formats.
- Dashboards: Combine saved searches and visualizations into a single interface.

## How the Components Work Together

A typical Elastic Stack workflow follows these steps:

1. Beats collect data from endpoints and other sources.
2. Logstash processes and normalizes the collected data when needed.
3. Elasticsearch stores and indexes the data.
4. Kibana allows analysts to search, investigate, and visualize the indexed data.

This workflow helps SOC analysts investigate events and identify suspicious patterns.

## Discover Tab

The Discover interface is one of the main workspaces for log analysis in Kibana.

Important features include:

- Index patterns or data views: Define which Elasticsearch data is available for exploration.
- Search bar: Allows analysts to search and filter events.
- Field panel: Displays fields extracted from the available logs.
- Time filter: Restricts results to a specific time range.
- Timeline: Shows the distribution of events over time.
- Add filter: Applies filters to specific fields.
- Saved searches: Preserve useful queries and selected fields for later use.

For the practical exercises, the `vpn_connections` data view was used to investigate VPN activity from January 2022.

## Kibana Query Language (KQL)

KQL is used to search and filter documents in Kibana.

### Free-text search

Search for a term across available fields:

```kql
United States
```

### Wildcard search

Use an asterisk to match additional characters:

```kql
United*
```

### Logical operators

Combine search conditions using `AND`, `OR`, and `NOT`.

```kql
"United States" AND "Virginia"
```

```kql
"United States" OR "England"
```

```kql
"United States" AND NOT "Florida"
```

### Field-based search

Search for a specific value in a field:

```kql
Source_ip : 238.163.231.224 AND UserName : Suleman
```

### Filter by country and users

```kql
Source_Country : "United States" AND (UserName : "James" OR UserName : "Albert")
```

### Investigate VPN activity after a specific date

```kql
UserName : "Johny Brown" AND @timestamp > "2022-01-01T00:00:00.000Z"
```

The selected time range must include the period being investigated. Field names and values must match the data available in the selected data view.

## Visualizations

Kibana allows analysts to transform log data into visual representations that make patterns easier to identify.

The room introduced:

- Tables for comparing field values.
- Pie charts for visualizing distributions.
- Correlations between fields such as source IP addresses and countries.
- Saved visualizations for reuse in dashboards.

### Investigating Failed VPN Connections

The exercise focused on identifying failed VPN connection attempts.

The investigation involved:

1. Selecting the `vpn_connections` data view.
2. Setting the time range to include January 2022.
3. Filtering the `action` field to show only `failed` events.
4. Using `UserName` and `Source_ip` to identify affected users and source addresses.
5. Creating and saving a table to summarize the results.

This approach helps analysts identify users or IP addresses associated with repeated failed authentication attempts.

## Dashboards

Dashboards combine saved searches and visualizations into a single workspace.

The dashboard creation process involved:

1. Opening the Dashboard tab.
2. Creating a new dashboard.
3. Selecting Add from Library.
4. Adding previously saved searches and visualizations.
5. Organizing the panels.
6. Saving the dashboard.

A dashboard can provide a consolidated view of VPN activity and help analysts identify unusual patterns more efficiently.

## Key Takeaways

- The Elastic Stack can support security monitoring and log investigations.
- Elasticsearch stores and indexes data for searching and analysis.
- Logstash processes and transforms data.
- Beats collect and forward data from endpoints.
- Kibana provides search, visualization, and dashboard capabilities.
- KQL allows analysts to filter logs using field-based and free-text queries.
- Visualizations and dashboards help summarize activity and identify potential anomalies.
- Investigating failed VPN connections is an example of how log analysis supports SOC operations.

## Skills Practiced

- Elastic Stack fundamentals
- Elasticsearch and Kibana concepts
- Log analysis and investigation
- Kibana Query Language (KQL)
- VPN connection analysis
- Failed authentication investigation
- Data visualization
- Dashboard creation

## Conclusion

This room provided a practical introduction to the Elastic Stack and its use in security operations. By exploring the main components, searching VPN logs, filtering failed connection attempts, and creating visualizations and dashboards, I gained foundational experience with a technology commonly used for log analysis and security monitoring.

These skills provide a foundation for further study of SIEM platforms, detection engineering, and incident response.
