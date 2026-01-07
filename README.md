# Log-Management-Detection-Alerting
Deploying a SIEM Solution &amp; Integrating Sophos Central
Project Overview

This project involved deploying ManageEngine Log360 (SIEM) and integrating it with a Sophos Central trial account to collect, analyze, and report on security events. The goal was to achieve centralized monitoring, detection, reporting, and alerting for endpoint security incidents such as malware detections and user activity.

🎯 Objectives

Deploy a functional SIEM solution (Log360)

Integrate Sophos Central using secure API-based log ingestion

Collect and parse security logs in CEF format

Generate reports and configure alerting for high-severity events

🛠 Tools & Technologies

ManageEngine Log360 (SIEM)

Sophos Central (Endpoint Security Platform)

Kali Linux

Python (Virtual Environment)

Sophos Central SIEM Integration Script

Syslog (CEF format)

⚙️ Implementation Steps

Deployed ManageEngine Log360 SIEM platform.

Registered for a Sophos Central trial account.

Generated API credentials via Sophos Central’s secure API portal.

Downloaded the Sophos SIEM integration script:
https://github.com/sophos/Sophos-Central-SIEM-Integration

Configured a Python virtual environment and installed required dependencies (requests, PyJWT, syslogcef).

Executed the integration script to fetch logs from Sophos Central and forward them to Log360 via syslog in CEF format.

Added Sophos Central as a new syslog device in Log360.

Triggered malware detections using the EICAR test string to validate log ingestion.

Created custom reports:

Blocked Malware Events

Top Users with Security Alerts

Configured email alerts for high-severity malware detections.

📊 Findings & Results

Sophos Central successfully transmitted logs in CEF format

Log360 parsed and stored Sophos logs accurately

Malware events triggered via EICAR were visible in the SIEM

Reports provided clear visibility into malware activity and affected users

Alerting enabled proactive incident response

⚠️ Challenges Faced

Cloning the integration repository into a non-empty directory

Filtering excessive syslog noise (cron, PAM, systemd events)

Initial delay in Sophos device visibility within Log360

Understanding Log360 field mappings (suser, dhost)

Designing meaningful alert message formats

🧠 Key Learnings

Practical SIEM deployment and configuration

API-based log ingestion and syslog forwarding

Real-world detection validation using safe test malware

Importance of alert tuning and log filtering

📄 Supporting Documentation

Detailed Report & Artifacts:
https://drive.google.com/drive/folders/1mCAgA8cjGWM8w_oO0UyplftHM5wk4vaX

https://drive.google.com/drive/folders/1t-Hzpncgrkvcz8KehJSbgysNlGb5cUhW
