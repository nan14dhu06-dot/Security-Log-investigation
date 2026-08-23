🔐 Security Log Investigation

📌 Project Overview

This project analyzes a synthetic authentication log to identify suspicious login behavior, detect potential brute-force and password-spraying attacks, reconstruct a likely incident timeline, and recommend appropriate incident-response actions.

The investigation demonstrates how raw authentication events can be transformed into structured security findings using Python, Pandas, Excel, and automated reporting.

«⚠️ Disclaimer: This project uses synthetic data for educational and cybersecurity-training purposes. It does not represent a real security incident.»

---

🎯 Objectives

- Normalize authentication log data.
- Analyze usernames, source IPs, actions, and authentication results.
- Detect potential brute-force attacks.
- Detect potential password-spraying activity.
- Identify successful authentication following suspicious failures.
- Reconstruct an incident timeline.
- Separate evidence from assumptions.
- Generate an investigation spreadsheet.
- Generate an incident-report PDF.
- Recommend containment and improved security controls.

---

🛠️ Technologies Used

Technology| Purpose
Python| Automated log analysis
Pandas| Data processing and analysis
OpenPyXL| Excel investigation report generation
ReportLab| PDF incident report generation
Microsoft Excel| Log review and visualization
Visual Studio Code| Development environment
GitHub| Project documentation and version control

---

📂 Project Structure

security-log-investigation/
│
├── README.md
│
├── logs/
│   └── authentication.csv
│
├── output/
│   ├── investigation.py
│   └── investigation.xlsx
│
├── reports/
│   └── Security_Log_Investigation_Complete_Report.pdf
│
├── screenshots/
│   ├── normalized-log.jpg
│   ├── project-structure.jpg
│   └── execution-output.jpg
│
└── requirements.txt

---

📊 Dataset

The investigation uses 15 synthetic authentication events containing fields such as:

timestamp
username
source_ip
action
result

Example:

username,source_ip,action,result
john,192.168.1.x,LOGIN,SUCCESS
admin,185.10.20.x,LOGIN,FAILED
admin,185.10.20.x,LOGIN,FAILED
admin,185.10.20.x,LOGIN,SUCCESS
admin,185.10.20.x,ACCESS,SUCCESS

---

🔍 Investigation Findings

1. Potential Brute-Force Activity

Multiple failed authentication attempts were recorded against the "admin" account from the same source-IP prefix:

185.10.20.x

The sequence contains repeated failures followed by a successful login.

Assessment

This pattern is consistent with potential brute-force authentication activity.

---

2. Potential Password Spraying

The source-IP prefix:

185.55.22.x

was associated with failed authentication attempts against multiple accounts:

bob
alice
john
david
sarah

Assessment

Multiple accounts being targeted from one source is consistent with a possible password-spraying attack.

---

3. Successful Authentication After Failures

The "admin" account successfully authenticated after several failed attempts.

A subsequent:

ACCESS → SUCCESS

event was also recorded.

Assessment

This requires investigation for possible account compromise.

However, the available authentication logs alone do not prove:

- Attacker identity
- Credential theft
- Malicious intent
- Data access
- Data exfiltration

Additional evidence is required.

---

🕒 Incident Timeline

Normal successful authentication
              ↓
Repeated failed admin logins
              ↓
Potential brute-force activity
              ↓
Successful admin authentication
              ↓
Successful admin access event
              ↓
Multiple-account failures from another source
              ↓
Potential password-spraying activity

---

🚨 Detection Logic

Brute-Force Detection

IF
multiple failed logins
against the same account
from the same source
within a short time period

THEN
flag as potential brute-force activity.

Password-Spraying Detection

IF
one source targets multiple accounts
AND produces repeated authentication 🔐 Security Log Investigation

📌 Project Overview

This project analyzes a synthetic authentication log to identify suspicious login behavior, detect potential brute-force and password-spraying attacks, reconstruct a likely incident timeline, and recommend appropriate incident-response actions.

