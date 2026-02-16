# Lab 03 — ELK Installation & Web Attack Investigation 🧠🔎

**Platform:** TryHackMe  
**Rooms Used:** Logstash + Slingshot  
**Focus:** SIEM deployment and web attack investigation using ELK Stack

---

## Objective

This lab demonstrates the ability to:

- deploy and configure a full ELK stack (Elasticsearch, Logstash, Kibana);
- investigate malicious activity through log analysis;
- identify attacker behaviour and post-exploitation actions.

The scenario simulates a compromised web server and requires performing a structured SOC investigation using Kibana.

---

## Lab Environment

- Linux server hosting ELK
- Apache web logs ingested via Logstash
- Kibana used as investigation interface
- Simulated attacker activity dataset

All work performed in an isolated lab environment using simulated data.

---

## Part 1 — ELK Stack Deployment

### 1. Elasticsearch Installation
Installed Elasticsearch and verified service availability.

📸 Evidence: `Images/1.1`

---

### 2. Service Configuration
Configured network binding and HTTP port in configuration file.

📸 Evidence: `Images/02_elasticsearch_config.png`

---

### 3. Logstash Installation
Installed Logstash and verified service status.

📸 Evidence: `Images/03_logstash_status.png`

---

### 4. Logstash Configuration
Configured pipeline to ingest web server logs.

📸 Evidence: `Images/04_logstash_pipeline.png`

---

### 5. Kibana Installation
Installed Kibana and verified service availability.

📸 Evidence: `Images/05_kibana_status.png`

---

### 6. Kibana Configuration
Configured Kibana to connect to Elasticsearch.

📸 Evidence: `Images/06_kibana_config.png`

---

### 7. Stack Validation
Confirmed data ingestion and dashboard accessibility.

📸 Evidence: `Images/07_kibana_dashboard.png`

---

## Part 2 — Security Investigation

Scenario: suspicious activity detected on a web server.

Investigation performed using filtering, aggregation and pivoting techniques in Kibana Discover.

---

### Attacker Identification
Identified excessive requests targeting authentication endpoints.

📸 Evidence: `Images/08_attacker_ip.png`

---

### Enumeration Activity
Detected directory enumeration behaviour and identified tool used.

📸 Evidence: `Images/09_enumeration.png`

---

### Failed Resource Requests
Filtered HTTP 404 responses to determine unsuccessful probing attempts.

📸 Evidence: `Images/10_failed_requests.png`

---

### Credential Access
Observed brute-force login behaviour and extracted credentials.

📸 Evidence: `Images/11_credentials.png`

---

### Web Shell Execution
Confirmed command execution following compromise.

📸 Evidence: `Images/12_webshell.png`

---

### Data Access
Identified database access and extraction activity via application endpoints.

📸 Evidence: `Images/13_database_access.png`

---

### Persistence / Post-Exploitation
Tracked attacker actions after gaining administrative privileges.

📸 Evidence: `Images/14_post_exploitation.png`

---

## Key Investigation Techniques Demonstrated

- Filtering by IP and HTTP method
- User-Agent analysis
- Status code analysis (200 / 404 / POST)
- Pattern detection (directory traversal)
- Credential discovery
- Post-exploitation tracking

---

## Skills Demonstrated

- SIEM deployment (ELK)
- Log ingestion troubleshooting
- Web attack investigation workflow
- Attacker behaviour analysis
- Evidence-based reporting

---

## Conclusion

This lab demonstrates practical blue-team investigation workflow:

1. Deploy monitoring infrastructure
2. Detect suspicious behaviour
3. Identify attacker activity
4. Track compromise progression
5. Determine impact

The workflow mirrors a real SOC triage and incident investigation process.
