# Nessus Essential Scan on Metasploitable 2

This project involves using Nessus Essential to perform a vulnerability assessment on the Metasploitable 2 virtual machine. The purpose is to identify and analyze security weaknesses in a controlled environment using the free version of Nessus. <br>


## Tools Used
- **Nessus Essential**: A free tool for identifying security vulnerabilities and weaknesses in systems and applications. <br>
- **Kali Linux**: A penetration testing distribution used to run Nessus. <br>
- **Metasploitable 2**: A vulnerable virtual machine used for testing and training. <br>

## Overview
The project includes: <br>
- Configuration of Nessus on Kali Linux. <br>
- Scanning of the Metasploitable 2 machine. <br>
- Analysis of the vulnerability report generated. <br>

## Getting Started
1. Set up Kali Linux and install Nessus. <br>
  - Downlaoded and installed [Kali Linux](https://www.kali.org/get-kali/#kali-installer-images) in [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
  - Signed up for [Nusses Essentials](https://www.tenable.com/products/nessus/nessus-essentials).
    -  Opened Terminal in Kali Linux and installed Nessus using the following [guide](https://docs.tenable.com/nessus/Content/InstallNessusLinux.htm).
    -  Started Nessus using the command 'sudo service nessusd start'.
    -  Did *ifconfig* to get IP of Kali Linux virtual machine.
  - Accessed Nessus via 'https://localhost:8834'.
    - Set up an account and activated Nessus Essentials using the activation code from signup.
2. Deploy Metasploitable 2. <br>
    - Downloaded and installed [Metasploitable 2] in VirtualBox.
    - Signed in using default credentials (msfadmin/msfadmin).
    - Did *ifconfig* to get IP of Metasploitable 2 virtual machine.
    - Ran a ping command test to verify connection between the two devices.
3. Perform the vulnerability scan using Nessus. <br>
4. Review the scan results to identify potential security issues. <br>
