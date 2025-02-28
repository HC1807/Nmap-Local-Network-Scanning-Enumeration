# Nmap: Local-Network-Scanning-Enumeration
This repository provides a comprehensive guide and scripts for network scanning and enumeration using Nmap, one of the most powerful tools for network discovery and security auditing. Whether you're an ethical hacker, system administrator, or cybersecurity enthusiast, this guide will help you efficiently map out network devices, open ports, and running services.

#  Features
* Host Discovery: Identify live devices on the network.
* Port Scanning: Detect open ports and services.
* OS & Service Fingerprinting: Identify the operating system and software versions running on hosts.
* Vulnerability Detection: Find potential security issues using NSE (Nmap Scripting Engine).
* Aggressive vs. Stealth Scanning: Choose between deep enumeration or low-profile scans.
* Custom Scripts: Automate scans for quick analysis.

#  INSTALLATION
# Linux
    sudo apt update && sudo apt install nmap -y

# Basic Usage
    nmap -sn 192.168.1.0/24
* This command scans an entire subnet to find active devices without probing individual ports.
  
* -sn (No port scan) only performs host discovery (ping scan).
  
# Scan Open Ports on a Target
    nmap -p 22,80,443 192.168.1.1
* This scans specific ports (22, 80, 443) on the target.
  
 # To scan all 65,535 ports, use:
    nmap -p- 192.168.1.1
    
# Perform OS and Service Version Detection
    nmap -A 192.168.1.1
  * -A enables aggressive mode (OS detection, service version detection, script scanning, and traceroute).
    
# Perform a Stealth Scan
    nmap -sS -T2 192.168.1.1
* -sS (SYN Scan) is a stealthier way to scan ports.
  
* -T2 sets a slower scan speed to avoid detection.

 # Scan for Known Vulnerabilities
    nmap --script vuln 192.168.1.1
* It uses the Nmap Scripting Engine (NSE) to check for security vulnerabilities.

# Save Results to a File
    nmap -oN scan_results.txt 192.168.1.0/24
* Saves scan output in normal text format.

 # For detailed reports:
    nmap -oX scan_results.xml 192.168.1.0/24






    
    





  

