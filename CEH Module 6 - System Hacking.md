
#K8). Phases of Hacking or how to successfully hack into system
		- **Reconnaissance**            
			Active = Acquiring Info with interacting with Target Directly.
			Passive = Gain Info by Acquiring the target Indirectly. (Via Calls, Emails, help Desk or Technical Department)
		- **Scanning** nmap , hping 3
			Scan IP's for Open Ports and Possible Vulnerabilities like Older version of OS, Running Services .
		- **Gaining Access**
			Attacker Gain Access by found Vulnerabilities in Scanning Phase (By Password Cracking, Insecure Authentication, Buffer Overflow, Etc)
		- **Maintaining Access**
			Maintain Access by Creating backdoor, installing Rootkit, Trojan, etc)
		- **Clearing Traces/Logs**
			Clear Footprints like connection established, Activities performed) Clear Date defining Hackers Identity



# Methods for System Hacking
	- Cracking Password :- 
	- Exploit Services, Application Installed, OS
	- Malicious Applications
-------------------------------------------------------------------------------------------------
# Password Cracking - Password Cracking is the method for extracting the password to gain authorized access to the target system like a legitimate user.
	Three type of authentication factors:
	- Authentication using Username and password
	- Authentication using Biometric (Fingerprint, Retina Scan)
	- Only Authorized Devices are allowed to connect. This can be done by filtering MAC Address
------------------------------------------------
# Characteristics of Secure password:
	- In Case sensitive letters
	- Special characters
	- Numbers
	- Lengthy password/Pin (more than 8 character)
	- Pass-Phrases
------------------------------------------------
# Types of Password Attacks
	# Non-Electronic Attacks - Don't require any type of technical understanding and knowledge.
		Example:
		- Shoulder-Surfing
		- Dumpster-Diving
		- Eaves-Dropping
		- Vishing   --->

	# Active Online Attack - Directly interact with the target for cracking password.
		- Dictionary/Wordlist Attack - In Dictionary Attack, Attacker Use Preconfigured wordlist (For Username or Password) to gain access into victims account.
		- Brute Force Attack - In Brute Force Attack, Attacker Try every possible combination of Characters to gain access to victims account.
		- Hash Injection - Hash Injection is performed after gaining access to System. In Hash Injection, Attacker try to crack Hashes available in SAM (Security Account Manager)
		Location : C:\windows\system32\config\SAM) in Windows and Shadow file in Linux OS.

	# Passive Online Attacks - Passive online attacks are performed without interfering with the target.
		- Wire Sniffing - In Wire Sniffing, Attacker Sniff network Traffic and try to extract sensitive Information like Telnet, FTP, SMTP credentials.
		- Man-in-the-Middle (MITM) Attack - The attacker involves himself into the communication, insert himself in.
			MITM Attacks:
				- xerosploit --> Ettercap --> Bettercap
				- Browser Exploitation Framework (BeEF-XSS) - older version on browser  ---> XSS Protection

	# Default Password - Default Password are Set by Developer or Manufacturer. Attacker Try those password to gain Access.
			- https://cirt.net/
			- https://default-password.info/
			- http://www.passwordsdatabase.com/

	# Password Guessing - The attacker uses the information extracted by initial phases and guess the password.

	# USB Drive - Attacker plug in an USB Drive that contain a password hacking tool. Windows Autorun feature allows running the application automatically, if enabled.

	# Password Cracking Mitigation
		- Change default password.
		- Do not store/save passwords in applications. 																						                        0ba232f0c8cdb6f0ddbb0d48adb666dc
		- Do not use guessable passwords.																							
		- Store passwords in form of salted hash.
		- Change passwords on weekly/Monthly basis.
		- Different password for each service.        https://md5decrypt.net/en/
		- Configure policies for incorrect password attempts.
-------------------------------------------------------------------------------------------------
# Escalating Privileges - Privilege Escalation is the process of gaining Privileges of Other user.			   -->    								
	- Horizontal Privileges Escalation - The attacker attempts to gain access to user with same set of privileges.
	- Vertical Privileges Escalation - The attacker try to gain access to user with higher set of Privileges.
-------------------------------------------------------------------------------------------------
# Keyloggers
	- Keylogger are malicious software that capture your keystrokes.

