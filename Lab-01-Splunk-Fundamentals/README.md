---
layout: default
title: Splunk Fundamentals Lab
---

# Splunk Fundamentals Lab (Search, Analysis, Dashboards & Alerting)

This lab documents hands-on Splunk fundamentals completed as part of self-directed cybersecurity training and SOC-focused practice.

The purpose of this lab is to demonstrate understanding of **SIEM fundamentals** and hands-on ability to:
- ingest and analyse log data;
- write SPL queries;
- extract fields for investigations;
- create dashboards and alerts relevant to SOC operations.

---

## Lab Environment

**Hypervisor**
- Oracle VirtualBox

**Virtual Machines**
- Windows Server 2022 (Splunk Enterprise)

**Software**
- Splunk Enterprise
- Splunk Web (Search & Reporting app)

**Datasets**
- BOTSv3 dataset
- DNS log dataset

---

## Objectives

This lab demonstrates the ability to:

1. Install and validate Splunk Enterprise;
2. Upload and search log data;
3. Use SPL for analysis and aggregation;
4. Extract fields from raw log events;
5. Perform DNS investigation workflows;
6. Create dashboards and alerts based on security logic.

---

## Lab Tasks and Implementation

### 1. Splunk Enterprise Installation
- Installed Splunk Enterprise on Windows Server 2022;
- Verified Splunk service status;
- Confirmed access to Splunk Web interface.

![Splunk installation](Images/lab01-01-splunk-install.png)

---

### 2. Data Upload (BOTSv3 Dataset)
- Uploaded BOTSv3 dataset into Splunk;
- Confirmed events were indexed and searchable.

---

### 3. SPL Fundamentals & Initial Analysis
- Used basic SPL commands (stats, sort, head) to perform an initial analysis of data

---

### 4. DNS Log Analysis & Field Extraction


### 4.1 Field Extraction
Extracted meaningful fields from DNS logs to support investigations:
- Source IP;
- Destination IP;
- Destination port;
- Queried domain.


### 4.2 Top Queried Domains
Identified 20 most frequently queried domains.


### 4.3 Suspicious Domain Investigation
- Identified suspicious domain based on frequency and naming pattern;
- Pivoted from domain to associated IP addresses.


### 5. Alert Creation (Processes Executed Before 8AM)
Created an alert to detect processes launched outside normal business hours.
- Configured scheduled alert;
- Defined trigger conditions;
- Verified alert logic using historical data.


### 6. Reporting & Dashboard
Built reports and dashboards to monitor VPN activity and authentication results.


### Key Skills Demonstrated
- SIEM fundamentals (Splunk);
- Log ingestion and validation;
- SPL querying and aggregation;
- Field extraction for investigations;
- DNS and process execution analysis;
- Alerting and dashboard creation;
- SOC-relevant investigative workflows.

---

###Disclaimer

All systems and data used in this lab are non-production, isolated, and for educational purposes only.
No real user data or sensitive information was used.
