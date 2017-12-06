# INFO

https://www.stigviewer.com/stigs


Siemens s7-1200 vulnerabilities
http://simplyautomationized.blogspot.co.uk/2014/12/raspberry-pi-getting-data-from-s7-1200.html

https://ics-cert.us-cert.gov/advisories/ICSA-14-079-02
https://ics-cert.us-cert.gov/advisories/ICSA-15-239-02
http://www.cvedetails.com/product/23307/Siemens-Simatic-S7-1200-Plc.html?vendor_id=109


Nikto Tutorial

https://hackertarget.com/nikto-tutorial/

nikto -h 192.168.1.104


Vulnerabilities Database


http://www.securityfocus.com/vulnerabilities

https://null-byte.wonderhowto.com/how-to/hack-like-pro-find-almost-every-known-vulnerability-exploit-out-there-0147820/

https://null-byte.wonderhowto.com/how-to/mr-robot-hacks/

NMAP CHEAT SHEETS

Nmap Target Selection

Scan a single IP	nmap 192.168.1.1

Scan a host	nmap www.testhostname.com

Scan a range of IPs	nmap 192.168.1.1-20

Scan a subnet	nmap 192.168.1.0/24

Scan targets from a text file	nmap -iL list-of-ips.txt

These are all default scans, which will scan 1000 TCP ports. Host discovery will take place.

map Port Selection

Scan a single Port	nmap -p 22 192.168.1.1

Scan a range of ports	nmap -p 1-100 192.168.1.1

Scan 100 most common ports (Fast)	nmap -F 192.168.1.1

Scan all 65535 ports	nmap -p- 192.168.1.1

Nmap Port Scan types

Scan using TCP connect	nmap -sT 192.168.1.1

Scan using TCP SYN scan (default)	nmap -sS 192.168.1.1

Scan UDP ports	nmap -sU -p 123,161,162 192.168.1.1

Scan selected ports - ignore discovery	nmap -Pn -F 192.168.1.1

Service and OS Detection

Detect OS and Services	nmap -A 192.168.1.1

Standard service detection	nmap -sV 192.168.1.1

More aggressive Service Detection	nmap -sV --version-intensity 5 192.168.1.1

Lighter banner grabbing detection	nmap -sV --version-intensity 0 192.168.1.1

Nmap Output Formats

Save default output to file	nmap -oN outputfile.txt 192.168.1.1

Save results as XML	nmap -oX outputfile.xml 192.168.1.1

Save results in a format for grep	nmap -oG outputfile.txt 192.168.1.1

Save in all formats	nmap -oA outputfile 192.168.1.1

Digging deeper with NSE Scripts

Scan using default safe scripts	nmap -sV -sC 192.168.1.1

Get help for a script	nmap --script-help=ssl-heartbleed

Scan using a specific NSE script	nmap -sV -p 443 –script=ssl-heartbleed.nse 192.168.1.1

Scan with a set of scripts	nmap -sV --script=smb* 192.168.1.1

The option --script-help=$scriptname will display help for the individual scripts. To get an easy list of the installed scripts try locate nse | grep script.

UDP based DDOS reflection attacks are a common problem that network defenders come up against. This is a handy Nmap command that will scan a target list for systems with open UDP services that allow these attacks to take place

 Scan for UDP DDOS reflectors     nmap –sU –A –PN –n –pU:19,53,123,161 –script=ntp-monlist,dns-recursion,snmp-sysdescr 192.168.1.0/24
 
 HTTP Service Information

Gather page titles from HTTP services	nmap --script=http-title 192.168.1.0/24

Get HTTP headers of web services	nmap --script=http-headers 192.168.1.0/24

Find web apps from known paths	nmap --script=http-enum 192.168.1.0/24

Detect Heartbleed SSL Vulnerability

Heartbleed Testing	nmap -sV -p 443 --script=ssl-heartbleed 192.168.1.0/24

https://iase.disa.mil/stigs/GPO/Pages/index.aspx

https://docs.microsoft.com/en-gb/windows-server/identity/securing-privileged-access/securing-privileged-access


