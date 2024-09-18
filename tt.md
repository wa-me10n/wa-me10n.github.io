#### 7. Privilege Management:

1. **Maker-Checker Framework Implementation**
   - Is a Maker-Checker framework implemented for modifying user rights in all internal applications?  
   - Are all privilege modifications, including granting, revoking, and modifying user permissions, routed through a Maker-Checker process to ensure oversight and reduce risks of errors or malicious changes?
   - How often is the effectiveness of the Maker-Checker framework reviewed, and are any exceptions allowed to bypass this process?
   - Is there a system in place to log and audit all actions related to privilege changes, with specific tracking of both the maker and checker?

2. **Least Privilege and Zero-Trust Implementation**
   - Is a formal "least privilege" policy implemented across all on-premise and cloud resources, ensuring users have only the access needed for their role?
   - How often are user access levels reviewed to ensure adherence to the least privilege principle, and is there a process for immediately revoking unnecessary access?
   - Has a Zero-Trust model been implemented, where each user or device is continuously authenticated and authorized before being granted access to any resource, regardless of network location?
   - How is identity verification enforced in the Zero-Trust model, and what mechanisms are in place (e.g., MFA, identity provider solutions) to validate users and devices before granting access to sensitive data?
   - How are off-premise users (e.g., remote workers) authenticated and granted access in accordance with the Zero-Trust model?

3. **Insider Threat Mitigation**
   - Are there automated systems in place to detect potential insider threats, such as monitoring for unusual behavior like privilege escalation, data exfiltration, or access to sensitive systems at irregular hours?
   - Is there a mechanism to track and investigate privilege abuse or misuse that could indicate insider threats?
   - How frequently is the access of high-privilege accounts audited to ensure no abuse of privileges?

#### 8. Cybersecurity Controls:

1. **Web and Email Filtering**
   - Are web and email filtering tools deployed across the network to scan incoming traffic for known malicious domains, IP addresses, and attachments?
   - Are filters configured to block known bad domains, and how often are these lists updated using threat intelligence feeds from sources such as CSIRT-Fin/CERT-In advisories?
   - Are email attachments and downloads scanned at both the mail gateway and on the host using a reputable antivirus or anti-malware solution?
   - How are users notified or protected if malicious domains or attachments are detected, and what follow-up actions are taken?

2. **Blocking Malicious Domains and IPs**
   - Is there a process in place to verify the legitimacy of malicious domains and IP addresses before blocking them to avoid disrupting business operations?
   - Are threat advisories from CSIRT-Fin and CERT-In regularly reviewed and integrated into your security controls to block malicious domains, IPs, C&C DNS servers, and malware links?
   - Is there a process to audit blocked domains/IPs to ensure operational impact is minimized while maintaining security?

3. **PowerShell and Wscript Restrictions**
   - Are "powershell" and "wscript" executions restricted across the enterprise unless absolutely required for specific business purposes?
   - If PowerShell is used, is the latest version installed with enhanced logging features enabled (e.g., script block logging, transcription logging)?
   - Are PowerShell logs being sent to a centralized log repository for continuous monitoring and analysis, and how often are these logs reviewed for suspicious activities?
   - Are any exceptions to PowerShell restrictions documented and monitored for security risks?

4. **Host-Based Firewall Configuration**
   - Are host-based firewalls configured to block unnecessary Remote Procedure Call (RPC) and Server Message Block (SMB) communication between endpoints to prevent lateral movement during an attack?
   - How often are the firewall rules reviewed and updated to ensure alignment with the latest security standards and operational requirements?
   - Are there logs that track blocked RPC and SMB communication, and are these monitored for signs of malicious activity?

5. **Port Whitelisting at Firewall Level**
   - Is port whitelisting practiced at the firewall level, ensuring that only the necessary ports are open based on business requirements?
   - Are all non-whitelisted ports blocked by default, and how is traffic on open ports monitored for potential security risks?
   - How often are firewall rules audited to ensure only the required ports are open, and is there a process to adjust whitelisted ports based on changing business needs?
   - Is there a system in place to review and respond to firewall rule changes, ensuring that no unauthorized modifications are made?
