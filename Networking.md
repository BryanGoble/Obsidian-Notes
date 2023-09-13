
---
share: true  
---
- Network - Two or more computer systems linked by a transmission medium to exchange data

# OSI Model
- Conceptual Framework
- 7 Layers (Typically referred to from 7 to 1)
	1. Physical (Cables) - Bits
		- Physical requirements such as cabling, wifi signals, power (voltages)
	2. Data Link (MAC) - Frames
		- Similar to Layer 3, but facilitates Node-to-Node data transfer between two directly connected nodes
		- Handles error correction from physical layer
		- Also hosts two sub-layers MAC/LLC
		- Most switches operate at Layer 2 but can operate at Layer 3
	3. Network (TCP/IP) - Packets
		- Responsible for packet forwarding
		- Finds best possible path for data to reach destination called routing
	4. Transport (Ports, TCP/UDP) - Segments
		- End-to-End communications between end systems and hosts
		- Determines what data to send and where to go
		- Assigns port numbers to data (TCP/UDP)
	5. Session 
		- Setup, Coordination, and Termination of communications between two devices
	6. Presentation (Encryption)
		- Transforms data between format for application and format needed for the network
		- Encryption/Decryption
		- Handles Compressing data before sending to layer 5
	7. Application
		- Displays incoming data to end user
		- Provides interface for applications to exchange data between various protocols (HTTP, FTP, SSH, DNS)
- Pneumonic - All People Seem To Need Data Processing

# Ports
- Necessary for making multiple network requests or having multiple services available
- 1,024 well-known ports ranging from 0-1,023
- Registered ports range from 1,024-49,151
- Dynamic use by applications range from 49,152-65,535
- Common Ports:
	- 20/21 - FTP
	- 22 - SSH/SFTP (SSH FTP)
	- 23 - TELNET
	- 25 - SMTP
	- 53 - DNS
	- 67/68 - DHCP
	- 69 - TFTP
	- 80 - HTTP
	- 110 - POP
	- 123 - NTP
	- 143 - IMAP
	- 161 - SNMP
	- 389 - LDAP
	- 443 - HTTPS
	- 445 - SMB
	- 636 - LDAPS
	- 1720 - H.323
	- 3389 - RDP
	- 5060/5061 - SIP