# Cyber Control Tower (CCT)

Cyber Control Tower (CCT) is a web-based cybersecurity SOC simulation platform developed during my **DEPI internship** with the Ministry of Communications and Information Technology in Egypt.

The project simulates how a Security Operations Center can monitor, analyze, correlate, and respond to cybersecurity incidents. It takes raw security log data, normalizes it into events, correlates related activity into incidents, maps threats to **MITRE ATT&CK**, calculates risk and trust scores, and displays the results in an interactive dashboard.

---

## Project Screenshots

Add your project UI screenshots here:

```md
![Dashboard](screenshots/dashboard.png)
![Incident Triage](screenshots/incident-triage.png)
![MITRE Heatmap](screenshots/mitre-heatmap.png)
![Cyber Digital Twin](screenshots/cyber-digital-twin.png)
```

---

## Main Features

* Security log ingestion from a CSV dataset
* Event normalization into a standard format
* Incident correlation from related security events
* Incident triage with severity and status tracking
* Explainable risk scoring
* MITRE ATT&CK mapping and heatmap
* Cyber Digital Twin graph for users, assets, and network segments
* Trust Score leaderboard for user behavior risk
* MTTD and MTTR security performance metrics
* Threat hunting search over incidents
* Response playbooks with simulated SOC actions
* Analyst notes for investigation and handoff
* Audit trail for sign-ins, searches, actions, and status changes
* Role-based access for Security Analysts and SOC Managers

---

## Tech Stack

### Backend

* Python
* Flask
* pandas
* NetworkX

### Frontend

* HTML
* CSS
* JavaScript

### Data

* CSV-based cybersecurity log dataset

---

## Project Structure

```text
Cyber-Control-Tower-CCT/
├── backend/
│   ├── app.py
│   ├── api/
│   ├── auth/
│   ├── correlation/
│   ├── data/
│   ├── graph/
│   ├── ingestion/
│   ├── metrics/
│   ├── mitre/
│   ├── response/
│   ├── search/
│   ├── trust_score/
│   ├── requirements.txt
│   └── test_api.py
│
├── frontend/
│   └── index.html
│
├── notebooks/
├── run.bat
├── run.sh
├── PROJECT_TEST_REPORT.md
├── SUBMISSION_CHANGES.md
└── README.md
```

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Cyber-Control-Tower-CCT.git
cd Cyber-Control-Tower-CCT
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

### 3. Activate the Virtual Environment

For Windows:

```bash
.venv\Scripts\activate
```

For Linux/macOS:

```bash
source .venv/bin/activate
```

### 4. Install Requirements

```bash
pip install -r backend/requirements.txt
```

### 5. Run the Application

```bash
python backend/app.py
```

Then open this URL in your browser:

```text
http://127.0.0.1:5000
```

---

## Quick Start Scripts

You can also use the included run scripts.

### Windows

```bash
run.bat
```

### Linux/macOS

```bash
chmod +x run.sh
./run.sh
```

---

## Demo Accounts

| Role             | Username  | Password     |
| ---------------- | --------- | ------------ |
| Security Analyst | `analyst` | `analyst123` |
| SOC Manager      | `manager` | `manager123` |

The **Security Analyst** can view and triage incidents.

The **SOC Manager** has access to additional features such as Trust Score, MTTD/MTTR metrics, and system health.

---

## Testing

To test the backend APIs, run:

```bash
python backend/test_api.py
```

Expected result:

```text
All 90 checks passed.
```

---

## How the System Works

The project follows a simple SOC workflow:

1. **Ingestion**
   Raw cybersecurity logs are loaded from a CSV dataset.

2. **Normalization**
   The logs are converted into a cleaner and more consistent event format.

3. **Correlation**
   Related events are grouped together into incidents instead of being shown as separate alerts.

4. **MITRE Mapping**
   Incidents are mapped to MITRE ATT&CK tactics and techniques.

5. **Risk Scoring**
   Each incident receives an explainable risk score based on severity, event volume, attack-chain confidence, and MITRE tactic criticality.

6. **Investigation**
   Analysts can view incident details, search for threats, add notes, and update incident status.

7. **Response**
   The system recommends response playbooks and allows analysts to simulate SOC actions such as endpoint isolation, IP blocking, evidence collection, and password reset.

8. **Reporting and Metrics**
   The dashboard displays SOC performance metrics such as MTTD, MTTR, risk summary, Trust Score, and audit history.

---

## Important Pages

* **Command Center** – Main overview dashboard
* **Incident Triage** – View, investigate, and update incidents
* **MITRE Heatmap** – See attack tactics and techniques
* **Cyber Digital Twin** – Graph view of users, assets, segments, and incidents
* **Threat Hunting** – Search through correlated incidents
* **Trust Score** – View user behavior risk scores
* **MTTD / MTTR** – Analyze detection and response performance
* **Audit Trail** – Review user actions and system activity

---

## Project Purpose

The goal of this project is to demonstrate how different cybersecurity concepts connect together inside a SOC environment. Instead of only showing raw alerts, CCT creates a complete workflow from log analysis to incident response.

This project helped me practice:

* SOC monitoring
* Log analysis
* Incident correlation
* Threat hunting
* MITRE ATT&CK mapping
* Risk scoring
* Incident response
* Dashboard development
* Backend API development
* Role-based access control

---

## Limitations

This project is a simulation and is not designed for real production use.

Current limitations:

* Uses a local CSV dataset instead of live SIEM data
* Stores demo users and audit logs in memory
* Simulated response actions instead of real SOAR integrations
* No production database
* No real-time deployment security hardening

Future improvements could include:

* Database integration
* Live SIEM connectors such as Wazuh or Splunk
* Real SOAR automation
* Persistent user management
* More advanced threat detection rules
* Authentication hardening
* Cloud deployment

---

## Author

**Ahmad Omich**

Cybersecurity Student
DEPI Intern
Ministry of Communications and Information Technology – Egypt

---

## Disclaimer

This project was created for educational and internship demonstration purposes. It is a SOC simulation platform and should not be used as a production security monitoring system without further development, testing, and security hardening.
