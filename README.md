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