The investigation demonstrates how raw authentication events can be transformed into structured security findings using Python, Pandas, Excel, and automated reporting.

«⚠️ Disclaimer: This project uses synthetic data for educational and cybersecurity-training purposes. It does not represent a real security incident.»

---

🎯 Objectives

- Normalize authentication log data.
- Analyze usernames, source IPs, actions, and authentication results.
- Detect potential brute-force attacks.
- Detect potential password-spraying activity.
- Identify successful authentication following suspicious failures.
- Reconstruct an incident timeline.
- Separate evidence from assumptions.
- Generate an investigation spreadsheet.
- Generate an incident-report PDF.
- Recommend containment and improved security controls.

---

🛠️ Technologies Used

Technology| Purpose
Python| Automated log analysis
Pandas| Data processing and analysis
OpenPyXL| Excel investigation report generation
ReportLab| PDF incident report generation
Microsoft Excel| Log review and visualization
Visual Studio Code| Development environment
GitHub| Project documentation and version control

---

📂 Project Structure

security-log-investigation/
│
├── README.md
│
├── logs/
│   └── authentication.csv
│
├── output/
│   ├── investigation.py
│   └── investigation.xlsx
│
├── reports/
│   └── Security_Log_Investigation_Complete_Report.pdf
│
├── screenshots/
│   ├── normalized-log.jpg
│   ├── project-structure.jpg
│   └── execution-output.jpg
│
└── requirements.txt

---

📊 Dataset

The investigation uses 15 synthetic authentication events containing fields such as:

timestamp
username
source_ip
action
result

Example:

username,source_ip,action,result
john,192.168.1.x,LOGIN,SUCCESS
admin,185.10.20.x,LOGIN,FAILED
admin,185.10.20.x,LOGIN,FAILED
admin,185.10.20.x,LOGIN,SUCCESS
admin,185.10.20.x,ACCESS,SUCCESS

---

🔍 Investigation Findings

1. Potential Brute-Force Activity

Multiple failed authentication attempts were recorded against the "admin" account from the same source-IP prefix:

185.10.20.x

The sequence contains repeated failures followed by a successful login.

Assessment

This pattern is consistent with potential brute-force authentication activity.

---

2. Potential Password Spraying

The source-IP prefix:

185.55.22.x

was associated with failed authentication attempts against multiple accounts:

bob
alice
john
david
sarah

Assessment

Multiple accounts being targeted from one source is consistent with a possible password-spraying attack.

---

3. Successful Authentication After Failures

The "admin" account successfully authenticated after several failed attempts.

A subsequent:

ACCESS → SUCCESS

event was also recorded.

Assessment

This requires investigation for possible account compromise.

However, the available authentication logs alone do not prove:

- Attacker identity
- Credential theft
- Malicious intent
- Data access
- Data exfiltration

Additional evidence is required.

---

🕒 Incident Timeline

Normal successful authentication
              ↓
Repeated failed admin logins
              ↓
Potential brute-force activity
              ↓
Successful admin authentication
              ↓
Successful admin access event
              ↓
Multiple-account failures from another source
              ↓
Potential password-spraying activity

---

🚨 Detection Logic

Brute-Force Detection

IF
multiple failed logins
against the same account
from the same source
within a short time period

THEN
flag as potential brute-force activity.

Password-Spraying Detection

IF
one source targets multiple accounts
AND produces repeated authentication 🔐 Security Log Investigation

📌 Project Overview

This project analyzes a synthetic authentication log to identify suspicious login behavior, detect potential brute-force and password-spraying attacks, reconstruct a likely incident timeline, and recommend appropriate incident-response actions.

The investigation demonstrates how raw authentication events can be transformed into structured security findings using Python, Pandas, Excel, and automated reporting.

«⚠️ Disclaimer: This project uses synthetic data for educational and cybersecurity-training purposes. It does not represent a real security incident.»

---

🎯 Objectives

