# NMAP Scans

> More effective approach (Takes less time)

> First of all, scan all the port with -p- switch to check the open ports. (Step 1- Find open ports)

> Now run service detection and other tests against **ports** identified in last step. (Stage 2: Do deep scan on only open ports)



1. Detect OS and Services   

` nmap -A 192.168.1.1 `
	
2. Standard service detection  

` nmap -sV 192.168.1.1 `

3. Save default output to file  

`nmap -oN outputfile.txt 192.168.1.1`

4. Save results as XML  

`nmap -oX outputfile.xml 192.168.1.1`

5. Save results in a format for grep 

`nmap -oG outputfile.txt 192.168.1.1`

6. Save in all formats 

`nmap -oA outputfile 192.168.1.1`

7. Scan using a specific NSE script	

`nmap -sV -p 443 –script=ssl-heartbleed.nse 192.168.1.1`

8. Scan with a set of scripts	

`nmap -sV --script=smb* 192.168.1.1`
