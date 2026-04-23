# incident-response-volatility-project
This project simulates a cybersecurity incident involving a potentially compromised Windows system. Memory forensics was conducted using Volatility to analyze running processes and network activity in order to identify suspicious behavior.
Tool Used
Volatility (memory analysis tool)
Data Used
A publicly available Windows memory image (boomer-win2003) was used for analysis. This dataset represents a snapshot of system memory and allows investigation of processes and network connections.
Analysis Performed
Identified running processes using pslist
Examined network connections using netscan
Investigated potential indicators of compromise
Findings
A suspicious process was identified that did not match typical system processes. Additionally, network connections were observed that could indicate external communication.
Incident Response Actions
Isolate the affected system
Conduct further forensic analysis
Remove malicious processes
Monitor for reinfection
Incident Response Lifecycle
Detection & Analysis: Suspicious activity identified
Containment: System isolation recommended
Eradication: Remove threats
Recovery: Restore system
Lessons Learned: Improve monitoring
