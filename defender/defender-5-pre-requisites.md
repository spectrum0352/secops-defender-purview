

## Pre-requisites

To implement Microsoft Defender XDR, we need to:

1. **A qualifying Microsoft 365 subscription:** This includes Microsoft 365 E5, E5 Security, Business Premium, or Defender XDR for Business.
2. **Supported operating systems and platforms:** Windows 10/11, Windows Server 2012+, macOS, Linux, Android, and iOS.
3. **Supported devices:** Computers, laptops, mobile devices, and servers.
4. **The latest Defender XDR agent:** Installed on all supported devices to collect and transmit data.
5. **Network connectivity:** A connection to the Microsoft 365 cloud for data transfer, updates, and security intelligence.

Meeting these requirements enables Defender XDR implementation. Further details can be found in the official documentation:
<https://learn.microsoft.com/en-us/microsoft-365/security/office-365-security/?view=o365-worldwide>


## Access management

global administrator or security administrator

To manage Microsoft Defender for Endpoint within Microsoft Defender XDR, you need to assign appropriate roles and permissions. This is done via Role-Based Access Control (RBAC).

**Enabling Roles:**

1. In the Microsoft Defender XDR portal, navigate to *Settings \> Endpoints \> Permissions \> Roles*.
2. Turn on roles if they are not already enabled.

**Assigning Roles:**

1. Click "Add item" to create a new role.
2. Give the role a name and select the appropriate permissions.
3. Assign the role to users or groups. Changes to device group configuration require applying the changes.

**Built-in Microsoft Entra Roles for managing access to Microsoft Defender XDR:**

- Global Administrator (full access)
- Global Reader (read-only access)
- Security Administrator (most permissions for security-related tasks)
- Security Operator (permissions for security operations tasks)
- Security Reader (read-only access to security data)

**Custom Roles (example configurations for a Security Operations Center):**

- **Security Analyst Level-1:** *Security Data/Alerts* (view alerts and related security data)
- **Security Analyst Level-2:** *Security Data/Alerts/Response/Basic Live Response* (adds response actions and basic live response capabilities)
- **Security Analyst Level-3:** *All read and manage permissions* (full access to security data, alerts, response, and advanced live response)
- **Security Engineer:** *Security Posture, Security Data Basics, Vulnerability Management, Exception Handling, Remediation Handling, Application Handling, Security Baseline Assessment* (focus on vulnerability management and security posture)
- **Security Admin:** *Authorization and Settings (Read and Manage All Permissions)* (manages roles, permissions, and settings)

**Permission Capabilities (grouped for clarity):**

- **Data & Analysis:** Security Data (alerts, incidents, investigations, hunting, devices, reports), Vulnerability Management (vulnerability data, software inventory, weaknesses, missing updates, baseline assessments)
- **Response & Remediation:** Alert (manage alerts, investigations, scans), Response (actions on devices, remediation approvals, allow/block lists), Basic Live Response (read-only remote actions), Advanced Live Response (upload files, run scripts remotely), Exception Handling, Remediation Handling
- **Security Posture & Configuration:** Application Handling, Security Baseline Assessment, Authorization (device groups, roles), Security Settings, System Settings

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 61%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th><strong>Role Group</strong></th>
<th><strong>Permissions</strong></th>
<th><strong>Function</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Security operations</strong></td>
<td><p>All read-only permissions</p>
<p>All read and manage permissions</p>
<p>Select Custom permissions on Security Data</p>
<ul>
<li><p>Read-only</p></li>
<li><p>Select all permissions</p></li>
<li><p>Select custom permissions for security data</p>
<ul>
<li><p><strong>Security data basics:</strong> View info of incidents/alerts/investigations/advanced hunting (MDE)/devices/submissions/evaluation lab, and reports.</p></li>
<li><p><strong>Alerts</strong>: Manage alerts, start automated investigations, run scans, collect investigation packages, and manage device tags</p></li>
<li><p><strong>Response (manage):</strong> Take response actions, approve/dismiss pending remediation actions, and manage blocked and allowed lists for automation</p></li>
<li><p><strong>Email and Collaboration quarantine (manage):</strong>
View and release emails and messages from quarantine</p></li>
</ul></li>
</ul></td>
<td>manage day to day operations and respond to incident and adversaries</td>
</tr>
<tr>
<td><strong>Security posture</strong></td>
<td><p>All read-only permissions</p>
<p>All read and manage permissions</p>
<p>Select custom permissions of posture management</p>
<ul>
<li><p>Read only</p></li>
<li><p>Select all permissions</p></li>
<li><p>Select custom permissions</p>
<ul>
<li><p><strong>Secure score (read)</strong>: View Secure Score data including your current score, recommended actions, history, and metrics &amp; trends</p></li>
<li><p><strong>Secure score (manage)</strong>: Work to improve your Secure Score by editing status &amp; action plan, managing tags, and editing score zones</p></li>
</ul></li>
</ul></td>
<td>manage organizations security posture, use MDVM</td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## Data Storage

