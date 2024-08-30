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
1. Set up Kali Linux and install Nessus.
  - Downloaded and installed [Kali Linux](https://www.kali.org/get-kali/#kali-installer-images) in [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
  - Signed up for [Nusses Essentials](https://www.tenable.com/products/nessus/nessus-essentials).
    -  Opened Terminal in Kali Linux and installed Nessus using the following [guide](https://docs.tenable.com/nessus/Content/InstallNessusLinux.htm).
    -  Started Nessus using the command 'sudo service nessusd start'.
      - When using the command I was asked to enter my Kali Linux password.
    -  Did *ifconfig* to get IP of Kali Linux virtual machine.
  - Accessed Nessus via 'https://localhost:8834'.
    - Set up an account and activated Nessus Essentials using the activation code from signup.
2. Deploy Metasploitable 2.
    - Downloaded and installed [Metasploitable 2](https://sourceforge.net/projects/metasploitable/) in VirtualBox.
    - Signed in using default credentials (msfadmin/msfadmin).
    - Did *ifconfig* to get IP of Metasploitable 2 virtual machine.
    - Ran a ping command test to verify connection between the two devices.
3. Perform the vulnerability scan using Nessus. <br>
    - Pressed on **New Scan** on the right side of the screen and was given a couple of Scan Templates to choose from.
    - The **first** scan I did was a **Host Discovery** scan found under the **Discovery** template. I entered the IP address of the Metasploitable 2 virtual machine in the **Targets** field and ran the scan. It took a few minutes and I was able to see the results after.
    - The **second** scan I did was a **Basic Network Scan** found under the **Vulnerabilities** template. I did the same thing and entered the IP address of the Metasploitable 2 virtual machine in the **Targets** field and ran the scan. It also looks like theres was a tab for Credentials.
    - The **third** scan I did was also the **Basic Network Scan**. This time I entered the IP address in the **Targets** field then clicked on the Credentials tab. I wasn't sure what to do in the Credentials tab so I looked it up a quick guide on what could be done in it. I was then able to use the Metasploitable 2 Credentials for this scan by clicking on the SSH section under the categories. I changed the Authentication method to password and filled in the *Username* and *Password* field using the login default credentials of (msfadmin/msfadmin). I clicked on save and then ran the scan. This scan took a lot longer than the scan before but I think it's because it was able to use the credentials to ran a more detailed and thorough scan.
    - The **fourth** scan I did was a **Malware Scan** also found under the **Vulnerabilities** template. I entered the same information as I did for the Credential scan prior and ran it.
    - The **fifth** scan I did was the **Active Directory Starter Scan**. I entered the IP address in the **Targets** field and nothing in the Credentials tab and ran the scan.
4. Review the scan results to identify potential security issues. <br>
    - The first scan from the Host Discovery scan resulted in 
