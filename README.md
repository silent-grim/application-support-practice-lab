# Application Support & Service Management — Practice Lab

A structured learning and practical exercise repository focused on Application Support, IT Operations, SaaS Support, IT Service Management and Technical Troubleshooting.

## Objective

Build foundational technical knowledge and practical troubleshooting skills relevant to an Application Support & Service Management Engineer role.

This repository documents simulated exercises, investigation procedures, technical notes and troubleshooting outcomes.

**Important:** This is a personal learning and practice repository. Exercises are simulated and do not represent professional production support experience.

## Learning Roadmap

### 01. Incident Triage & Outage Investigation

**Status: Completed**

- Understand incident identification and impact assessment.
- Investigate application availability and performance issues.
- Examine simulated application logs.
- Identify symptoms and possible causes.
- Document findings and recommended investigation steps.

**Practical exercise:**
- Simulated dashboard outage investigation.
- Application log examination.
- Incident report and findings.

**Files:** `01-incident-triage/`

### 02. IT Service Management (ITSM)

**Status: Not Started**

- Incident Management
- Problem Management
- Service Request Management
- Major Incident Management
- Change Management
- SLA monitoring and escalation
- Priority vs severity
- Root Cause Analysis (RCA)

**Practical exercise:** Simulate ticket prioritisation, incident escalation, problem investigation and service request handling.

### 03. SaaS & Web Application Support

**Status: Not Started**

- SaaS application fundamentals
- Browser troubleshooting
- Web portal availability and accessibility
- Cache, cookies and browser-related issues
- User-specific vs application-wide issues
- Vendor-managed application dependencies
- Release impact assessment

**Practical exercise:** Investigate simulated web portal access and functionality problems.

### 04. Identity & Access Management (IAM)

**Status: Not Started**

- Authentication vs authorisation
- Single Sign-On (SSO)
- Multi-Factor Authentication (MFA)
- User provisioning and deprovisioning
- Access permissions and roles
- SAML, OAuth 2.0 and OpenID Connect (OIDC)
- Access reviews and recertification

**Practical exercise:** Investigate simulated login failures, access-denied errors and permission issues.

### 05. HTTP, REST APIs & Integration Troubleshooting

**Status: Not Started**

- HTTP and HTTPS
- HTTP methods and status codes
- REST API fundamentals
- API requests and responses
- JSON fundamentals
- API authentication
- API testing
- Integration failures and troubleshooting

**Practical exercise:** Investigate simulated API errors and failed application integrations.

### 06. Networking & Connectivity

**Status: Theory Completed — Practical Lab Pending**

**Topics covered:**

- TCP/IP fundamentals and networking layers
- OSI model and network encapsulation
- IP addressing and private IP ranges
- DNS resolution and troubleshooting
- Default gateway and routing fundamentals
- TCP vs UDP
- Common network ports and protocols
- TCP three-way handshake
- TCP connectivity testing
- TLS handshake and certificate validation
- HTTP/HTTPS communication lifecycle
- HTTP methods and status codes
- Gateway and upstream connectivity troubleshooting

**Practical exercise:**

Perform Windows-based IP configuration, DNS resolution, routing and TCP connectivity checks. Investigate simulated network and application connectivity failures.

**Files:** `06-networking/`

### 07. Application Logs, Monitoring & Alert Management

**Status: Not Started**

- Application log fundamentals
- Log levels: INFO, DEBUG, WARNING and ERROR
- Log investigation and filtering
- Application health monitoring
- Monitoring dashboards
- Alert identification and prioritisation
- Application Performance Monitoring (APM)
- Response time and availability

**Practical exercise:** Investigate simulated application errors, performance degradation and production alerts.

### 08. Database & Scheduled Job Troubleshooting

**Status: Not Started**

- SQL fundamentals
- Database connectivity
- Query troubleshooting
- Database availability
- Application-to-database dependencies
- Batch processing
- Scheduled jobs and task failures
- Job execution logs

**Practical exercise:** Investigate simulated database connection failures and failed scheduled jobs.

### 09. Vendor & Third-Party Management

**Status: Not Started**

- Raising technically complete vendor tickets
- Incident evidence and documentation
- Vendor escalation procedures
- Evaluating vendor responses
- Tracking incidents through resolution
- Vendor release notes and impact assessment
- Fix validation and post-resolution checks
- Maintaining a knowledge base

**Practical exercise:** Prepare a simulated vendor escalation ticket, assess a sample release update and document fix validation.

### 10. Patch Management

**Status: Not Started — Dedicated Module**

- Patch management fundamentals
- Security patches vs software updates
- Vulnerability identification and prioritisation
- Patch assessment and compatibility checks
- Change approval and maintenance windows
- Backup and rollback planning
- Testing patches before deployment
- Patch deployment and verification
- Patch compliance and documentation
- Handling failed or unsuccessful patches

