# We GRC regulations 
GreenFuel Logistics – Secure Fleet Management Project
📌 Overview

This project documents the information security assessment, ISO 27001 control mapping, secure architecture design, and front-end dashboards for GreenFuel Logistics, a subsidiary of GreenWatt Energy Solutions.

The initiative combines:

Security governance (Risk Register, ISO 27001 mapping, SoA, policies).

Secure technical design (segmented architecture, minimal firewall rules).

Practical dashboards (built with HTML, CSS, and JavaScript) to visualize operations.

🎯 Objectives

Protect Fleet Management and Fuel Card systems from cyber risks.

Provide secure real-time telemetry for 200 tablets and IoT gateways.

Maintain compliance with GDPR, PCI-DSS, Egyptian Privacy Law.

Implement ISO 27001 Annex A controls (SoA).

Deliver interactive dashboards for visibility and decision-making.

🏗️ Project Scope
In-Scope Environments

Production: FMS, Fuel Card Payment, AWS IoT Core, DynamoDB, PostgreSQL.

Non-Production: UAT, staging, QA environments.

On-Premises: Windows Server 2016, PostgreSQL.

Cloud: AWS IoT Core + DynamoDB.

Endpoints: 200 in-truck tablets, 50 desktops.

SaaS: GPS APIs, billing, notifications.

🛡️ Key Deliverables
1. Risk Assessment & Heatmap

Risk Register (8+ risks, inherent vs residual).

5×5 scoring model.

Residual risk = Inherent risk – control effectiveness.

Heatmap visualization.

2. ISO 27001 Annex A Control Mapping

Statement of Applicability (SoA) with rationale.

Included: A.5 Organizational, A.6 People, A.8 Technological.

Excluded: A.7 Physical (handled by CSP).

3. Secure Architecture & Segmentation

Network zones: External, DMZ, App, Data, SOC.

WAF, reverse proxy, VPN tunnels, EDR, SOC monitoring.

Minimal inbound/outbound rules defined in a traffic rules matrix.

Policy snippets for: Access Control, Logging, Incident Response, Vendor Management.

4. Dashboards (Front-End Development)

Developed three dashboards using HTML, CSS, JavaScript:

🚛 Fleet Dashboard

Displays real-time vehicle tracking (maps integration).

Shows routes, fuel consumption, and status of each truck.

Visual indicators for delays, maintenance needs, or deviations.

⛽ Fuel Transactions Dashboard

Monitors all fuel card payments.

Shows transaction history, anomalies (e.g., duplicate or unusual amounts).

Graphs for cost savings and consumption trends.

🔐 Security Monitoring Dashboard

Shows SOC alerts, VPN status, and endpoint security health.

Includes a simplified visualization of incidents by severity.

Links to logs & compliance reports.

These dashboards demonstrate practical visualization of the project scope and can be extended into production-grade tools.

📊 Diagrams

Scope & Stakeholders Diagram – environments + roles.

Risk Heatmap – likelihood vs impact distribution.

Secure Architecture – zones, gateways, SOC integration.

📑 Statement of Applicability (Excerpt)
Annex A Clause	Control	Applicability	Justification
A.5 Organizational	Policies, IS roles, compliance, supplier security	✅ Included	Governance, regulatory adherence
A.6 People	Awareness, employment lifecycle, segregation of duties	✅ Included	High relevance due to phishing & insider risks
A.7 Physical	Physical entry, equipment security	❌ Excluded	Infrastructure cloud-hosted; CSP responsible
A.8 Technological	Logging, monitoring, secure coding, resilience	✅ Included	Critical for ransomware, DDoS, misconfigurations
🚀 How to Use This Repo
1. Documentation

Contains:

Risk Register

SoA

Policies & governance snippets

Secure architecture diagrams

2. Dashboards

fleet-dashboard/ → Vehicle tracking UI.

fuel-dashboard/ → Payment visualization.

security-dashboard/ → SOC/security monitoring UI.

Each dashboard can be run locally:

cd fleet-dashboard
open index.html

3. Templates

Policy snippets

Risk assessment templates

Control mapping matrix

📌 Next Steps

Add backend integration (API for real telemetry + payment data).

Automate compliance monitoring (e.g., AWS Config, Security Hub).

Expand dashboards into full SIEM integration.

Penetration testing & security validation.

👥 Stakeholders

Executive Mgmt: Strategy & budget.

Fleet Managers: Operations oversight.

IT Ops: Infra & uptime.

Security Team (SOC, CISO): Threat monitoring.

Drivers/Users: App & tablets.

📄 License

This repo is licensed under the MIT License for educational and professional use.

