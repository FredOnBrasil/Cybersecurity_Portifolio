# Cybersecurity Incident Report: Network Traffic Analysis

## Part 1: Summary of the Problem Found in the DNS and ICMP Traffic Log

The UDP protocol reveals that the port 53 is unreachable.

This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message: **“UDP port 53 unreachable.”**

The port noted in the error message is used for the **ICMP protocol**.

The most likely issue is: **ICMP flood attack**.

## Part 2: Analysis of the Data and Cause of the Incident

**Time Incident Occurred:** Between 13:24 and 13:28.

**How the IT Team Became Aware of the Incident:**  
The site was unable to respond when they tried to access it.

**Actions Taken by the IT Department to Investigate the Incident:**  
The professionals from the SOC (Security Operations Center) have taken the log from DNS and ICMP traffic in transit using data from a network protocol analyzer tool.

**Key Findings of the IT Department's Investigation:**
- **Port affected:** 53
- **DNS server:** 203.0.113.2.domain

**Likely Cause of the Incident:**  
**DoS (Denial of Service) attack.**
