# Event-Driven-Cloud-Security-Compliance-Automation-AWS-


## 📌 Project Overview

This project demonstrates the design and implementation of an event-driven security automation framework in AWS. The solution detects security events in real time, triggers automated remediation, and enforces compliance aligned with NIST 800-53 and RMF.

## 🧱 Architecture Diagram
                +----------------------+
                |    AWS CloudTrail    |
                +----------+-----------+
                           |
                +----------v-----------+
                |     GuardDuty        |
                +----------+-----------+
                           |
                +----------v-----------+
                |     AWS Config       |
                +----------+-----------+
                           |
                +----------v-----------+
                |    EventBridge       |
                +----------+-----------+
                           |
        +------------------+------------------+
        |                                     |
  +-------v--------+             +--------v--------+
  |   Lambda       |             |   SNS Alerts    |
  | Auto-Remediate |             | (Email/Slack)   |
  +-------+--------+             +--------+--------+
          |
          |
  +-------v--------+
  |   S3 Bucket    |
  | (Logs/Evidence)|
  +----------------+

                  +----------------------+
                  |   Security Hub       |
                  | (Compliance View)    |
                  +----------------------+

## 🎯 Objectives
- Detect security threats and misconfigurations in real time
- Automate remediation using serverless functions
- Enforce compliance with NIST 800-53 controls
- Provide centralized visibility using Security Hub
- Generate audit-ready logs and evidence

## 🧩 Core Components
### Detection Layer
- AWS CloudTrail (API logging)
- Amazon GuardDuty (threat detection)
- AWS Config (configuration compliance)
### Event Layer
- Amazon EventBridge (event routing)
### Response Layer
- AWS Lambda (automated remediation)
### Notification Layer
- Amazon SNS (alerts and notifications)
- Governance & Compliance
- AWS Security Hub
- S3 (log storage and audit evidence)

## ⚙️ Use Cases
1. IAM Compromise Response
Detect suspicious login activity
Automatically disable compromised credentials
Send alert and log incident
2. Public S3 Bucket Remediation
Detect public access via AWS Config
Remove public permissions automatically
3. Root Account Usage Alert
Trigger immediate alert when root account is used
4. Compliance Drift Detection
Identify when logging or encryption is disabled
Flag and optionally remediate

## 🔐 NIST 800-53 Control Mapping
AWS Service	Control
IAM	AC-2 (Account Management)
CloudTrail	AU-2 (Audit Events)
Config	CM-6 (Configuration Settings)
GuardDuty	SI-4 (System Monitoring)
## 🚀 Deployment Plan
- Phase 1: Environment Setup
    - Configure IAM roles and policies
    - Enable CloudTrail, GuardDuty, Config
- Phase 2: Event Routing
    - Create EventBridge rules for security events
- Phase 3: Automation
    - Develop Lambda functions for remediation
- Phase 4: Notifications
    - Configure SNS alerts
- Phase 5: Compliance & Monitoring
    - Enable Security Hub
    - Aggregate findings

## 📊 Expected Outcomes
- Reduced response time to security incidents
- Improved compliance visibility
- Automated enforcement of security policies
- Hands-on experience with cloud security operations

## 📁 Repository Structure

/event-driven-security-automation
│── /lambda
│   ├── disable_iam_user.py
│   ├── remediate_s3_public.py
│
│── /terraform
│   ├── main.tf
│   ├── variables.tf
│
│── /docs
│   ├── architecture.png
│   ├── security_assessment.md
│   ├── poam.md
│
│── README.md


## 🧠 Skills Demonstrated
Cloud Security Engineering
Incident Response Automation
Compliance Assessment (NIST RMF)
Infrastructure as Code (Terraform)
Monitoring & Logging

## 📌 Future Enhancements
Integrate Slack/PagerDuty for alerting
Add SOAR-style workflows
Expand to multi-account AWS environments
Implement Zero Trust networking controls

## ✍️ Author

Kenneth Joiner

## ⭐ Notes

This project is designed to align with federal cybersecurity roles (GS-12/GS-13) by demonstrating real-world security operations, compliance validation, and automated remediation capabilities.
