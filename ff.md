### **4. Host-Based Firewall Settings (RPC and SMB Communication)**

**How an Auditor Will Check:**
- **Configuration Review**: The auditor will review the firewall configurations on endpoints to confirm that policies restricting Remote Procedure Call (RPC) and Server Message Block (SMB) communication are properly implemented. They will check if there is any unauthorized communication between endpoints that could allow lateral movement within the network.
  
- **Logs and Monitoring**: The auditor will examine logs from host-based firewalls to ensure that RPC and SMB traffic is being blocked as expected. They will verify if alerts for unauthorized communication attempts are enabled and if there is a centralized logging system where this traffic is monitored and analyzed.

- **Vulnerability Scanning**: Auditors might use vulnerability scanning tools to simulate an attack and check whether unauthorized RPC or SMB traffic is being blocked. They may also test whether the firewall is effectively limiting lateral movement in case of a compromised endpoint.

- **Whitelisted Exceptions**: If any exceptions exist for allowing RPC or SMB communication, the auditor will review these to ensure they are documented and justified. They will confirm that these exceptions are isolated to specific endpoints and not applied broadly across the network.

---

### **5. Port Whitelisting Practices (Firewall Configuration)**

**How an Auditor Will Check:**
- **Firewall Policy Review**: The auditor will begin by reviewing the organization's firewall policies to check that they are following a port whitelisting approach rather than blacklisting. This means only necessary ports based on business needs should be open, and all other ports should be blocked by default.

- **Configuration and Rule Set Audit**: They will inspect the firewall rule set to verify that only the required ports are whitelisted. The auditor will look for any unnecessary open ports or misconfigurations that could expose the system to potential attacks.

- **Penetration Testing**: Auditors may conduct penetration testing to check if they can access the network through any non-whitelisted ports. This will help ensure that the default block-all policy is functioning correctly.

- **Review of Whitelisting Procedures**: The auditor will also assess the procedures in place for reviewing and updating the list of whitelisted ports. They will check if there is a process to promptly update firewall rules when a business requirement for a specific port changes or when a new vulnerability is discovered.

- **Monitoring and Alerts**: The auditor will ensure that traffic on blocked ports is being monitored and that alerts are generated when any attempt is made to communicate through these ports. They will check if the organization has appropriate response protocols in place to address such alerts.

---

These checks will involve a combination of technical tools, such as log analysis software, vulnerability scanners, and penetration testing frameworks, as well as a thorough review of policies and documentation to ensure the organization's firewall and communication settings are secure.
