# Exploring Services

## FTP 21

1. Do telnet / nc to identify the FTP Service Version and banner grabbing.

2. See if anonymous access available to FTP Server (user Filezilla Client -- can be installed with sudo apt install)

3. Do searchsploit query to identify possible exploits.  

4. Enumerate FTP users and try bruteforcing the way in.

5. NSE Script available : ftp-brute, FTP Annon, ftp-proftpd-backdoor, ftp-vsftpd-backdoor, ftp-vuln-cve2010-4221

6. THC Hydra : For brute forcing the user credentials

## SSH 22

1. To telnet to identify the SSH Service Version and banner grabbing

2. Do searchsploit query to identify possible exploits. 

3. Run NSE Scripts with ssh-* switch.

4. Hydra, medusa: For bruteforcing 

## SMTP 25

1. To telnet to identify the SMTP Service Version and banner grabbing

2. Do searchsploit query to identify possible exploits.

3. Use NSE scripts. Try enumerating usernames using smtp-enum-users.

## DNS 53

1. Do searchsploit query to identify possible exploits (Not many of exploits in DNS servers but something happens in future).

2. NSE Scripts dns-zone-transfer, dns-brute; dns-service-discovery

3. Try querying DNS server for DNS records.

4. Brute force for subdomains.


## HTTP / HTTPS 80/443/8080   -----Its long one.

1. Run Nikto to find basic information.

2. Bruteforce the directories or files using dirbuster.

3. Finding Virtual Hosts 

` nmap -p 80 --script hostmap-bfk.nse nmap.org `

`nmap --script http-enum 192.168.10.55`

`nmap --script -http-enum --script-args http-enum.basepath='pub/' 192.168.10.55`

4. Try to identify Web server and CMS installed. (Some exploits can be used)

5. Try to use default creds for any CMS found. Try bruteforcing using Cewl word lists also.


> There is detailed list available at:

> http://www.0daysecurity.com/penetration-testing/enumeration.html 