# Anti-Keyloggers
	- Anti-Keylogger is an application which ensures protection against keylogging by providing SSl protection, keylogging protection, clipboard logging protection and screen logging protection.

# Key-logging Countermeasures
	- Don't click on doubtful URLs
	- On-Screen keyboard for secrets
	- Physical monitoring
	- Host-based IDS
	- File scanning prior to installation

# Adware - Adware is a malicious software that show Advertisements to victim by inspecting his actions and interests.

# Spyware - Spyware are malicious software that capture your keystrokes, screen, camera, Mic, Location, etc.
	Features:
	- Tracking users (i.e. keylogging)
	- Voice recording
	- Video recording

-------------------------------------------------------------------------------------------------
# File Systems
	- New Technology File System (NTFS) Data Stream, is a Windows file system by Microsoft. NTFS is the default file system for Windows 10,- 7,- Vista,- XP,- 2000,- NT.
	- File Allocation Table (FAT) file system, is a simple file system originally designed for small disks and simple folder structures.
	- Extended File System (Ext) file System, is the first file system created specifically for the Linux kernel
-------------------------------------------------------------------------------------------------
# Steganography - Steganography is a technique for hiding sensitive information in an ordinary message to ensure confidentiality. Steganography uses encryption to maintain the confidentiality. It hides the encrypted data to avoid detection. An attacker may use this to technique to transfer data without being detected.
	Examples of Steganography:
		- Image/Pixel Steganography - In Image Steganography, hidden information can be kept in different formats of Image such as PNG, JPG, BMP, etc.
		- Video Steganography - Hiding information in Video files or format.
		- Audio Steganography - Hiding information in Audio files or format.
-------------------------------------------------------------------------------------------------
# Covering tracks - After gaining access, escalating privileges, executing applications, the next step is to wipe digital footprint that perdict attacker identity. In this phase, attacker removes all the event logs, error messages and other evidence to prevent its attack from being discovered easily.
	Common techniques:
	- Disable auditing
			Preventing another security mechanism to indicate an alert of any sort of intrusion, and leaving to track leaving to track on the machine. The best practice for leaving no track and prevent detection is by disabling the auditing as you logged in on the system. It will not only prevent to log events, but also resist in the detection. Auditing in a system is enabled to detect and track events.
	- Clearing logs - By clearing logs, all events logged during the compromise will be erased.

# Disable auditing policies :-
- List auditing categories in windows:
	**-> C:\Windows\system32>auditpol /list /category	"**

- Check all category audit policies:
	**-> C:\Windows\system32>auditpol /get /category:*		"**

- Command to enable auditing for System and Account logon: -
	**-> C:\Windows\system32>auditpol /set /category:"System","Account logon" /success:enable /failure:enable		"**

- Command to enable auditing for all categories:
	**-> C:\Windwos\system32>auditpol /set /category:* /success:enable		"**

- Clear Audit Policies
	**-> C:\Windows\system32>auditpol /clear	/y "**												

# Clearing logs -
	Folder of log files:
	Windows 2000/Server2003/Windows XP: %SystemRoot%\System32\Config
	Server 2008/Vista and up: %SystemRoot%\system32\winevt\logs
	Linux, OpenBSD: /var/log/








Auditpol Command Examples
Lists all the settings

Auditpol /get /category:*
Lists only the Account Management category settings.

Auditpol /get /category:"Account Management"
Lists only the User Account Management subcategory setting.

Auditpol /get /subcategory:"User Account Management"
Set the  Account Management category setting as success.

Auditpol /set /category:"Account Management" /success:enable
Set the  Account Management category setting as failure.

Auditpol /set /category:"Account Management" /failure:enable
Disable/Remove success setting of the  Account Management category.

Auditpol /set /category:"Account Management" /success:disable
Disable/Remove failure setting of the  Account Management category.

Auditpol /set /category:"Account Management" /failure:disable
Set only the subcategory setting User Account Management as success.

Auditpol /set /subcategory:"User Account Management" /success:enable
Set only the subcategory setting User Account Management as failure.

Auditpol /set /subcategory:"User Account Management" /failure:enable
Lists Detailed Tracking category settings only for the user Administrator.

Auditpol /get /user:Administrator /category:"Detailed Tracking"
Set Detailed Tracking category setting as success only for the user Administrator.

Auditpol /set /user:Administrator /category:"Detailed Tracking" /success:enable