**Practical exercise:** Create a simulated patch management plan, assess a proposed update, document deployment checks and prepare a rollback procedure.

### 11. SSL/TLS & Certificate Lifecycle

**Status: Not Started**

- SSL and TLS fundamentals
- Digital certificates
- Certificate expiration
- Certificate validation
- Certificate renewal
- Trust chains and certificate authorities
- HTTPS troubleshooting

**Practical exercise:** Investigate simulated certificate expiry and HTTPS connection errors.

### 12. Windows & Linux Operations

**Status: Not Started**

- Windows services and processes
- Event Viewer and system logs
- Basic Linux commands
- Process and service management
- File permissions
- Disk and resource utilisation
- Basic server troubleshooting

**Practical exercise:** Investigate simulated service failures and resource-related problems.

### 13. Configuration, CMDB & Knowledge Management

**Status: Not Started**

- Configuration Management
- Configuration Management Database (CMDB)
- Configuration Items (CIs)
- Application and infrastructure dependencies
- Operational documentation
- Runbooks and standard operating procedures
- Knowledge base creation and maintenance

**Practical exercise:** Create a sample application configuration record, dependency map and troubleshooting runbook.

### 14. Security, Risk & Application Lifecycle

**Status: Not Started**

- Application security fundamentals
- Vulnerability management
- Access management controls
- Application onboarding and offboarding
- Disaster Recovery (DR) fundamentals
- Backup and recovery concepts
- Audit evidence and compliance documentation
- Security assessments and questionnaires
- Application upgrades and lifecycle controls

**Practical exercise:** Prepare a simulated application security and operational risk assessment.

### 15. Operational Tools & CI/CD Fundamentals

**Status: Not Started**

- ITSM and ticketing systems
- Application Performance Monitoring tools
- Log search tools
- API testing tools
- SQL clients
- CI/CD fundamentals
- Deployment and release processes
- Monitoring dashboards

**Practical exercise:** Document the purpose and basic workflows of common application support tools.

## Troubleshooting Methodology

Use the following approach when investigating an application issue:

**Size → Spot → Search → Shift → Solve → Secure**

- **Size:** Assess the impact and scope.
- **Spot:** Identify the symptoms.
- **Search:** Collect evidence and investigate.
- **Shift:** Check recent changes and releases.
- **Solve:** Coordinate resolution or escalate.
- **Secure:** Verify recovery and document the outcome.

## Repository Structure

```
application-support-practice-lab/
│
├── README.md
│
├── 01-incident-triage/
│   └── incident-report.md
│
├── 02-itsm/
├── 03-saas-web-support/
├── 04-identity-access-management/
├── 05-http-rest-api/
├── 06-networking/
│   └── README.md
├── 07-logs-monitoring/
├── 08-database-scheduled-jobs/
├── 09-vendor-management/
├── 10-patch-management/
├── 11-ssl-tls-certificates/
├── 12-windows-linux/
├── 13-cmdb-knowledge-management/
├── 14-security-risk-lifecycle/
└── 15-tools-cicd/
```

## Exercise Documentation Standard

Each completed exercise should include:

- **Scenario:** What happened?
- **Impact:** Who or what was affected?
- **Symptoms:** What was observed?
- **Investigation:** What checks were performed?
- **Evidence:** Logs, commands, outputs or observations.
- **Findings:** What was established?
- **Resolution:** What corrective action was taken or recommended?
- **Verification:** How was recovery confirmed?
- **Lessons learned:** What could prevent recurrence?

## Progress Tracking

The roadmap is updated as exercises are completed.

| Area  | Status |
|---|---|
| Incident Triage & Outage Investigation | Completed |
| IT Service Management | Not Started |
| SaaS & Web Application Support | Not Started |
| Identity & Access Management | Not Started |
| HTTP, REST APIs & Integrations | Not Started |
| Networking & Connectivity | Theory Completed — Practical Lab Pending |
| Logs, Monitoring & Alerts | Not Started |
| Database & Scheduled Jobs | Not Started |
| Vendor Management | Not Started |
| Patch Management | Not Started |
| SSL/TLS & Certificates | Not Started |
| Windows & Linux Operations | Not Started |
| CMDB & Knowledge Management | Not Started |
| Security, Risk & Application Lifecycle | Not Started |
| Operational Tools & CI/CD | Not Started |

## Learning Approach

This repository follows a practical, scenario-based learning approach. Each topic is studied through technical fundamentals, simulated incidents, troubleshooting exercises and documented findings.

Modules are marked complete only after their relevant learning objectives and practical exercises have been validated.
