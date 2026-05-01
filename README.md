# Memory Forensics Investigation Using Volatility

## Overview
For this project, I performed a memory forensic analysis using Volatility to examine a RAM image and figure out what was happening on a system at the time it was captured. The goal was to identify any suspicious or malicious activity, including hidden processes, unusual commands, and network connections.

This project focuses on actually understanding the output, not just running commands.

---

## Objectives
- Identify running processes at the time of capture  
- Detect suspicious or hidden processes  
- Analyze command line activity  
- Investigate network connections  
- Find indicators of compromise (IOCs)  

---

## Tools Used
- Volatility  
- Volatility 3  
- Python  

---

## Dataset
The memory image used in this project was provided as part of a digital forensics lab. Due to file size, the raw memory dump is not included in this repository.

---

## Methodology

I used multiple Volatility plugins to analyze different aspects of the system:

### Process Analysis
volatility -f memory.raw windows.pslist

This was used to list all running processes and get a baseline of what was active.

### Network Analysis

volatility -f memory.raw windows.netscan

This helped identify any active or suspicious network connections.

### Command Line Investigation

volatility -f memory.raw windows.cmdline

Used to see what commands were executed, which can reveal attacker behavior.

### Malware Detection

volatility -f memory.raw windows.malfind

This was used to detect injected or potentially malicious code inside processes.

---

## Key Findings

During the analysis, I found:

- Suspicious processes that did not match normal system behavior  
- Unusual parent-child process relationships  
- Signs of possible code injection  
- Network connections that could indicate external communication  

These findings suggest that the system may have been compromised.

---

## Analysis

Instead of just listing outputs, I focused on understanding what they meant. For example, when looking at processes, I checked if anything looked out of place or if processes were spawning in ways they normally shouldn’t.

The `malfind` results were especially important because they can indicate injected code, which is a strong sign of malware.

---

## Indicators of Compromise (IOCs)
- Suspicious process names  
- Abnormal process behavior  
- Potential injected memory regions  
- Unusual network connections  

---

## Recommendations
- Implement endpoint detection and response (EDR) tools  
- Monitor process behavior more closely  
- Regularly analyze memory for threats  
- Improve system logging and alerting  

---

## Conclusion

This project showed how powerful memory forensics can be when investigating cyber incidents. Using Volatility, I was able to go beyond surface-level analysis and look directly at what was happening in memory.

Overall, this investigation highlights how attackers can leave traces in RAM, even if they try to hide on disk.

---

## References
- Volatility Documentation  
