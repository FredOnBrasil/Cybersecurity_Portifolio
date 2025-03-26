# Incident Report Analysis

## Summary  
In this multimedia company, there was an incident related to a **DDoS attack**. The attacker used a method called **flood of ICMP packets** to compromise the company's internal network and services, making it difficult for employees and customers to access critical resources. This situation was possible due to a **firewall misconfiguration**.  

---

## NIST Framework Analysis  

### **Identify**  
- The type of attack was a **flood of ICMP packets** exploiting a **misconfigured firewall**, affecting the internal network.  

### **Protect**  
- Recommended measures include:  
  - Implementation of a **firewall with proper rules**  
  - Deployment of an **Intrusion Prevention System (IPS)**  
  - Use of a **network monitoring tool** to detect abnormal traffic patterns  

### **Detect**  
- **Continuous monitoring** with a **SIEM tool** will help prevent similar incidents.  
- **Implementation of an IDS** will mitigate vulnerabilities and detect potential threats.  

### **Respond**  
- The response plan should include:  
  - **Communication with authorities** (e.g., FBI) to alert other companies and prevent future attacks.  
  - **Log analysis and network monitoring** to investigate and address security gaps.  

### **Recover**  
- A **recovery plan** is essential to restore normal system functions. Recommended actions include:  
  - **Regular system imaging**  
  - **Frequent backups** of crucial data to prevent data loss  
  - **Rapid recovery strategies** to minimize downtime  
