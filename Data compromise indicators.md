
* Large amount of compressed data in wrong place such as 5TB zip file.
* Email admin see large number of bounced emails with suspicious content
* Filename with unusual characters may the files are encrypted, possible ransomware attack.
* High volumes of e-mail sent
* HTML response sizes
* Increased DB read volume
* Increased database write volume.
* Large number of requests for same file
* Look for database alerts and logs. 
* Look for storage service alerts and logs. 
* Messages demanding a ransom for the release of your files 
* People informing you of strange emails coming out of your domain
* Phishing emails with payload attachments
* Tampered files 
* Look for database alerts and logs. 

**Unusual Data Activity:**
* Large, unexpected compressed files: 5TB zip files in unusual locations could indicate data exfiltration.
* High volume of bounced emails with suspicious content: Spam or phishing attempts targeting a large number of users.
* Unusual filenames: Files with strange characters might signal encryption or other tampering.
* High email sending volume: Unexpectedly high emails sent from an account could be a sign of compromise.
* Large database read/write volume: Significant deviations from typical database activity patterns.
* Large number of requests for the same file: Unexpected surge in access attempts for a specific file.

**System and Security Alerts:**
* Database alerts and logs: Unusual activity or errors reported by database monitoring systems.
* Storage service alerts and logs: Alerts from cloud storage or file servers indicating suspicious access.
* Security software alerts: Antivirus, firewall, or IDS notifications of potential threats.
* EDR sensor issues: Endpoint detection and response sensors disabled or malfunctioning.

**User Reports:**
* Ransomware messages: Demands for payment to decrypt compromised data.
* User reports of strange emails: Users notifying IT about unusual emails sent from their accounts.
* Suspicious login attempts: Users reporting unauthorized login attempts.

**Network Activity:**
* Unusual DNS requests: Spikes in queries to suspicious domains, potentially for data exfiltration.
* Data exfiltration attempts: Signs of data being transferred out of the network.
* Lateral movement: Attempts by attackers to pivot to other internal systems.
* Tunnelling activity: Encrypted connections suggesting data obfuscation.
* High bandwidth usage by unknown processes: Unidentified applications consuming excessive bandwidth.

**Endpoint Security:**
* Anti-malware signature update failures: Inability to update anti-malware definitions.
* Security software tampering: Attempts to disable or modify security software settings.

**File System Activity:**
* Unusual file creation: Unexpected files appearing on the system, especially in sensitive locations.
* Modified system files: System files showing signs of tampering.
* Deleted logs: Missing system or application logs that could hold clues.
* Hidden files or directories: Unexplained hidden folders or files containing stolen data.
* Suspicious file names: Files with obfuscated names or unusual extensions.

**User Activity:**
* Unusual user login times: Login attempts outside the user's typical timeframe.
* Access attempts from unknown locations: Login attempts originating from unfamiliar geographical locations.
* Increased privileged account activity: Unusual activity on accounts with elevated access.
* Access to sensitive data: Unauthorized access attempts to sensitive files or folders.
* Downloaded unknown files: Downloads from untrusted sources or websites.

**Indicators of Persistence:**
* Autoruns modified: Changes to startup programs allowing attackers to maintain access.
* Scheduled tasks altered: Modifications to scheduled tasks used for malicious activity.
* Registry changes: Suspicious entries added to the system registry.
* Rootkit detection: Signs of a program designed to hide malicious processes.
* Hidden services or backdoors: Unexplained services or backdoors allowing remote access.

**Web Browsing Activity:**
* Unexpected browser extensions: Unfamiliar extensions installed in the user's web browser.
* Bookmarked malicious websites: Bookmarks to known phishing or malware distribution sites.
* Browser history changes: Deletion or modification of browsing history.

**Email Activity:**
* Sending spam emails: The endpoint sending unsolicited emails, potentially due to compromise.
* Unusual email activity: Increased email sending/receiving from compromised accounts.

**Other Indicators:**
* Unexplained peripheral device activity: Unexpected activity on external devices like USB drives.
* Microphone or webcam activation: Unexpected activation of audio or video recording devices.
* Changes in file permissions: Modification of access rights for files and folders.
* System resource exhaustion: High CPU, memory, or disk usage without apparent cause.
* Failed login attempts: Repeated login attempts from unrecognized locations.
* Brute-force attacks: Attempts to crack passwords through automated guessing.
* Anomalous port scans: Scans for vulnerabilities on other network devices.
 

* Increases in DB read volume
* HTML response sizes
* Large number of requests for same file
* Bundles of data in wrong place
* Tampered files
* Large amounts of compressed files and data in wrong place
* filename with unusual characters
* Email admin see large number of bounced emails with suspicious content
* Messages demanding a ransom for the release of your files 
* People informing you of strange emails coming out of your domain
* Phishing emails with payload attachments
* High volumes of e-mail sent
* Increases in DB read volume
* HTML response sizes
* Large number of requests for same file
* Bundles of data in wrong place
* Tampered files
* Large amounts of compressed files and data in wrong place
* filename with unusual characters
* Email admin see large number of bounced emails with suspicious content
* Messages demanding a ransom for the release of your files 
* People informing you of strange emails coming out of your domain
* Phishing emails with payload attachments
* High volumes of e-mail sent


Data Loss and Exfiltration
•	Data Misplacement: Files or data located in unexpected or unauthorized locations.
•	Email Anomalies: 
o	High volumes of bounced emails
o	Emails with suspicious content/payloads
o	Emails originating from compromised accounts/High volumes of email sent.
•	File Naming Irregularities: Files with unusual or suspicious file names.
•	Data Transfer Anomalies: Large amounts of compressed data, excessive data transfers, or unusual file access patterns.

Data Corruption and Modification
•	Database Activity: 
o	Increased database read activity without corresponding writes.
o	Large number of requests for same file.
•	File Tampering: Altered or corrupted files.

Data Breach and Ransomware
•	Ransomware Demands: Messages demanding payment for data recovery.
•	Phishing Attacks: Emails containing malicious attachments or links.
•	Website HTML response size

Users reporting suspicious activity:
•	Messages demanding a ransom for the release of your files 
•	People informing you of strange emails coming out of your domain

These IOCs are indicators of potential data-related incidents, but further investigation is often required to confirm a data breach or compromise.

•	Bundles of data in wrong place
•	Email admin see large number of bounced emails with suspicious content
•	filename with unusual characters
•	High volumes of e-mail sent
•	HTML response sizes
•	Increases in DB read volume
•	Large amounts of compressed files and data in wrong place
•	Large number of requests for same file
•	Messages demanding a ransom for the release of your files 
•	People informing you of strange emails coming out of your domain
•	Phishing emails with payload attachments
•	Tampered files 


 
## Data IoC
* •	Bundles of data in wrong place
* •	Email admin see large number of bounced emails with suspicious content
* •	filename with unusual characters
* •	High volumes of e-mail sent
* •	HTML response sizes
* •	Increases in DB read volume
* •	Large amounts of compressed files and data in wrong place
* •	Large number of requests for same file
* •	Messages demanding a ransom for the release of your files 
* •	People informing you of strange emails coming out of your domain
* •	Phishing emails with payload attachments
* •	Tampered files 

Bundles of data in wrong place
Email admins see large number of bounced emails with suspicious content
filename with unusual characters
High volumes of e-mail sent
HTML response sizes
Increases in DB read volume
Large amounts of compressed files and data in wrong place
Large number of requests for same file
Look for database alerts and logs. 
Look for storage service alerts and logs. 
Messages demanding a ransom for the release of your files 
People informing you of strange emails coming out of your domain
Phishing emails with payload attachments
Tampered files 
