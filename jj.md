# 8 cyber sec controls

1. Web and Email Filters

Deployment and Configuration

Question: Have we deployed web and email filters across our network infrastructure?

Audit Check: The auditor will:

Review network architecture diagrams to locate web and email filtering components.

Examine procurement records or licenses for filtering solutions.

Conduct interviews with IT personnel responsible for network security.

Use network scanning tools to detect the presence of filtering devices or software.


Question: Are these filters configured to scan for known malicious domains, sources, and addresses?

Audit Check: The auditor will:

Access the configuration settings of the filters to verify threat intelligence feeds are active.

Check the subscription status to reputable threat databases.

Review the blacklist and whitelist configurations.

Analyze sample logs to confirm that malicious content is being identified and blocked.


Question: Do the filters block malicious content before messages are received and downloaded?

Audit Check: The auditor will:

Perform controlled tests by sending benign messages containing known malicious signatures to see if they are blocked.

Review system alerts and logs for instances of blocked content.

Evaluate the policies set for inbound traffic filtering.



Email and Attachment Scanning

Question: Are all emails, attachments, and downloads scanned both on the host machines and at the mail gateway?

Audit Check: The auditor will:

Verify the presence of antivirus and anti-malware solutions on host machines.

Inspect mail gateway configurations for scanning policies.

Check update logs to ensure scanning engines are up-to-date.

Review sample logs to confirm that scanning is occurring at both levels.


Question: Are we using a reputable antivirus solution for scanning?

Audit Check: The auditor will:

Identify the antivirus software in use and compare it against industry standards and certifications (e.g., AV-TEST, SE Labs).

Check for recent awards or recognitions received by the antivirus vendor.

Verify that the software is widely adopted and well-reviewed in the cybersecurity community.


Question: Is our antivirus software regularly updated to detect the latest threats?

Audit Check: The auditor will:

Review update schedules and settings within the antivirus software.

Examine logs that document when updates were last applied.

Check for any failed updates or update errors in the logs.

Confirm automatic updates are enabled and functioning.




---

2. Blocking Malicious Domains/IPs

Verification and Blocking Process

Question: Do we have a diligent process to verify and block malicious domains and IPs without disrupting business operations?

Audit Check: The auditor will:

Review documented procedures for threat verification and blocking.

Examine change management records related to updates in blocking policies.

Interview staff responsible for network security to understand the process.

Assess whether the process includes steps for impact analysis before blocking.


Question: How do we ensure that legitimate operations are not impacted when blocking these domains/IPs?

Audit Check: The auditor will:

Check for whitelisting procedures for critical business domains/IPs.

Review incident reports for any past disruptions caused by blocking.

Evaluate testing protocols used before implementing blocks.

Verify that there is a rollback plan in case legitimate services are affected.



Reference to Advisories

Question: Are we regularly referring to CSIRT-Fin and CERT-In advisories for the latest information on malicious domains, IPs, C&C DNS, and links?

Audit Check: The auditor will:

Examine subscriptions or notifications set up for CSIRT-Fin/CERT-In advisories.

Review logs or records showing receipt and acknowledgment of advisories.

Check for documented procedures that incorporate these advisories into security updates.


Question: How frequently do we update our security measures based on these advisories?

Audit Check: The auditor will:

Analyze update logs to determine how promptly advisories are acted upon.

Review policies that dictate the frequency of security updates.

Interview IT staff to confirm adherence to update procedures.




---

3. Restricting "PowerShell" and "wscript" Execution

Execution Restrictions

Question: Have we restricted the execution of "PowerShell" and "wscript" in our enterprise environment where they are not required?

Audit Check: The auditor will:

Review Group Policy Objects (GPOs) to see restrictions on script execution.

Inspect endpoint configurations for execution policies.

Use security tools to scan for unauthorized use of "PowerShell" and "wscript".

Interview system administrators about the necessity and control of script execution.


Question: Is there a policy in place outlining where and when "PowerShell" and "wscript" can be used?

Audit Check: The auditor will:

Request and review the organization's security policies regarding script execution.

Check for employee acknowledgments of policy understanding.

Assess training materials or sessions that cover these policies.



PowerShell Configuration

Question: Are we using the latest version of PowerShell with enhanced logging features enabled?

Audit Check: The auditor will:

