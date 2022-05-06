# CSN-Project

Software Evaluating - Metasploit

Name - Ricardo Antonio

# Tools used
---Metasploit - Security Tool that uses scans machines for known exploits and is ablt to execute the exploits in a payload
---Kali Linux - Pen Testing OS used by InfoSec professionals 
---Metasploitable - Vulnerable VM used for practice for hacking into Systems
---Virutal Box - hypervisor used for creation and managment of Virutal Machines

# Reason why working with Metasploit - 
Metasploit is  idustry recognized and used by InfoSec professionals for testing networks for vulnerabilites. By researching this tool and learning how it works, I will gain valuable experience in CyberSecurity.

# Project
Use Metasploit on a Kali Linux VM to use a vulnerability to exploit vsftpd, VSFTPD a secure unix based ftp server, this vulnerability was disocvered in 2011 in version 2.3.4 of VSFTPD. Exploiting it will give us root access to the Victim Machine.

# Project Setup
Tools to download
--- Kali linux
--- Metasploitable 2
--- Virtualbox

Steps

1. Install Kali Linux and Metasploitable VMs into Virutal Box
2. Remove Kali and Metaspoiltable from your network by changing Network option to Host-only Adapter

<img width="597" alt="SNIP-1" src="https://user-images.githubusercontent.com/98781636/167211743-03a9c129-4649-43f2-9e20-ebfc9032a972.PNG">

3. Start Metasploitable VM on Virtual box, login and password will be msfadmin
4. Once Metasploitable VM is started, power on Kali Linux, once in Kali open terminal and run command 'msfconsole' to start metasploit shell

<img width="89" alt="SNIP-2" src="https://user-images.githubusercontent.com/98781636/167217134-6a38eedc-29fe-489b-9fc2-ad5c0633fc14.PNG">
5. Inside the msf shell, run the command 'search vstfpd' to search for the vulnerability by name
6. Once search reveals location of vulnerability, load it into the payload by typing 'use exploit/unix/ftp/vsftpd_234_backdoor'
7. set the IP address of the VIctim machine on your shell by typing ' set RHOST [VICTIM IP]
8. to find IP address of Metasploitable machine type 'ifconfig' into the shell
9. finally run the 'run' command on the kali machine msf console
10. you know have root access into the machine!