Microsoft Defender XDR data storage and retention are configured within the Microsoft 365 Defender portal
([https://security.microsoft.com](https://security.microsoft.com/)) under Settings -\> Endpoints -\> General -\> Data Retention -\> Data Storage.

- **Data Residency:** Data is stored in either the US, UK, or EU. The initial region selected during setup *cannot* be changed after configuration. Data cannot be moved between these regions.
- **Data Retention:** The default retention period is 6 months.
- **Storage Details:** Microsoft Defender XDR uses its own internal storage for logs. Specific details about this storage are not publicly disclosed for security reasons.



### Access Management

To manage Microsoft Defender for Endpoint within Microsoft Defender XDR, you need to assign appropriate roles and permissions. This is done via Role-Based Access Control (RBAC).

#### Enabling Roles:
1. In the Microsoft Defender XDR portal, navigate to Settings > Endpoints > Permissions > Roles.
2. Turn on roles if they are not already enabled.

#### Assigning Roles:
1. Click "Add item" to create a new role.
2. Give the role a name and select the appropriate permissions.
3. Assign the role to users or groups. Changes to device group configuration require applying the changes.

#### Built-in Microsoft Entra Roles:
- Global Administrator (full access)
- Global Reader (read-only access)
- Security Administrator (most permissions for security-related tasks)
- Security Operator (permissions for security operations tasks)
- Security Reader (read-only access to security data)

#### Custom Roles (example configurations for a Security Operations Center):
- **Security Analyst Level-1:** Security Data/Alerts (view alerts and related security data)
- **Security Analyst Level-2:** Security Data/Alerts/Response/Basic Live Response (adds response actions and basic live response capabilities)
- **Security Analyst Level-3:** All read and manage permissions (full access to security data, alerts, response, and advanced live response)
- **Security Engineer:** Security Posture, Security Data Basics, Vulnerability Management, Exception Handling, Remediation Handling, Application Handling, Security Baseline Assessment (focus on vulnerability management and security posture)
- **Security Admin:** Authorization and Settings (Read and Manage All Permissions) (manages roles, permissions, and settings)

#### Permission Capabilities:
- **Data & Analysis:** Security Data (alerts, incidents, investigations, hunting, devices, reports), Vulnerability Management
- **Response & Remediation:** Alert, Response, Basic Live Response, Advanced Live Response, Exception Handling, Remediation Handling
- **Security Posture & Configuration:** Application Handling, Security Baseline Assessment, Authorization, Security Settings, System Settings

### Data Storage

Microsoft Defender XDR data storage and retention are configured within the Microsoft 365 Defender portal (https://security.microsoft.com/) under Settings > Endpoints > General > Data Retention > Data Storage.

- **Data Residency:** Data is stored in either the US, UK, or EU. The initial region selected during setup cannot be changed after configuration. Data cannot be moved between these regions.
- **Data Retention:** The default retention period is 6 months.
- **Storage Details:** Microsoft Defender XDR uses its own internal storage for logs. Specific details about this storage are not publicly disclosed for security reasons.
