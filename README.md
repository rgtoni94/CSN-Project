# CSN-Project

Software Evaluating - Metasploit

Name - Ricardo Antonio

# Tools used
- Metasploit - Security Tool that uses known exploits and is able to load and execute them in as a payload on vulnerable victim machines
- Kali Linux - Pen Testing OS used by InfoSec professionals, comes preinstalled with pen testing software
- Metasploitable - intentionally vulnerable Linux VM 
- Virtual Box - hypervisor used for creation and managment of Virutal Machines

# Reason why working with Metasploit 
Metasploit is industry recognized and used by InfoSec professionals for testing networks for vulnerabilites. By researching this tool and learning how it works, I will gain valuable experience in CyberSecurity.

# Overview of Metasploit
The workflow of metasploit is as follows:
- Run msfconsole in terminal
- Scan victim machine for exploits
- Load exploit in payload
- Execute payload against target machine

# Project
Use Metasploit on a Kali Linux VM to use an exploit, VSFTPD, to gain access backdoor root access to victim machine. We will be exploiting the VSFTPD vulnerability. VSFTPD is a secure unix based ftp server, this vulnerability was discovered in 2011 in version 2.3.4 of VSFTPD. 

# Project Setup
Tools to download
- Kali linux
- Metasploitable 2
- Virtualbox

# Steps

1. Install Kali Linux and Metasploitable VMs into Virutal Box

2. Remove Kali and Metasploitable from your network by changing Network option to Host-only Adapter, so that you don't leave your network vulnerable

<img width="597" alt="SNIP-1" src="https://user-images.githubusercontent.com/98781636/167211743-03a9c129-4649-43f2-9e20-ebfc9032a972.PNG">

3. Start Metasploitable VM on Virtual box, login and password will be msfadmin

4. Once Metasploitable VM is started, power on Kali Linux, once in Kali open terminal and run command 'msfconsole' to start metasploit shell

<img width="89" alt="SNIP-2" src="https://user-images.githubusercontent.com/98781636/167217134-6a38eedc-29fe-489b-9fc2-ad5c0633fc14.PNG">

5. Run the command 'search vstfpd' to search for the vulnerability by name

<img width="467" alt="SNIP-3" src="https://user-images.githubusercontent.com/98781636/167223056-f611ba3c-b94b-4a78-be36-7b87c9021d10.PNG">

6. Once search reveals location of vulnerability, load it into the payload by typing 'use exploit/unix/ftp/vsftpd_234_backdoor'

<img width="278" alt="SNIP-4" src="https://user-images.githubusercontent.com/98781636/167223076-22351d64-0b65-49d5-a4e4-d6ece15ad55d.PNG">

7. Type 'set RHOST [VICTIM IP]' to start attack on victim machine

<img width="346" alt="SNIP-5" src="https://user-images.githubusercontent.com/98781636/167223117-4365ed65-28c9-46dc-a8bc-7f8c5fc98057.PNG">

8. To find IP address of Metasploitable machine type 'ifconfig' into the shell

9. Run the 'run' command on the kali machine msf console

<img width="404" alt="SNIP-6" src="https://user-images.githubusercontent.com/98781636/167223155-07305578-62a5-4fe9-a759-299e9cfce4dc.PNG">

10. You now have root access into the machine!
