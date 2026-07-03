# Microsoft Defender XDR - Complete Guide

## Table of Contents
1. [Understanding Concepts](#understanding-concepts)
2. [Advantages](#advantages)
3. [Disadvantages](#disadvantages)
4. [Pre-requisites](#pre-requisites)
5. [Use Cases](#use-cases)
6. [Plan to Deploy](#plan-to-deploy)
7. [Implementation](#implementation)
8. [Threat Detection](#threat-detection)
9. [Threat Investigation](#threat-investigation)
10. [Threat Response](#threat-response)
11. [Threat Mitigation](#threat-mitigation)
12. [Analytics & Visualization](#analytics--visualization)
13. [Threat Hunting](#threat-hunting)
14. [Troubleshooting](#troubleshooting)
15. [Additional Components](#additional-components)
16. [Scenario-based QnA](#scenario-based-qa)

---

## Understanding Concepts

### What is Extended Detection and Response (XDR)?

XDR system is designed to deliver an intelligent, automated, and integrated security across an organization's different domains. It helps to prevent, detect, and respond to threats across identities, endpoints, applications, email, IoT, infrastructure, and cloud platforms.

### Microsoft Defender XDR

Microsoft Defender is an integrated threat protection suite with solutions that detect malicious activity across email, endpoints, applications, and identity. It provides a complete attack chain compromise story that enables a complete understanding of the threat.

Microsoft Defender XDR provides a comprehensive solution for managing and responding to security threats. Here's a breakdown of its key features:

- **Dashboard:** Offers a centralized view of your security posture, including key metrics, alerts, and Secure Score.
- **Incident Management:** Streamlines the process of managing and responding to security alerts and incidents.
- **Threat Hunting:** Enables proactive searching for threats and vulnerabilities.
- **Automated Response:** Allows for automated responses to threats, such as quarantining devices.
- **Threat Analytics:** Provides insights into threat trends and patterns.
- **Asset Management:** Offers a detailed view of devices, including their security status, vulnerabilities, and compliance.
- **Email & Collaboration Security:** Allows for configuration of security policies for email and collaboration tools like Microsoft 365.
- **Reporting:** Provides access to various security reports for analysis and compliance.
- **Incident Classification:** Defender allows for incident severity to be set and tagging for custom organization.
- **Incident Investigation:** Defender provides tools and features for incident investigation, including alert linking and status management.
- **Quarantine Removal:** Defender allows for the removal of files from quarantine.
- **Automated Investigation:** Defender includes automated investigation capabilities.
- **Features:** Defender integrates threat protection across various domains (endpoints, email, identities, cloud apps).
- **Incident Response:** Defender enables incident response actions across the integrated domains.

Essentially, Microsoft Defender XDR combines elements of SIEM and XDR to offer a holistic approach to security. It's designed to simplify security management, improve threat detection, and accelerate response times.

### SIEM vs XDR Comparison

Both SIEM and XDR are important security solutions for organizations, but they have different strengths and weaknesses.

SIEM solutions are better at collecting and analysing large volumes of data, while XDR solutions are better at detecting and responding to threats across multiple security silos.

| Aspect | SIEM | XDR |
|--------|------|-----|
| **Strengths** | Collects and analyses large volumes of data from a variety of sources. Provides a central view of security posture. Can be used to generate reports for compliance purposes. | Detects and responds to threats across multiple security silos. Uses advanced analytics to detect threats that may not be visible to traditional SIEM systems. Can automate many of the tasks involved in threat detection and response. |
| **Weaknesses** | Can be complex and expensive to implement and maintain. Can generate many false positives. May not be able to detect and respond to threats that span multiple security silos. | May not be as good at collecting and analysing large volumes of data as SIEM systems. Can be expensive to implement and maintain. May not be as mature as SIEM systems. |
| **Focus** | Focuses on collecting and analysing large volumes of security data for compliance and threat detection. It's great for organizations needing strong auditing and log management capabilities. | Prioritizes threat detection and response across multiple security layers (email, endpoints, cloud, etc.). It excels at correlating data from different sources to identify and respond to sophisticated attacks. |

---

## Advantages

Microsoft Defender XDR offers numerous benefits for organizations:

- **Integrated threat protection:** Microsoft Defender XDR integrates all of your threat protection tools into a single platform, providing a unified view of your security posture and making it easier to identify and respond to threats.

- **AI-powered insights:** Microsoft Defender XDR uses AI to identify threats and anomalies that may be missed by traditional security solutions. This helps you to focus your security resources on the most important threats.

- **Automated security workflows:** Microsoft Defender XDR can automate common security workflows, such as incident response and threat hunting. This frees up your security team to focus on more strategic tasks.

- **Scalability and performance:** Microsoft Defender XDR is a cloud-native platform that can scale to meet the needs of even the largest organizations. It also offers high performance and reliability.

- **Unified Incident View:** Correlates alerts from different security products (e.g., Defender for Office 365, Defender for Endpoint, Defender for Cloud Apps) into a single incident, providing a holistic view of the threat. This simplifies threat analysis and response.

- **Integrated Threat Detection and Response (XDR):** Combines signals from identity, endpoints, email, and applications for comprehensive threat detection and mitigation.

- **Automated Remediation and Containment:** Provides automated threat remediation and containment capabilities, including:
  - Automated or analyst-approved remediation of detected threats.
  - Sharing threat intelligence across Microsoft security tools.
  - Integration with Intune and Conditional Access in Microsoft Entra ID to restrict access to corporate resources from infected devices.
  - Automated restoration of access upon threat remediation.

- **Improved Security Posture:** Helps mitigate risk by preventing attackers from accessing corporate resources while minimizing disruption to user productivity.

- **Reduced workload for security teams:** Automated investigation can help security teams to save time by automating many of the tasks involved in investigating security alerts and incidents.

- **Improved response times:** Automated investigation can help security teams to respond to incidents more quickly by automating the initial stages of the investigation process.

- **Increased accuracy:** Automated investigation can help to improve the accuracy of incident investigations by using machine learning and analytics to identify patterns and trends.

- **Reduced costs:** Automated investigation can help to reduce the costs associated with incident response by reducing the workload for security teams and improving response times.

---

## Disadvantages

While Microsoft Defender XDR offers many benefits, there are some potential limitations and challenges:

- **Complexity:** Can be challenging to configure and manage effectively, especially for organizations with limited security expertise.

- **Integration Challenges:** While integration with the Microsoft ecosystem is strong, integrating with third-party tools can sometimes be complex.

- **Cost:** Can be expensive, especially for larger organizations. See the pricing section for details.

- **Dependence on Microsoft Ecosystem:** Best performance is achieved when used within the broader Microsoft security ecosystem.

- **Data Overload:** XDR platforms generate a large amount of data. Effectively analyzing and prioritizing this data can be challenging.

- **Talent Shortage:** Skilled security analysts are needed to effectively operate and manage XDR platforms.

- **Customization and Tuning:** Tuning the XDR platform to the specific environment and threat landscape can be complex.

- **Organizational Silos:** Breaking down organizational silos between different security teams is often necessary for effective XDR implementation.

---

## Pre-requisites

### Requirements

To implement Microsoft Defender XDR, you need:

1. **A qualifying Microsoft 365 subscription:** This includes Microsoft 365 E5, E5 Security, Business Premium, or Defender XDR for Business.
2. **Supported operating systems and platforms:** Windows 10/11, Windows Server 2012+, macOS, Linux, Android, and iOS.
3. **Supported devices:** Computers, laptops, mobile devices, and servers.
4. **The latest Defender XDR agent:** Installed on all supported devices to collect and transmit data.
5. **Network connectivity:** A connection to the Microsoft 365 cloud for data transfer, updates, and security intelligence.

---

---

---

## Implementation

### Threat Prevention

Microsoft Defender is a unified platform that provides integrated threat protection across endpoints, identities, email, and applications. It uses machine learning and artificial intelligence (AI) to identify and respond to sophisticated attacks.

Microsoft Defender XDR includes the following products and solutions:
- **Microsoft Defender for Endpoint:** Protects devices from malware, viruses, and other threats.
- **Microsoft Defender for Office 365:** Protects email and collaboration tools from phishing attacks, spam, and other threats.
- **Microsoft Defender for Identity:** Protects identities from unauthorized access and malicious activity.
- **Microsoft Defender for Cloud Apps:** Protects cloud applications from data breaches and other threats.

Microsoft Defender XDR can be used to protect a wide range of environments:
- **Cloud environments:** Microsoft Azure, Amazon Web Services (AWS), and Google Cloud Platform (GCP)
- **On-premises environments:** Windows and Linux servers, as well as network devices
- **Hybrid environments:** Combining cloud and on-premises resources

#### How to Configure XDR Policies and Alerts

**Define Your Scope:**
- **Prioritize Assets:** Identify your most critical assets (servers, databases, user accounts) to prioritize protection.
- **Threat Modelling:** Analyze potential threats and attack vectors relevant to your organization.

**Configure Alert Rules:**
- **Granular Conditions:** Define specific conditions for triggering alerts (file activity in sensitive directories, suspicious login attempts, network connections to known malicious IPs)
- **Severity Levels:** Assign severity levels (low, medium, high, critical) to each alert based on potential impact.

**Establish Alerting Workflow:**
- **Notification Channels:** Set up notifications via email, SMS, SIEM, or SOAR platforms.
- **Recipient Groups:** Create groups (security team, IT administrators) to receive alerts based on severity and type.
- **Escalation Procedures:** Define how alerts are escalated for investigation and response.

**Policy Optimization:**
- **Alert Grouping:** Create policies to group related alerts for easier management.
- **Suppression Rules:** Configure rules to suppress false positives or known benign events.
- **Tuning:** Regularly review and adjust alert thresholds and rules to reduce noise.

**Testing and Monitoring:**
- **Simulate Attacks:** Conduct regular tests to validate alert rules and response procedures.
- **Continuous Monitoring:** Monitor alert activity, investigate trends, and fine-tune your XDR configuration.

### Vulnerability Management

- Discovers vulnerable and misconfigured devices based on known attack vectors and software vulnerabilities.
- **Exposure Score:** Current exposure associated with machines in organization (Less is good)
- **Secure Score:** Shows collective security configuration posture of machines (High is good)
  - OS
  - Application
  - Network
  - Account
  - Security Controls
- **Exposure Distribution:** Exposed machines are easy targets for attacks (High, Medium, Low)
- **Top Security Recommendations:** Based on highest organizational exposure impact

#### How to Download Vulnerability Scan Report
1. Go to the Microsoft Defender XDR portal.
2. Click Endpoints > Vulnerabilities.
3. In the Vulnerabilities table, click the Export button.
4. In the Export Vulnerabilities dialog box, select the CSV or JSON format for the report.
5. Click the Export button to download the report.

### Attack Surface Reduction (ASR)

Attack surface reduction (ASR) rules in Microsoft Defender focus on mitigating vulnerabilities by restricting software behaviors that could be exploited by attackers.

#### Components of Attack Surface Reduction

- **Attack surface reduction rules:** Reduce attack surface in apps with intelligent rules (Need Microsoft Defender Antivirus)
- **Hardware-based isolation:** Protects integrity of system during start and running, validates system integrity with local and remote attestation, and uses container isolation for Microsoft Edge
- **Application control:** Use application control so that your applications must earn trust in order to run.
- **Exploit protection:** Help protect operating systems and apps your organization uses from being exploited. Works with third-party antivirus solutions.
- **Network protection:** Extend protection to your network traffic and connectivity on your organization's devices (Requires Microsoft Defender Antivirus)
- **Web protection:** Secure your devices against web threats and help you regulate unwanted content.
- **Controlled folder access:** Help prevent malicious or suspicious apps (including file-encrypting ransomware malware) from making changes to files in your key system folders (Requires Microsoft Defender Antivirus)
- **Device control:** Protects against data loss by monitoring and controlling media used on devices, such as removable storage and USB drives.

#### ASR Rules List
- Block abuse of exploited vulnerable signed drivers
- Block Adobe Reader from creating child processes
- Block all Office applications from creating child processes
- Block credential stealing from the Windows local security authority subsystem (lsass.exe)
- Block executable content from email client and webmail
- Block executable files from running unless they meet a prevalence, age, or trusted list criterion
- Block execution of potentially obfuscated scripts
- Block JavaScript or VBScript from launching downloaded executable content
- Block Office applications from creating executable content
- Block Office applications from injecting code into other processes
- Block Office communication application from creating child processes
- Block persistence through WMI event subscription
- Block process creations originating from PSExec and WMI commands
- Block rebooting machine in Safe Mode (preview)
- Block untrusted and unsigned processes that run from USB
- Block use of copied or impersonated system tools (preview)
- Block Webshell creation for Servers
- Block Win32 API calls from Office macros
- Use advanced protection against ransomware

### Endpoint Security

Endpoint protection should be installed on your machines. Endpoint protection health issues should be resolved on your machines.

#### Check Status of Microsoft Defender Antivirus
```powershell
Get-MpComputerStatus
```

#### List of Antivirus Health Issues
Any of the following properties being false indicates an issue:
- AMServiceEnabled
- AntispywareEnabled
- RealTimeProtectionEnabled
- BehaviorMonitorEnabled
- IoavProtectionEnabled
- OnAccessProtectionEnabled

#### PowerShell Commands for Defender Management
- Update settings: `Add-MpPreference`
- Get history of detected threat: `Get-MpThreat`
- Get known threats from definition catalog: `Get-MpThreat`
- Remove active threats from machine: `Remove-MpThreat`
- Configure scan and updates: `Set-MpPreference`
- Start Antimalware scan: `Start-MpScan`
- Start offline Antimalware scan: `Start-MpWDOScan`
- Update Signature: `Update-MpSignature`

#### Windows Defender Exploit Guard
Windows Defender Exploit Guard should be enabled on your machines. Components include:
- Attack surface reduction
- Controlled folder access
- Exploit protection
- Network protection

### Network Security

#### Adaptive Network Hardening
Adaptive Network Hardening provides a more granular recommendation based on the traffic it has analysed. This is an add-on feature to NSG. MDC needs to collect data for at least 30 days to provide recommendations for adaptive network hardening.

#### Network Security Recommendations
- All Internet traffic should be routed via your deployed Azure Firewall
- All network ports should be restricted on network security groups associated to your VMs
- API Management services should use a VNET
- App Configuration should use private link
- Authorized IP ranges should be defined on Kubernetes Services
- Azure Cache for Redis should reside within a VNET
- Azure Cosmos DB accounts should have firewall rules
- Azure DDoS Protection Standard should be enabled
- Azure Defender for DNS should be enabled
- Azure Key Vault should disable public network access
- Private endpoint should be configured for Key Vault
- Storage account public access should be disallowed
- Storage accounts should restrict network access
- Web Application Firewall (WAF) should be enabled for Application Gateway

---

## Threat Detection

### How Microsoft Defender Detects Threats

- **Data Collection & Correlation:** XDR solutions gather data from various sources (endpoints, networks, cloud) and correlate it to identify threat patterns and relationships.
- **Statistical Anomaly Detection:** XDR uses statistical analysis to identify deviations from normal behavior.
- **Threat Intelligence Integration:** XDR incorporates threat intelligence feeds to identify known threats and their indicators of compromise (IOCs).
- **Machine Learning for Threat Identification:** XDR employs machine learning models to accurately detect new, unseen threats.
- **Automated Investigation & Response:** Machine learning in XDR can automate threat investigation, helping determine root cause and suggesting remediation actions.
- **Enhanced Visibility:** By collecting data from diverse sources, XDR provides a comprehensive view of the security landscape.
- **Reduced False Positives:** Analytics and machine learning help minimize false positives.
- **Accelerated Detection & Response:** Automation through XDR enables faster threat detection and response.

### Indicators of Attack (IoA)

Patterns of behavior that confirm a cyber-attack has happened:
- Unusual network activity (sudden increase in traffic, spikes in bandwidth, traffic to known malicious IPs)
- Unexpected login attempts (failed logins from unusual locations, logins from compromised accounts)
- Changes to system or security configurations (disabling security software, changing permissions, installing new software)
- Data exfiltration (attempts to transfer large amounts of data out of the network)
- Ransomware demands (appearance of ransom notes, encryption of critical files)
- Performance issues (slow system performance, unexpected reboots, unavailability of applications)
- User complaints (unusual activity, problems logging in, missing files)

### Adding Indicators of Compromise (IoCs)

You can add up to 15000 indicators (Files Hashes, IP addresses, URLs/Domains, Certificates). Navigate to Settings > Endpoints > Rules > Indicators.

#### How to Add File Hash
- **Indicator:** Add File Hash, Title, Description, Expiry date
- **Actions:** Allow, Audit, Warn, Block execution, Block and Remediate
- **Alert details:** Generate alerts with severity (Informational, Low, Medium, High) and category per MITRE ATT&CK Framework
- **Organizational scope:** All devices in organization

### Alerts Classification

- **High:** High probability that resource is compromised
- **Medium:** Probable suspicious activity that might indicate that a resource is compromised
- **Low:** This might be a benign positive or a blocked attack
- **Informational:** Useful to understand the context of attack

### Threat Reports

Microsoft Defender for Cloud has three types of threat reports:
- **Activity Group Report:** Provides deep dives into attackers, their objectives, and tactics.
- **Campaign Report:** Focuses on details of specific attack campaigns.
- **Threat Summary Report:** Covers all the items in the previous two reports.

Download threat report: MDC > Alerts > Select alert > View full details > Alert details > Threat intelligence report

---

## Threat Investigation

### Investigation through XDR

XDR enhances threat investigation and response by collecting and correlating data from multiple sources like endpoints, networks, and cloud environments.

#### How XDR Helps Security Teams
- **Investigate effectively:** Identify root cause by connecting dots between different security layers, uncover suspicious activity using analytics and machine learning, automate evidence collection.
- **Respond efficiently:** Automate responses like quarantining infected devices, blocking malicious traffic, integrate with existing security tools.

#### Steps for Using XDR to Investigate
1. **Define the scope:** Identify affected systems, users, and data.
2. **Pinpoint the root cause:** Leverage XDR's analytics and machine learning.
3. **Contain and remediate:** Isolate infected systems, block malicious traffic.
4. **Hunt for similar incidents:** Use XDR to proactively search for related threats.
5. **Document everything:** Record incident details for future learning.

### Investigation through MDE (Microsoft Defender for Endpoint)

#### Actions and Submissions
**Actions Tracked:**
- Collect investigation package
- Isolate device (can be undone)
- Offboard machine
- Release code execution
- Release from quarantine
- Request sample
- Restrict code execution (can be undone)
- Run antivirus scan
- Stop and quarantine
- Contain devices from the network

**Pending Actions:** Displays actions requiring attention. Users can approve or reject actions individually or in bulk.

**Action History:** Serves as an audit log, recording all actions taken and providing a way to undo them.

#### How to Perform Device Investigation
1. Identify the device to investigate by reviewing alerts or incidents.
2. View the device details (device name, operating system, hardware configuration, security status).
3. Investigate the device's activity (event logs, network traffic, file system activity).
4. Collect evidence (system logs, network traffic logs, malware samples).
5. Remediate the threat (remove malware, patch vulnerabilities, harden security configuration).

### Investigation through Sentinel

#### Notebooks
Notebooks in Sentinel are used for Advanced Hunting. They provide a virtual sandbox with machine learning, visualizations, and data analysis capabilities.

Two libraries are used:
- **KQLmagic:** Provides easy to implement API wrapper to run KQL queries
- **MSTIcpy:** Microsoft Threat Intelligence Python Security tools for investigation and hunting

#### Bookmarks
- During hunting and investigation, bookmark items to refer to them in the future.
- Hunting bookmarks enable Sentinel users to save, tag, annotate, share and investigate results from a Log Analytics query.

#### Data Connectors QnA
- Use KQL queries to generate alerts and group them into incidents
- Implement solution to view/stream creation of user account on Windows cloud server: Windows security events connector
- Collect events from non-Azure Windows machine: Install Azure Arc and enable Legacy Agent
- Ingest Azure AD Identity Protection data: Requires Workspace read/write permissions, Global Administrator or security administrator, Azure AD premium P2
- Connect Azure AD to Sentinel: Navigate to Azure Portal > Sentinel > Configuration > Data Connectors > Azure Active Directory

### Investigation through MDC (Microsoft Defender for Cloud)

#### Key Concepts
- **Real-time Security Events:** MDC alerts notify you of potential risks in your Azure environment.
- **Severity Levels:** High, Medium, Low, Informational
- **Indicators of Compromise (IoCs):** Affected resource IDs, attacker IP addresses, user UPNs
- **Email Notifications:** Configure email alerts for notifications
- **Alert Suppression:** Reduces noise from false positives (rules expire after six months)
- **Automated Response:** Triggers Logic Apps for incident response workflows
- **Threat Intelligence Reports:** Comprehensive view of attack campaigns

#### Responding to Specific MDC Alerts

##### Key Vault Alerts
- **Investigation:** Determine if traffic source is internal or external
- **Mitigation:**
  - Contact user or application owner if behavior is expected
  - If source is unknown, enable Key Vault firewall and configure trusted resources/VNETs
  - If unauthorized, adjust Key Vault access policies
  - If source is an Azure AD role, contact administrator to review permissions
- **Impact Assessment:** Review accessed secrets and timestamps
- **Action:** Rotate accessed secrets, keys, and certificates. Disable or delete affected secrets.

##### DNS Alerts
- **Investigation:** Contact resource owner to determine if behavior is expected
- **Mitigation:**
  - Isolate resource from network
  - Perform full antimalware scan
  - Review installed and running software
  - Revert to healthy state (reimage if necessary)
  - Address MDC recommendations

##### Resource Manager Alerts
- **Investigation:** Contact resource owner to determine if behavior is expected
- **Mitigation:**
  - **Compromised User Accounts:** Delete unfamiliar accounts, change credentials, review Azure Activity Logs
  - **Compromised Subscriptions:** Remove unfamiliar Runbooks, review IAM permissions, delete unfamiliar resources, review security alerts
  - **Compromised VMs:** Change user passwords, perform full antimalware scan, reimage from trusted source

### Investigation through MDCA (Microsoft Defender for Cloud Apps)

#### Identify Scope and Impact
- First step in IR is to identify scope and impact of incident
- Identify which cloud services, users, devices, and data is affected
- Determine how severe the damage is
- CASB can help by providing visibility and alerts on cloud activity and anomalies

#### Contain and Isolate Incident
- CASB can enable you to apply granular policies and controls on cloud services
- Use CASB automated response capabilities to contain threats quickly

#### Eradicate and Restore
- CASB can help with backup and recovery options
- Use CASB to audit and verify recovery processes

#### Learn and Improve
- CASB can provide reports and dashboards showing incident timeline, impact, and response
- Use CASB to implement and monitor action items to improve security posture

---

## Threat Response

### Microsoft Defender XDR Threat Response

Microsoft Defender XDR's Threat Response feature provides a centralized location to manage remediation actions across devices, email & collaboration content, and identities.

#### Actions Tracked
- Collect investigation package
- Isolate device (can be undone)
- Offboard machine
- Release code execution
- Release from quarantine
- Request sample
- Restrict code execution (can be undone)
- Run antivirus scan
- Stop and quarantine
- Contain devices from the network
- Initiate automated investigation
- Block URL (time-of-click)
- Soft delete email messages or clusters
- Quarantine email
- Quarantine email attachment
- Turn off external mail forwarding
- Disable user
- Reset user password
- Confirm user as compromised

#### Required Roles
- Security Administrator
- Active remediation actions
- Search and Purge

#### Taking Remediation Actions
1. Navigate to the "Devices" page in the Defender XDR portal.
2. Select the target device.
3. Go to the "Remediation" tab.
4. Choose the desired action.
5. Click "Act."

### SOAR in Defender

#### What is SOAR?
SOAR stands for Security Orchestration and Automated Response. SOAR system takes alerts from many sources, such as a SIEM system, then triggers action-driven automated workflows and processes to run security tasks that mitigate the issue.

#### SOAR Components
- Security Orchestration
- Security Automation
- Security Response

### SOAR in MDC

#### Workflow Automation
- Create Logic Apps to automate responses to MDC alerts and recommendations
- Configure triggers based on Defender for Cloud data type, alert/recommendation name, severity, or state
- Define actions to be taken by the Logic App

#### Alert Suppression
- Create rules to automatically dismiss specific alerts based on criteria
- Useful for frequent alerts, false positives, or known non-critical issues

### Automated Response through Sentinel

#### Automation Playbooks
- Copy existing playbook: clone
- Changes to playbook: edit
- Run playbook manually on alert in incident: Incident page > Select incident > View full details > Alerts > View playbooks

#### Automation Rules
Solution that runs playbooks as a response of incidents.

#### How to Run Playbook Manually
1. Incident page > Select incident > View full details
2. In alerts tab > Click on alert on which you want to run playbook
3. Click view playbooks and select playbook to run from list

### Automate Remediations through Playbooks

Resources:
- Automate Azure Security Center actions with Playbooks and ServiceNow: https://techcommunity.microsoft.com/t5/microsoft-defender-for-cloud/automate-azure-security-center-actions-with-playbooks-and/ba-p/264843
- Remediation scripts: https://github.com/Azure/Microsoft-Defender-for-Cloud/tree/main/Remediation%20scripts

---

## Threat Mitigation

### Mitigating Cyberattacks with Microsoft Defender XDR

Microsoft Defender XDR empowers you to effectively respond to cyberattacks:

1. **Identify Affected Systems and Users:** Use detection capabilities and threat intelligence to pinpoint compromised systems and user accounts.
2. **Determine the Scope of the Infection:** Investigate the extent of the attack, analyze network traffic, examine files accessed or modified.
3. **Identify the Root Cause:** Uncover how the attack originated, trace the initial infection vector, identify exploited vulnerabilities.
4. **Remediate the Infection:** Take action to contain and eradicate the threat (isolate systems, remove malware, restore data, patch vulnerabilities).
5. **Prevent Future Infections:** Strengthen defenses (email filtering, web filtering, strong authentication, application control, security awareness training).

### Key Microsoft Defender XDR Features for Mitigation
- **Security Score:** Comprehensive assessment of security posture
- **Threat Hunting Tools:** Enable proactive searching for suspicious activities
- **Automated Investigation and Response (AIR):** Automates investigation and response actions
- **Microsoft Security Experts:** Leverage Microsoft's expertise for tailored security guidance

### Malware Infection Investigation

#### Investigating Malware with XDR
1. Identify the affected systems and users using XDR to search for known malware IOCs.
2. Determine the scope of the infection by investigating network traffic and file activity.
3. Identify the root cause by investigating how the malware was introduced.
4. Remediate the infection by removing malware, restoring data, patching vulnerabilities.
5. Prevent future infections by implementing additional security controls.

#### Investigating Malware with SIEM
(SIEM-specific investigation methods would be detailed here)

### Ransomware Infection Investigation

#### Detecting and Responding to Ransomware with XDR

**Detection:**
1. Use XDR to correlate data from various sources to identify suspicious activity.
2. Look for signs of ransomware attack:
   - Unusual network traffic patterns
   - Unusual file activity (large number of files being encrypted or deleted)
   - Unusual login attempts
   - Users reporting encrypted files or inability to access systems
3. Use XDR to investigate suspicious activity and determine if it's a ransomware attack.

**Response:**
1. Use XDR to isolate affected systems from the rest of the network.
2. Identify the ransomware variant affecting your systems.
3. If possible, restore affected systems from backups.
4. After responding, take steps to improve security posture and prevent future attacks.

**Additional Tips:**
- Use XDR to automate tasks such as data collection, threat detection, and incident response.
- Use XDR to collaborate with other security teams.
- Use XDR to monitor the attack after responding to ensure full remediation.

---

## Analytics & Visualization

### Dashboards

#### Types of Dashboards

**Executive Dashboard**
- Provides high-level overview of security posture for executives
- Includes metrics: number of security events, open security incidents, top threats detected
- Used by executives to make informed decisions about security investments

**Compliance Dashboard**
- Tracks compliance with security policies and regulations
- Includes metrics: policy violations, open security findings, outstanding compliance tasks
- Used by security managers and compliance officers

**Security Overview Dashboard**
- Provides high-level overview of security posture for security analysts and managers
- Metrics: security events by type, by severity level, top source IPs, top users, top applications, top threats

**Incident Response Dashboard**
- Provides single view of all open security incidents
- Includes: incident status, incident owner, estimated time to resolution
- Used to track progress of incident response activities

**Threat Hunting Dashboard**
- Provides tools and data for analysts to hunt for threats
- Includes visualizations of network traffic, user activity, security events
- Used to proactively identify threats

**Patching Compliance Dashboard**
- Overall patching compliance
- Windows patching compliance
- Linux patching compliance

**Vulnerability Tracking Dashboard**
- Total number of vulnerabilities
- Number by severity
- Number having malware kits and exploits
- Number by environment
- Number by product type
- Top Zero-day vulnerabilities

**Cloud Security Dashboard**
- Secure score over time
- Security control implementation by domain
- Cloud security recommendations by severity

**Firewall Monitoring Dashboard**
- Total allow/deny traffic
- Allow/deny traffic by region
- List resources receiving high number of traffic
- List of source IPs of highest inbound traffic

### Reports

#### Types of Reports in SIEM

**Security Events Report**
- Detailed overview of all security events during specified period
- Includes: type of event, severity level, source IP, destination IP

**Incident Response Report**
- Summary of all open security incidents
- Includes: incident ID, status, assigned analyst, estimated time to resolution

**Threat Hunting Report**
- Summary of all threat hunting activities
- Includes: date/time, analyst who performed activity, findings

**Compliance Report**
- Summary of organization's compliance with security policies and regulations
- Includes: policy/audited regulation, findings, actions taken

**Executive Report**
- High-level overview of security posture for executives
- Includes: number of security events, open incidents, top threats detected

### Workbooks

Microsoft Sentinel Workbooks are a key feature for both threat detection and data visualization. They analyze and interpret data to identify threats, and visualize data within the Sentinel workspace using graphs, trends, charts, and dashboards built with KQL.

#### Key Functions of Workbooks
- **Threat Detection:** Analyze and interpret data to identify potential security threats
- **Data Visualization:** Present data in user-friendly format using graphs, charts, trends, and summary dashboards

#### Workbook Features
- KQL-Driven: All dashboards are powered by KQL queries
- Built-in Templates and Recommendations: Microsoft provides pre-built workbooks
- Customization: Templates can be customized, users can create their own workbooks
- Advanced Visualizations: Support for creating sophisticated visual representations
- Data Analysis: Facilitate viewing and analysis of Sentinel data
- Incident Metric Tracking: Security Operations Efficiency workbook helps monitor incident metrics

### KQL Queries

#### Best Practices for Writing Efficient KQL Queries
- Use indexes on your tables to improve performance
- Filter your data as early as possible in your query
- Use appropriate data types for your columns
- Avoid using nested queries
- Use the explain statement to understand the execution plan

#### Common KQL Operators

**Where**
Filters a table to the subset of rows that satisfy a predicate.

**Extend**
Creates calculated columns and appends new columns to the result set.

**Order**
Sorts the rows of the input table by one or more columns.

**Project**
Controls what columns to include, add, remove, or rename in the result set.

**Render**
Generates a visualization of the query results (areachart, barchart, columnchart, piechart, scatterchart, timechart).

**Summarize**
Aggregates data, often used with bin() function to create time series.

**Union**
Takes 2 or more tables and returns rows of all of them.

**Join**
Merges rows of two tables to form a new table by matching specified columns' values.

**Extract**
Gets a match for a regular expression from a text string.

**Parse**
Evaluates a string expression and parses its value into one or more calculated columns.

#### Testing KQL Queries
- Use the KQL explain statement to show execution plan
- Use the KQL trace statement to show step-by-step execution
- Use KQL testing tools such as KQL Query Analyzer in Azure Monitor
- Use Livestream in Sentinel to test queries continuously

#### Sample KQL Queries

**List MDC alerts:**
```kql
SecurityAlert
| where ProductName == "Azure Security Center"
```

**Powershell execution events that could involve download:**
```kql
Union DeviceProcessEvents, DeviceNetworkEvents
| where Timestamp > ago(7d)
| where FileName in~ ("powershell.exe", "powershell_ise.exe")
| where ProcessCommandLine has_any ("WebClient", "DownloadFile", "DownloadData", "DownloadString", "WebRequest", "Shellcode", "http", "https", "Invoke-Expression", "IEX", "bitsadmin", "certutil", "ftp", "tftp", "curl", "wget")
| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, FileName, ProcessCommandLine, RemoteIP, RemoteUrl, RemotePort, RemoteIPType
| top 100 by Timestamp
```

**Credential Access/Private Key Files:**
```kql
DeviceFileEvents
| where Timestamp > ago(7d)
| where FileName endswith '.pfx' or FileName endswith '.pfn' or FileName endswith '.p12'
```

**Detect mass secret retrieval from Azure Key Vault:**
```kql
AzureDiagnostics
| where ResourceType == "VAULTS"
| where OperationName == "SecretGet"
| where ResultSignature == "Success"
| summarize SecretGetCount=count() by Caller, bin(TimeGenerated, 10m)
| where SecretGetCount > 50
```

### Analytics Rules

Sentinel analytics rules are crucial for threat detection and identifying anomalous behavior. They leverage KQL to analyze data from various sources, correlate events, and pinpoint anomalies.

#### Key Capabilities
- **Threat Detection:** Identifying potential security threats
- **KQL Queries:** Custom KQL queries form the basis of these rules
- **Data Correlation:** Rules analyze data from multiple sources
- **Anomaly Detection:** Identifying anomalous behavior that deviates from baselines
- **Alerting:** Rules can trigger alerts based on detected attack techniques
- **Incident Insights:** Provide insights into attack origin, compromised resources, data loss, timeline

#### Types of Analytics Rules
- **Built-in:** Anomaly, Fusion, Machine Learning (ML), and Microsoft security rules
- **Custom:** Scheduled rules created by users to address specific threats

#### Analytics Rule Types
- **Scheduled Rules (Custom):** Most common type, created using KQL, run on a schedule
- **Near-Real-Time (NRT) Rules:** Designed for rapid threat detection, run every minute
- **Anomaly Rules:** Use statistical analysis to identify unusual patterns
- **Microsoft Security Rules (Built-in):** Pre-built rules based on Microsoft's threat intelligence
- **Fusion Rules (Built-in):** Correlate multiple anomalies and alerts to detect complex attacks
- **Machine Learning (ML) Rules (Built-in):** Use machine learning for behavioral analytics

---

## Threat Hunting

### What is Threat Hunting?

Threat hunting means proactive identification of threats by analyzing the logs. KQL queries are used to analyze logs in Sentinel workspace.

### Threat Hunting Capabilities
- Create custom hunting queries
- Run hunting queries manually
- Monitor hunting queries by using Livestream
- Perform advanced hunting with notebooks
- Track query results with bookmarks
- Use hunting bookmarks for data investigations
- Convert a hunting query to an analytical rule

### Threat Hunting Stages
- Before incident
- During compromise/incident
- After compromise/incident

### Threat Hunting Before Compromise

#### Techniques
- **Hypothesis-driven hunting:** Develop a hypothesis about a potential threat and use data to investigate
- **Anomaly detection:** Use data and tools to identify anomalous activity in the network
- **Indicators of compromise (IOCs):** Use IOCs to search for evidence of threats
- **Threat intelligence:** Use threat intelligence to inform hunting activities

#### Specific Examples
- Monitor for unusual login activity
- Monitor for unusual network traffic
- Monitor for suspicious file activity
- Search for known IOCs
- Analyze threat intelligence

### Threat Hunting During Compromise
(Detailed investigation techniques during active compromise)

### Threat Hunting After Compromise
(Post-incident analysis and lessons learned)

### Use Cases for Threat Hunting
- Convert a hunting query to an analytical rule
- Create custom hunting queries
- Detection of data exfiltration by attackers
- Detection of insider's threats
- Identification of compromised accounts
- Investigation incidents
- Monitor hunting queries by using Livestream
- Network traffic analysis to locate trends indicating potential attacks
- Perform advanced hunting with notebooks
- Run hunting queries manually
- Track query results with bookmarks
- Use hunting bookmarks for data investigations
- User behaviour to detect suspicious patterns

---

## Troubleshooting

### How to Troubleshoot XDR Issues

#### General Troubleshooting Steps
- Gather information about the issues or errors or steps taken to resolve issue
- Check the XDR logs
- Search for known issues on the XDR vendor's website or support portal
- Contact the XDR vendor for assistance
- Check the XDR configuration
- Restart the XDR services
- Update the XDR software
- Collect XDR diagnostic data

### Common Issues

#### XDR Agent Not Reporting Data
- Verify that the XDR agent is installed correctly
- Verify that the XDR agent is configured correctly
- Restart the XDR agent service
- Check the XDR agent logs for errors

#### XDR Console Not Responding
- Restart the XDR console service
- Clear the XDR console cache and cookies
- Try accessing the XDR console from a different browser
- Contact the XDR vendor for assistance

#### XDR Alerts Not Being Generated
- Verify that XDR alerts are configured correctly
- Check the XDR logs for errors
- Contact the XDR vendor for assistance

---

## Additional Components

### Microsoft Defender for Identity (MDI)

Microsoft Defender for Identity (MDI) strengthens on-premises Active Directory security by:
- **Detecting malicious activity:** Identifies suspicious behaviours like reconnaissance, lateral movement, and privilege escalation
- **Providing security insights:** Offers visibility into user and entity behaviour, revealing potential vulnerabilities
- **Recommending improvements:** Suggests actions to bolster security and reduce the attack surface

MDI sensors can be directly installed on **Active Directory Federation Services (ADFS) servers and Domain Controllers** to collect data about Active Directory activity. MDI is specifically designed for protecting on-premises Active Directory environments.

### Microsoft Defender for Cloud Apps (MDCA)

Microsoft Defender for Cloud Apps (formerly MCAS) provides:
- Cloud App Discovery: Detecting employees using new cloud apps
- Information Protection: Detecting employees sharing confidential files with external cloud services
- Shadow IT monitoring and control
- Cloud security posture management

#### Cloud App Discovery Prerequisites
- Enable integration of MCAS with Microsoft Defender for Endpoint (MDE)
- Establish automatic log upload for Cloud Discovery reports from firewalls and network devices

---

## Scenario-based QnA

1. **One of the employees accidentally runs executable from email, which steals employee credentials. What solution can be used to respond to these types of threats?**
   - Microsoft Defender for Office 365

2. **User in accounting department violates policy related to risk IP address by accessing it. Task is assigned to you to resolve issue. You access MDCA portal's alert page. What remediation will you perform?**
   - Investigate the context, communicate with the user, and take action based on investigation (block IP, suspend account, revoke access, or educate user)

3. **Employee sends email outside organization with sensitive information. Manager wants incident should be identified as Red Incident by Defender. What 2 actions will you perform?**
   - Edit the incident and add a tag named "Red"

4. **How to write advanced hunting query that counts failed sign-in authentications on 2 devices named device1 and device2?**
   ```kql
   DeviceLogonEvents
   | where DeviceName in ("device1", "device2")
   | where ActionType == "LogonFailed"
   | summarize LogonFailureCount = count() by DeviceName
   ```

5. **While investigating incident, how to categorize and associate alerts with incidents?**
   - Open the incident details page and use the option to link related alerts to the incident

6. **Incident involved risk user sign-in was blocked because of MFA not completed, but credentials was correct. You contacted user and sign-in was not user in question. User completed SSPR and updated the password. Now what manual risk detection resolution should we select?**
   - Dismiss user risk

7. **In KQL query results, how to include only last 2 weeks and only 50 results, sorted by TimeRange column?**
   ```kql
   YourTable
   | where Timestamp > ago(14d)
   | top 50 by Timestamp desc
   ```

8. **The automated investigation has quarantined a file believed to be malicious on 12 devices. We completed further research and found out that file is not malicious. How to remove this file from quarantine?**
   - Action center > History tab > select the file > Undo (Apply to all instances)

9. **What permissions/roles are required to configure data loss prevention policy (DLP)?**
   - Compliance Data Administrator, Communication Compliance Analyst, Communication Compliance Viewer

10. **What permissions/roles are required to configure insider risk management policy?**
    - IRM Admin, IRM Analyst, IRM Investigator, IRM Auditor

11. **Alert has triggered and automated investigation has initiated. On analyzing the progress its status shows "Terminated by System". What 2 reasons cause this issue?**
    - Pending actions timed out (after one week)
    - Actions are too numerous (resource exhaustion)

12. **How to create Safe attachments policy that fulfills tracking requirement and send malicious email to admin for review?**
    - Enable redirect, enter admin's email address, select "Block" or "Replace" (not "Monitor")

13. **What is meant by secure score?**
    - Secure Score helps assess and improve an organization's security posture, but it's not a direct solution for specific threats like credential theft.

---

## Additional Resources

### Documentation Links
- Microsoft Defender for Cloud: https://learn.microsoft.com/en-us/microsoft-365/security/office-365-security/?view=o365-worldwide
- Alerts Reference: https://docs.microsoft.com/en-us/azure/defender-for-cloud/alerts-reference
- Sentinel Playbooks: https://learn.microsoft.com/en-us/azure/sentinel/tutorial-respond-threats-playbook
- Logic Apps: https://learn.microsoft.com/en-us/azure/logic-apps/quickstart-create-example-consumption-workflow

### GitHub Resources
- MDC Remediation Scripts: https://github.com/Azure/Microsoft-Defender-for-Cloud/tree/main/Remediation%20scripts
- ServiceNow Integration: https://github.com/Azure/Microsoft-Defender-for-Cloud/blob/main/Workflow%20automation/Create-SNOWCRfromASCRec/azuredeploy.json

### Community Resources
- Isolate Azure VM using ASC Workflow Automation: https://techcommunity.microsoft.com/t5/microsoft-defender-for-cloud/how-to-isolate-an-azure-vm-using-azure-security-center-s/ba-p/1250985
- Automate ASC actions with Playbooks and ServiceNow: https://techcommunity.microsoft.com/t5/microsoft-defender-for-cloud/automate-azure-security-center-actions-with-playbooks-and/ba-p/264843
- Automating change requests in ServiceNow: https://techcommunity.microsoft.com/t5/microsoft-defender-for-cloud/azure-security-center-automating-change-requests-in-servicenow/ba-p/1285670

---

*This document provides a comprehensive guide to Microsoft Defender XDR, covering concepts, implementation, investigation, response, and troubleshooting. For the most up-to-date information, always refer to official Microsoft documentation.*
