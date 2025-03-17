# Create Cybersecurity Incident Report _ SYN flood attack

## Section 1: Identify the Type of Attack That May Have Caused This Network Interruption

One potential explanation for the website's connection timeout error message is: that the server is busy trying to answer lots of SYN requests.

**The logs show that:** There is an abnormal influx of SYN requests on the server.

**This event could be:** an SYN (Synchronize) flood attack.

---

## Section 2: Explain How the Attack Is Causing the Website to Malfunction

When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol. The three steps of the handshake are:

1. **SYN Packet:** The initial request of an employee trying to access the company sales page.
2. **SYN/ACK Packet:** The server's response to the visitor's request, accepting the connection.
3. **ACK Packet:** The visitor/employee's machine acknowledges the permission to connect.

### How a Malicious Actor Exploits This Process
When a malicious actor sends a large number of SYN packets all at once, the server becomes overwhelmed and unable to respond to all requests.

### Log Analysis and Server Impact
The logs indicate a large number of SYN packets that do not follow the normal SYN-SYN/ACK-ACK sequence. Instead, the logs show multiple SYN packets being sent in sequence from at least two distinct IP addresses. This irregularity suggests a **SYN flood attack**, leading to server resource exhaustion and service disruption.