Verify the PowerShell version installed on various systems.

Check configuration settings for logging features.

Review logs to confirm that enhanced logging is operational.

Examine update policies to ensure PowerShell is kept up-to-date.


Question: Have we enabled script block logging and transcription in PowerShell?

Audit Check: The auditor will:

Inspect PowerShell execution policies and logging settings.

Review GPOs enforcing script block logging and transcription.

Analyze sample logs to ensure they contain detailed execution data.


Question: Are the logs generated by PowerShell sent to a centralized log repository for monitoring and analysis?

Audit Check: The auditor will:

Verify the log forwarding configurations on endpoints.

Inspect the centralized log repository for receipt of PowerShell logs.

Evaluate monitoring tools and alert systems that analyze these logs.

Review retention policies for log data.




---

4. Host-Based Firewall Settings

RPC and SMB Communication

Question: Are host-based firewalls configured to prevent Remote Procedure Call (RPC) and Server Message Block (SMB) communication between endpoints whenever possible?

Audit Check: The auditor will:

Review firewall settings on a sample of endpoints.

Analyze network policies restricting RPC and SMB traffic.

Use network scanning tools to detect open RPC/SMB ports between endpoints.

Check for exceptions and assess their validity.


Question: Have we identified systems where RPC and SMB communication is necessary and limited it to those systems?

Audit Check: The auditor will:

Request documentation that lists systems requiring RPC/SMB communication.

Verify firewall rules that allow RPC/SMB only between specified systems.

Confirm that unnecessary endpoints do not have access.

Review change management records for updates to these rules.



Limiting Lateral Movement

Question: How are we monitoring for unauthorized RPC and SMB communications that could indicate lateral movement by an attacker?

Audit Check: The auditor will:

Examine the monitoring tools used for network traffic analysis.

Review logs and alerts specifically related to RPC/SMB activities.

Assess the configuration of intrusion detection systems (IDS) or intrusion prevention systems (IPS).

Evaluate the incident response procedures when suspicious activity is detected.


Question: Do we have intrusion detection systems in place to alert us of suspicious activities related to RPC and SMB?

Audit Check: The auditor will:

Verify the deployment and configuration of IDS/IPS solutions.

Review the signatures or rules that detect RPC/SMB anomalies.

Test alert mechanisms to ensure they are functioning properly.

Check the escalation procedures following an alert.




---

5. Port Whitelisting Practices

Firewall Configuration

Question: Do we implement port whitelisting at the firewall level based on actual business needs?

Audit Check: The auditor will:

Review firewall rule sets to ensure only necessary ports are open.

Compare open ports against documented business requirements.

Inspect any temporary rules for appropriateness and expiration.

Evaluate the process for approving and implementing firewall changes.


Question: Is our default firewall setting to block all ports except those explicitly whitelisted?

Audit Check: The auditor will:

Check the default policies on firewalls to confirm a 'deny all' stance.

Review configuration files or management console settings.

Test the firewall behavior by attempting to access non-whitelisted ports.



Review and Maintenance

Question: How often do we review the list of whitelisted ports to ensure they are still necessary for business operations?

Audit Check: The auditor will:

Examine schedules or policies dictating the frequency of reviews.

Review meeting minutes or records from previous reviews.

Check for any outdated or unnecessary ports that remain open.

Assess the effectiveness of the review process in removing obsolete rules.


Question: Do we have procedures in place to quickly update port configurations in response to emerging threats?

Audit Check: The auditor will:

Review the incident response plan for processes related to firewall updates.

Check for documented procedures on emergency change management.

Verify past instances where rapid updates were made and evaluate their execution.

Interview network security staff about their readiness to implement urgent changes.




---

These notes provide insight into how an auditor would verify compliance with the cybersecurity controls outlined in the Securities and Exchange Board of India circular. The auditor's approach typically includes:

Documentation Review: Assessing policies, procedures, and records to ensure controls are defined and communicated.

Configuration Analysis: Examining system and device settings to verify that controls are implemented correctly.

Interviews and Observations: Engaging with personnel to understand processes and observe practices in action.

Testing and Verification: Conducting tests, such as simulated attacks or control evaluations, to confirm effectiveness.


By understanding these audit methodologies, your organization can better prepare for assessments and strengthen its cybersecurity posture.

