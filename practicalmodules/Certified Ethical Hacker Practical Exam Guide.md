Tools were used in the exam.
1) Nmap
2) Snow — Stegnography
3) Open Stego
3) Wpscan
4) WireShark
5) SqlMap
6) OWASP ZAP
7) Hashcat
8) John
9) Hydra
10) Veracrypt
11) Crypttool
12) Hash Calculator
13) MD5 Calculator
14) PhoneSploit
15) MetaSploit
16) BCTextEncoder


Topics Covered
1) Scanning and Enumeration
2) Web-Application Pentesting
3) Cryptography
4) Stegnography
5) Dos & DDOS (Packet Sniffing)
6) Android Exploit


Sample Questions
1) Find the IP address of the machine which is running the RDP?
2) Find the OS name of the machine which is running MySQL database?
3) Find the HTTP method that poses a high risk to the application example.com?
4) Find the Phone number the employee?
5) Find the file name which is tampered by comparing the hashes which is given in the /hashes folder?
6) Decrypt the volume file using veracrypt?
7) Connect to the Server remotely using the credentials give by RDP?
8) Decode the file which is encoded in DES(ECB) format?
9) Find the password of the wordpress user “Raj”?
10) Find the attacker IP address who has launched the DOS attack?
11) Find the number of machines that were used to iniate the DDOS attack?
12) Find the username/password from the pcap file, which is in plain text?
13) Extract the information from the SDcard of the Android User?


Windows
There were more windows based questions so you have to practice on windows GUI tools like mentioned below.
1) “Open Stego” for Stegnography
https://www.openstego.com/

2) “WireShark” for Pcap analysis
https://www.wireshark.org/download.html

3) “ZAP” for SQLInjecion exploit
https://www.zaproxy.org/download/

4) “Veracrypt” for Disk Decryption
https://www.veracrypt.fr/en/Downloads.html

5) “Hash calculator” to find the hash of the file
https://www.slavasoft.com/hashcalc/

6) “MD5 Calculator” to compare the hashes
http://www.md5calculator.com/

7) “Cryptool” and “BCTextEncoder” to Crack the encoded files
https://www.jetico.com/free-security-tools/encrypt-text-bctextencoder

Windows based Commands which will help you to find the answers.
1) net user — For Domain Users Enumeration
2) snow.exe -C -p “password” stegfile.txt
3) type C:\path.txt — It displays the content of the path.txt file.
4) dir
5) cd
6) hostname
7) whoami
8) PWd

Before giving the exam its very important to practice on these tools because the whole exam is based on the tools you should definitely know about these tools.


Check out the links
https://www.youtube.com/watch?v=ycZFk-GT5-I
https://github.com/cmuppin/CEH

TryHackMe Rooms
Try to solve these machines, after completing these machines you will become familiar with windows and some other tools, these rooms will also helps you in the real pentesting world.

https://tryhackme.com/room/ice
https://tryhackme.com/room/windowsfundamentals1xbx
https://tryhackme.com/room/cryptographyfordummies
https://tryhackme.com/room/lianyu
https://tryhackme.com/room/startup

Linux
Linux based tools
1) Nmap
2) wpscan
3) sqlmap
4) hashcat
5) john
6) Hydra
7) PhoneSploit
8) Metasploit

Commands were used during the exam
1) Nmap
nmap -sn 170.16.0.1/24 -oN nmap.txt
nmap -O 170.16.0.1/24 -oN namp-OS.txt
namp -sC -sV -sS 170.16.0.20 -oN namp-all.txt

2) wpscan
wpscan -u james -P /password.txt — url http://172.16.0.27:8080/CEH/

3) sqlmap
I didn’t used “sqlmap” for any sqlinjection related question, incase if you get any questions related to sqlinjection use github repo you will find some usefull commands.
https://github.com/cmuppin/CEH/blob/main/SQL%20Injection

4) “hashcat” and “john”
If you get questions related to Hash caracking use this github repo you will find some usefull commands.
https://github.com/cmuppin/CEH/blob/main/Cryptography

6) Hydra
hydra -L /user.txt -P /password.txt ftp://172.0.16.21

7) Phonesploit
To exploit the Android device and get the reverse shell, these commands will help you and the phonesploit will be installed in the root folder, if you don't find the phonesploit use the command like “find phonesploit”.
https://github.com/cmuppin/CEH/blob/main/Android

8) Metasploit
If you get any questions related to netbios, SMB use metasploit.

Check out the links
https://www.youtube.com/watch?v=ycZFk-GT5-I
https://github.com/cmuppin/CEH

TryHackMe Rooms
https://tryhackme.com/room/linuxfundamentalspart1
https://tryhackme.com/room/crackthehash
https://tryhackme.com/room/basicpentestingjt
https://tryhackme.com/room/sqlmap
https://tryhackme.com/room/dvwa

The Username and Password file will be present in the parrot machine it will help you to crack the ftp and wordpress related questions.

Don’t be nervous, you are going to pass the exam with no doubt. Patience is really needed for the exam because the parrot machine is outdated and its very slow.

Tips
1) First finish linux based questions like nmap etc and save those in the desktop folder, believe me you will look into the nmap scans over and over again.
2) Watch the ilab videos from youtube and reffer CEH practical Lab manual.
3) Everything will be asked from the ilab videos nothing will be out of sylabus.
4) Be Cool.

Some resource links will help you in the exam.
https://github.com/cmuppin/CEH
https://chirag-singla.notion.site/CEH-Practical-Preparation-7f2b77651cd144e8872f2f5a30155052
https://github.com/Samsar4/Ethical-Hacking-Labs
https://github.com/Rezkmike/CEH_Practical_Preparation
https://www.youtube.com/watch?v=ycZFk-GT5-I (i-lab videos)


