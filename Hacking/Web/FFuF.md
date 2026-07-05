Reconocer Vhost
	ffuf -w /usr/share/wordlists/seclists/Discovery/DNS/subdomains-top1million-5000.txt  -u http://172.17.0.2	-H "Host: FUZZ.172.17.0.2"
![[Pasted image 20260511203826.png]]

Genera muchísimo ruido al ser activa
