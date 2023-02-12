# Enumeration Guide 

Information gathering and enumeration are very important steps in many different information security operations including penetration testing. In this guide, we are going to explore many enumeration techniques. We are going to learn: 
DNS Enumeration
FTP Enumeration 
SMB Enumeration
MySQL Enumeration
RPCBind
SNMP Enumeration
HTTP
MSRPC
Let’s get started, 
DNS enumeration 
sudo dnsrecon -d www.hackthissite.org -D /usr/share/wordlists/dnsmap.txt -t std --xml report.xml

dnsenum hackthissite.org

FTP Enumeration
nmap -script ftp-anon -p 21 192.168.43.110

You can also try to use the following Nmap scripts:
ftp-brute.nse
ftp-bounce
Try to connect:
ftp <IP-ADDRESS-HERE>
nc <IP-ADDRESS-HERE> 21
SMB Enumeration
SMB USERS
nmap -script smb-enum-users  -p 445  192.168.43.110

SMB Shares
nmap -script smb-enum-shares  -p 445  192.168.43.110
NBLOOKUP
nmblookup -A <IP ADDRESS HERE>
SMBclient
smbclient -L //<IP ADDRESS HERE>
smbclient //MOUNT/share -I $<IP ADDRESS HERE> -N
RPC client
rpcclient -U "" <IP ADDRESS HERE>
SMB OS Discovery
nmap -p 445 --script smb-os-discovery <IP ADDRESS HERE>
SMB Bruteforce
nmap -sV -p 445 --script smb-brute <IP ADDRESS HERE>
MySQL Enumeration
nmap -p 1433 -script ms-sql-info <IP ADDRESS HERE>
nmap -p 1433 -script ms-sql-config <IP ADDRESS HERE>
nmap -p 1433 -script ms-sql-tables <IP ADDRESS HERE>
RPCBind
rpcinfo –p <IP ADDRESS HERE>
SNMP Enumeration
snmpwalk -c public -v1 <IP ADDRESS HERE>
nmap  -p 161 -script=snmp-info <IP ADDRESS HERE>
HTTP
nmap --script http-enum <IP ADDRESS HERE>
nmap -p80 --script http-apache-server-status <IP ADDRESS HERE>
More Nmap scripts:
http-iis-short-name-brute.nse
Apache users 
Included in Kali Linux
apache-users -h <IP ADDRESS HERE> -l /usr/share/wordlists/metasploit/unix_users.txt -p 80 -s 0 -e 403 -t 10
MSRPC
Microsoft RPC enumeration:
nmap <IP ADDRESS HERE> --script=msrpc-enum

  


