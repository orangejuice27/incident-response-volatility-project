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