- Normalize authentication log data.
- Analyze usernames, source IPs, actions, and authentication results.
- Detect potential brute-force attacks.
- Detect potential password-spraying activity.
- Identify successful authentication following suspicious failures.
- Reconstruct an incident timeline.
- Separate evidence from assumptions.
- Generate an investigation spreadsheet.
- Generate an incident-report PDF.
- Recommend containment and improved security controls.

---

🛠️ Technologies Used

Technology| Purpose
Python| Automated log analysis
Pandas| Data processing and analysis
OpenPyXL| Excel investigation report generation
ReportLab| PDF incident report generation
Microsoft Excel| Log review and visualization
Visual Studio Code| Development environment
GitHub| Project documentation and version control

---

📂 Project Structure

security-log-investigation/
│
├── README.md
│
├── logs/
│   └── authentication.csv
│
├── output/
│   ├── investigation.py
│   └── investigation.xlsx
│
├── reports/
│   └── Security_Log_Investigation_Complete_Report.pdf
│
├── screenshots/
│   ├── normalized-log.jpg
│   ├── project-structure.jpg
│   └── execution-output.jpg
│
└── requirements.txt

---

📊 Dataset

The investigation uses 15 synthetic authentication events containing fields such as:

timestamp
username
source_ip
action
result

Example:

username,source_ip,action,result
john,192.168.1.x,LOGIN,SUCCESS
admin,185.10.20.x,LOGIN,FAILED
admin,185.10.20.x,LOGIN,FAILED
admin,185.10.20.x,LOGIN,SUCCESS
admin,185.10.20.x,ACCESS,SUCCESS

---

🔍 Investigation Findings

1. Potential Brute-Force Activity

Multiple failed authentication attempts were recorded against the "admin" account from the same source-IP prefix:

185.10.20.x

The sequence contains repeated failures followed by a successful login.

Assessment

This pattern is consistent with potential brute-force authentication activity.

---

2. Potential Password Spraying

The source-IP prefix:

185.55.22.x

was associated with failed authentication attempts against multiple accounts:

bob
alice
john
david
sarah

Assessment

Multiple accounts being targeted from one source is consistent with a possible password-spraying attack.

---

3. Successful Authentication After Failures

The "admin" account successfully authenticated after several failed attempts.

A subsequent:

ACCESS → SUCCESS

event was also recorded.

Assessment

This requires investigation for possible account compromise.

However, the available authentication logs alone do not prove:

- Attacker identity
- Credential theft
- Malicious intent
- Data access
- Data exfiltration

Additional evidence is required.

---

🕒 Incident Timeline

Normal successful authentication
              ↓
Repeated failed admin logins
              ↓
Potential brute-force activity
              ↓
Successful admin authentication
              ↓
Successful admin access event
              ↓
Multiple-account failures from another source
              ↓
Potential password-spraying activity

---

🚨 Detection Logic

Brute-Force Detection

IF
multiple failed logins
against the same account
from the same source
within a short time period

THEN
flag as potential brute-force activity.

Password-Spraying Detection

IF
one source targets multiple accounts
AND produces repeated authentication  failures

THEN
flag as potential password-spraying activity.
Failure Followed by Success
IF
multiple failed authentication attempts
are followed by a successful login

THEN
generate a possible-compromise alert.
🧪 Practical Implementation
The investigation was automated using Python.
The execution process performs:
Loading authentication logs
        ↓
Loaded 15 events
        ↓
Normalizing timestamps
        ↓
Checking for brute-force activity
        ↓
Checking for password spraying
        ↓
Checking successful logins after failures
        ↓
Creating investigation spreadsheet
        ↓
