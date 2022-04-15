Week 16 Homework Submission File: Penetration Testing 1
Step 1: Google Dorking
Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is: Karl Fitzgerald Chairman & Chief Executive Officer

How can this information be helpful to an attacker: The attacker can now search social media platforms using this CEO’s name to continue their enumeration.

Step 2: DNS and Domain Discovery
Enter the IP address for demo.testfire.net into Domain Dossier and answer the following questions based on the results:

Where is the company located: Sunnyvale, California

What is the NetRange IP address:0.0.0.0 - 127.255.255.255

What is the company they use to store their infrastructure: Akamai

What is the IP address of the DNS server: 65.61.137.117


Step 3: Shodan
What open ports and running services did Shodan find: Open ports : 80,443,8080
Services: TCP and Apache Tomcat/Coyote 

Step 4: Recon-ng
Install the Recon module xssed.
Set the source to demo.testfire.net.
Run the module.
Is Altoro Mutual vulnerable to XSS: Yes 

Step 5: Zenmap
Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

Command for Zenmap to run a service scan against the Metasploitable machine: 
# nmap -T4 -A -v 192.168.0.10

Bonus command to output results into a new text file named zenmapscan.txt:
root@kali : ~/Documents # nmap -T4 -A -v 192.168.0.10 > zenmapscan.txt


Zenmap vulnerability script command: # nmap -sV 192.168.0.10


Once you have identified this vulnerability, answer the following questions for your client:

What is the vulnerability: The  Samba 3.x service is the vulnerability here. It is allowing the SMB protocol and ports 139/445 to be open which allows communication with an external file server, and access to the files on the compromised system.

Why is it dangerous: It allows a hacker to gain remote access to the system by using a simple tool called smbclient.


What mitigation strategies can you recommendations for the client to protect their server:
I recommend closing those open ports and upgrading to the latest version of Samba from the vendor’s website.


