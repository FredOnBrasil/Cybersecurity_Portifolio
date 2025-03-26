# Incident Report: Brute Force Attack via TCP Traffic

## 1. Network Protocols Involved
The incident involved the following network protocols:

- **DNS (Domain Name System)**: Used for resolving domain names to IP addresses.
- **TCP (Transmission Control Protocol)**: Used for establishing and maintaining connections.
- **HTTP (Hypertext Transfer Protocol)**: Used for web communication over port 80.

The traffic logs suggest a brute force attack through excessive HTTP requests.

---

## 2. Incident Documentation

### **Timeline and Key Observations:**

#### **1. DNS Resolution Requests:**
- The source machine (`your.machine.52444`) requested DNS resolution for `yummyrecipesforme.com`, resolving to IP `203.0.113.22`.
- Later, another request was made for `greatrecipesforme.com`, resolving to `192.0.2.172`.

#### **2. TCP Connection Establishment:**
- A SYN (`Flags [S]`) packet was sent from `your.machine.36086` to `yummyrecipesforme.com.http` (port 80), initiating an HTTP session.
- The server responded with a SYN-ACK (`Flags [S.]`), confirming the connection.
- The client acknowledged (`Flags [.]`), completing the TCP three-way handshake.

#### **3. HTTP Requests:**
- The client sent an HTTP `GET / HTTP/1.1` request.
- Multiple HTTP requests followed within a short time frame, suggesting an automated brute force attempt.

#### **4. Repetitive Patterns:**
- The pattern repeated for `greatrecipesforme.com`, showing the same sequence: DNS resolution, TCP connection, HTTP GET requests, and rapid successive traffic.
- A high volume of connections over port 80 indicates an automated attack.

---

## 3. Recommended Remediation for Brute Force Attacks

### **1. Network-Level Defenses**
- **Rate Limiting**: Restrict the number of connection attempts per second from a single IP.
- **IP Blacklisting**: Block known malicious IP addresses or those showing suspicious behavior.
- **Geo-blocking**: Restrict access from regions linked to malicious activity.
- **Deep Packet Inspection (DPI)**: Use firewall rules to detect and block malicious request patterns.

### **2. Application-Level Defenses**
- **Strong Authentication Mechanisms**:
  - Enforce multi-factor authentication (MFA).
  - Implement CAPTCHA after multiple failed login attempts.
- **Account Lockout Policy**:
  - Temporarily lock accounts after several failed login attempts.
- **Web Application Firewall (WAF)**:
  - Deploy a WAF to monitor and filter incoming HTTP traffic.

### **3. Monitoring and Logging**
- **Intrusion Detection and Prevention Systems (IDS/IPS)**:
  - Deploy tools like Snort or Suricata to detect anomalies.
- **Log Analysis**:
  - Continuously monitor logs for repeated access attempts from the same IP.

### **4. Server Hardening**
- **Disable Unused Services**: Close unnecessary ports and services.
- **Patch and Update Systems**: Keep web servers and applications up to date.
- **Implement Secure Password Policies**: Enforce strong password requirements.

---

## Conclusion
The logs indicate a brute force attack through repetitive HTTP requests over TCP. Effective defense strategies include rate limiting, account lockout policies, WAF deployment, and proactive monitoring to detect and block attacks in real time.
