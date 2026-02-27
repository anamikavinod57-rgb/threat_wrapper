#  Threat Intel Mini Aggregator

A structured Threat Intelligence Dashboard built to simulate real-world SOC indicator triage and correlation workflows.

---

##  Executive Summary

Threat Intel Mini Aggregator is a locally deployed cybersecurity intelligence platform that aggregates data from multiple public threat intelligence sources and transforms it into a normalized, risk-scored analysis report.

This project was designed to bridge the gap between theoretical cybersecurity knowledge and practical analyst workflows.

---

##  Core Objective

Modern Security Operations Centers rely on correlating multiple intelligence feeds to make informed decisions.

This application replicates that process by:

- Collecting intelligence from multiple APIs
- Normalizing inconsistent data formats
- Applying weighted threat scoring logic
- Presenting actionable results in a structured dashboard

The goal is not just to query APIs — but to simulate analyst reasoning.

---

##  Supported Indicators

The system can analyze:

- SHA256 File Hashes  
- IPv4 Addresses  
- Domain Names  

Indicator type detection can be manual or automatic.

---

##  Intelligence Sources

The aggregator integrates:

- **VirusTotal** – Multi-engine malware and reputation analysis  
- **MalwareBazaar** – Malware sample intelligence database  

Each source is queried independently, then correlated into a unified internal data structure.

---

##  System Design

### Architecture Philosophy

This project follows a layered design approach:

1. **Input Validation Layer**  
   Sanitizes and validates indicators.

2. **Service Layer**  
   Handles API requests and response parsing.

3. **Normalization Layer**  
   Converts heterogeneous API schemas into a standard internal format.

4. **Correlation & Risk Engine**  
   Applies weighted logic to calculate final threat levels.

5. **Presentation Layer**  
   Renders results using a professional SOC-style interface.

This modular design allows easy expansion to additional threat feeds.

---

##  Risk Scoring Model

Rather than relying purely on raw detection counts, the risk engine applies weighted intelligence indicators:

- High malicious detection threshold increases severity
- Malware family attribution adds contextual risk
- Ransomware tagging escalates urgency
- Suspicious classifications increase monitoring priority

Risk levels are classified as:

- LOW  
- MEDIUM  
- HIGH  

This provides triage-level decision support.

---

##  User Interface Features

- Dark-themed SOC-style dashboard
- Detection ratio visualization
- Aggregated threat summary
- Raw JSON inspection option
- Clean indicator result presentation

The interface is intentionally structured to mimic real threat analysis tools.

---

##  Technology Stack

- Python
- Flask
- REST API Integration
- Environment Variable Configuration
- Chart.js (Frontend Visualization)

---

##  Secure Configuration

- API keys stored in `.env`
- Sensitive credentials excluded from version control
- Local execution to reduce exposure risk
- Input validation to prevent malformed queries

---

##  Educational & Practical Value

This project demonstrates competency in:

- RESTful API integration
- Backend service abstraction
- Data normalization strategies
- Risk modeling logic
- Secure credential handling
- Practical SOC workflow simulation

It serves as both a learning platform and a portfolio-ready cybersecurity automation project.

---

##  Planned Enhancements

- Multi-source expansion (OTX, AbuseIPDB, etc.)
- Historical query logging
- Intelligent caching layer
- Report export functionality
- Optional authentication system

---

##  Author

Anamika Vinod  
Cybersecurity Enthusiast | Threat Analysis Learner  

Focused on automation, intelligence correlation, and practical defensive security tools.

---

##  Disclaimer

This tool is built for educational and defensive security purposes only.  
Users are responsible for complying with API usage policies and ethical cybersecurity practices.
