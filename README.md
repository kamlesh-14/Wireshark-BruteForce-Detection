# Brute Force Attack Detection Using Wireshark

## Project Objective
Detect FTP brute-force attacks by analyzing live network traffic using Wireshark.

## Tools Used
- Wireshark
- Kali Linux (Attacker)
- Metasploitable 2 (Victim)

## Steps Performed
1. Set up Kali Linux and Metasploitable 2 in VirtualBox.
2. Configured both machines on the same NAT network.
3. Used Hydra tool from Kali to perform brute-force attack on FTP service.
4. Captured traffic on Wireshark.
5. Applied filter: `ftp.port == 21`

## Observations
1. Observed multiple `530 User cannot log in` errors indicating brute-force attempts.
2. Multiple TCP SYN-ACK packets were exchanged rapidly.
3. This repetitive failure pattern indicates a brute-force attack.

## Conclusion
Using Wireshark, it's possible to detect FTP brute-force attacks by filtering specific ports and analyzing the error responses (530 errors). 
This method can help SOC analysts spot suspicious behavior early.
