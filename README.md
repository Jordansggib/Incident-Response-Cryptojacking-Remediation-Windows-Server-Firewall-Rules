# Incident-Response-Cryptojacking-Remediation-Windows-Server-Firewall-Rules
Project simulating a high-priority incident response (IR) lifecycle. Features forensic analysis, cryptojacking eradication (XMRig miner), and network hardening by implementing DMZ firewall rules and endpoint security controls. Demonstrates practical threat containment and preventative action planning.


Incident Response & Threat Remediation Project: Cryptojacking on Production Server

This project simulates the complete lifecycle of a high-priority security incident involving unauthorized resource utilization on a Windows Engineering Application Server. The analysis, containment, and eradication steps documented here align with industry-standard incident response frameworks.

Challenge

The primary challenge was investigating and resolving unusually high GPU and CPU usage on a critical production server (WIN-6JNN6RLT6IL), which was severely impacting user access to the CAD application (Pro-Engineer).

Key Findings and Threat Identification (Investigate Phase)

Compromised System IP: 10.10.20.10 (Windows Server 2019)

Malicious Process Identified: XMRig miner (a known cryptojacking application).

Malicious Traffic Destination Port: 3333 (Used for unauthorized outgoing communication).

Functional Impact: High (Application run-time latency and timeouts, rendering the primary function of updating models unusable).

Remediation and Containment Actions

The remediation phase focused on immediate eradication and strengthening the network perimeter to prevent recurrence.

Eradication: Used anti-malware security tools to perform a quick scan and successfully remove the XMRig crypto miner software from the compromised system.

Network Hardening: A critical firewall rule was added to the DMZ (Demilitarized Zone) to block all inbound and outbound TCP traffic on port 3333. This immediately contained the malicious network communication and prevented further exploitation.

System Restoration: Functionality was restored after removing the miner, resolving the high resource utilization issues.

Lessons Learned and Preventive Actions

This incident highlighted the need for stronger preventative endpoint controls. The following actions were recommended and implemented to enhance security posture:

Action Category

Action Taken

Prevention Method

Endpoint Security

Enforced activation of Windows Defender Antivirus on all server systems.

Ensures proactive defense against malware installation (e.g., malware removal software).

Network Security

Configured and restricted DMZ firewall rules.

Ensures only necessary and authorized ports remain open, significantly reducing the attack surface.

Skills Demonstrated: Incident Handling, Threat Analysis, Digital Forensics, Network Hardening, Firewall Management, Windows Server Security, Security Documentation (Incident Reporting).
