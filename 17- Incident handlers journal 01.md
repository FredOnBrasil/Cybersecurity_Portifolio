# Incident Journal Entry

**Date:** April 19, 2025

## Description
A user downloaded an attachment from an email that was provided with a password. After the download, the user typed the password into the file, which resulted in the execution of multiple unauthorized executables on the user's endpoint, ultimately infecting the machine.

## Tool(s) Used
In this case, we utilized **VirusTotal** to investigate the hash code of the file.

### More Information from VirusTotal:
- **Popular Threat Label:** trojan.flagpro/fragtor
- **Basic Properties:**
  - **MD5:** 287d612e29b71c90aa54947313810a25
  - **SHA-1:** 8f35a9e70dbec8f1904991773f394cd4f9a07f5e
  - **SHA-256:** 54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b
- **File Type:** Win32 EXE executable (Windows Win32)
- **Compiler:**
  - EP: Microsoft Visual C/C++ (2008-2010) [EXE32]
  - Microsoft Visual C/C++ (15.00.21022) [LTCG/C++]
- **Linker:** Microsoft Linker (9.00.21022)
- **Tool:** Visual Studio (2008)
- **File Size:** 430.00 KB (440320 bytes)

## The 5 W's
- **Who caused the incident?** A user from this company.
- **What happened?** After the download and insertion of the password provided via email, multiple unauthorized executable files were created on the employee’s computer.
- **When did the incident occur?** 1:13 p.m.
- **Where did the incident happen?** On the employee’s computer.
- **Why did the incident happen?** Because of the user’s action of opening the infected file. Following this action, the Security Operations Center (SOC) was alerted to intrusion activity.

## Additional Notes
After the actions of the employee, what measures will be taken to prevent this from happening again?