Creating incident report PDF
The implementation generated:
investigation.xlsx
Security_Log_Investigation_Complete_Report.pdf
📸 Project Evidence
Normalized Authentication Log
The authentication dataset was normalized and reviewed using Microsoft Excel.
Python Investigation
The Python script was executed from a virtual environment and successfully processed the authentication dataset.
Generated Outputs
The investigation generated both an Excel investigation workbook and a PDF incident report.
🛡️ Recommended Response Actions
If this activity were detected in a real environment:
Validate the suspicious activity.
Investigate the affected account.
Reset the account password if compromise is suspected.
Revoke active sessions and authentication tokens.
Enable or enforce MFA.
Apply login rate limiting.
Investigate suspicious source IP addresses.
Review endpoint and network logs.
Check for unauthorized account or privilege changes.
Preserve relevant forensic evidence.
📈 Recommended Security Improvements
Organizations should implement:
Multi-Factor Authentication (MFA)
Account lockout policies
Login rate limiting
SIEM-based authentication monitoring
Password-spraying detection
Brute-force detection
Privileged-account monitoring
Centralized logging
Accurate timestamp synchronization
Session and token monitoring
Automated security alerts
🔎 Additional Evidence to Collect
Authentication logs should be correlated with:
Identity Provider / SSO logs
MFA logs
VPN logs
Firewall logs
Proxy logs
EDR telemetry
Windows/Linux security logs
Web application logs
Cloud audit logs
File-access logs
Threat-intelligence information
Correlation across these sources can help determine whether the suspicious authentication resulted in actual compromise.
📋 Evidence vs. Assumptions
Evidence
Possible Interpretation
Not Proven
Repeated admin login failures
Possible brute force
Attacker identity
Admin login succeeds afterward
Possible credential success
Credential theft
Admin ACCESS succeeds
Authenticated access occurred
Malicious access
One IP targets multiple users
Possible password spraying
Attacker intent
Failed authentication events
Suspicious activity
System compromise
Maintaining this distinction is important for a defensible cybersecurity investigation.
📊 Risk Assessment
Category
Assessment
Brute-force activity
🔴 High concern
Password spraying
🔴 High concern
Possible admin compromise
🔴 High concern
Confirmed malicious access
Not established
Data exfiltration
Not established
Attacker attribution
Not established
🎓 Learning Outcomes
Through this project, the following skills were developed:
Authentication log analysis
Security-event normalization
Brute-force detection
Password-spraying detection
Incident timeline reconstruction
Evidence-based investigation
Python automation
Spreadsheet-based forensic analysis
Incident reporting
Security monitoring and detection engineering
📄 Deliverables
The project produces the following deliverables:
Investigation Spreadsheet
investigation.xlsx
Contains normalized logs and investigation findings.
Incident Report
Security_Log_Investigation_Complete_Report.pdf
Contains the complete investigation, findings, timeline, evidence analysis, recommendations, and practical implementation screenshots.
🚀 How to Run
1. Clone the Repository
git clone https://github.com/<your-username>/security-log-investigation.git
cd security-log-investigation
2. Create a Virtual Environment
Windows
python -m venv venv
venv\Scripts\activate
Linux / macOS
python3 -m venv venv
source venv/bin/activate
3. Install Dependencies
pip install -r requirements.txt
4. Run the Investigation
python output/investigation.py
The script analyzes the authentication log and generates the investigation outputs.
📦 Requirements
Example requirements.txt:
pandas
openpyxl
reportlab
🔐 Ethical Use
This project is intended exclusively for:
Cybersecurity education
Security-log analysis practice
Digital-forensics training
Defensive security research
Incident-response learning
Do not use the techniques or scripts against systems, accounts, or networks without authorization.
👩‍💻 Project Information
Project: Security Log Investigation
Category: Cybersecurity / SOC / Digital Forensics
Investigation Type: Authentication Log Analysis
Dataset: Synthetic
Platform: GitHub
⭐ Conclusion
This project demonstrates a complete security-log investigation workflow, from raw authentication events to detection, analysis, timeline reconstruction, and incident-response recommendations.
The investigation identified patterns consistent with potential brute-force and password-spraying activity, including repeated failed administrator logins followed by successful authentication.
The findings should be treated as investigation indicators rather than definitive proof of compromise. Correlating authentication logs with identity, endpoint, network, and application evidence is essential for making a final forensic determination.
