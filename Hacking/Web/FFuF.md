Reconocer Vhost
	ffuf -w /usr/share/wordlists/seclists/Discovery/DNS/subdomains-top1million 5000.txt  -u http://pterodactyl.htb -H "Host: FUZZ.pterodactyl.htb"
![[Pasted image 20260511203826.png]]
