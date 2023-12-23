# BRUTEFORCE

*******************************************************************************
# PYTHON SERVER
python3 : python3 -m http.server {port} eg: python3 -m http.server 80
python2 : python -m SimpleHTTPServer {port} eg : python -m SimpleHTTPServer 80

********************************************************************************
# GOBUSTER SCAN SUBDOMAIN
goobuster dir -u {url} -w {wordlist path}
eg :gobuster dir -u google.com -w common.txt

********************************************************************************
# WIFI HACKING

start monitor mode
-------------------
fmt : airmon-ng start [interface]
eg  : airmon-ng start wlan0

monitor
-------
fmt : airodump-ng [interface]
eg  : airodump-ng wlan0

capture packet
---------------
fmt : airodump-ng -d [bssid of router] -w [file name to be saved] -c [channel] [interface]
eg  : airodump-ng -d 00:AA:11:BB:22:CC -w myWifi -c 11 wlan0

deauthentication attack
-----------------------
fmt : aireplay-ng -O [number of deauthentication packets] -a [bssid of router] -c [bssid of device] [interface]
eg  : aireplay-ng -O 10 -a 00:AA:11:BB:22:CC -c AA:BB:CC:DD:EE:FF wlan0

rockyou.txt wordlist location
------------------------------
/usr/share/wordlists/rockyou.txt

crack password using wordlist
------------------------------

aircrack-ng -w [wordlist location] [captured file ".cap"]

****************************************************************************************
# SCANNING (NMAP)
------------------
subnet scan
------------
fmt : nmap -sn [ip range]
eg  : nmap 192.168.1.0/24

tcp scan (with service version)
-------------------------------
fmt : nmap -sT -sV [ip address]
eg  : nmap -sT -sV 192.168.1.18

syn scan (only sending syn packets) [ROOT PRIVILIEGE]
------------------------------------
fmt : nmap -sS [ipaddress]
eg  : nmap -sS 192.168.1.18

udp scan [ROOT PRIVILIEGE]
---------------------------
fmt : nmap -sU [ipaddress]
eg  : nmap -sU 192.168.1.18


