# Useful Linux Notes

**Permission Levels**

4 = read (r)
2 = write (w)
1 = execute (x)

7 = 4+2+1
6 = 4+2
5 = 4+1
4 = 4
3 = 2+1
2 = 2
1 = 1

COMMAND:	OWNER: 	GROUP:	WORLD:	PATH
chmod		7	7	7	/path/to/file

-----------------------------------------------------------------------------------------

Nmap -sP 10.0.0.0/24
Or -sL or -sn 
Ping sweep of entire network, returns device details

Nmap -p- hostname
Scans all ports of a given host and returns service details

Nmap -sS -A 10.10.1.1
Or -sV gives banner information
Portscan an IP and return complete service details

NC -lvp 10101
Ncat listens on port 10101

Nc -c 10101 hostname
Connect to host on port 10101

Ngrep google.com
Grep all network traffic to google.com

-----------------------------------------------------------------------------------------
WIRELESS

set wireless nic to monitor mode
1) check mode of nic with iwconfig wlp4s0
2) sudo ifconfig wlp4s0 down
3) sudo iwconfig wlp4s0 mode monitor
4) sudo ifconfig wlp4s0 up
5) check status again with iwconfig wlp4s0

airmon-ng start (wlan1 / wlp4s0)
start monitor process on wifi nic

airodump-ng wlan1mon

sudo iwlist scanning
scan networks to find BSSID and more info

aireplay-ng --deauth 0 -a (BSSID) wlan1mon
Sends deauth signal to all connected devices on a wireless network

iw dev mon0 del

kill monitor interface at the end
-----------------------------------------------------------------------------------------
METASPOIT

msf > use auxiliary/scanner/portscan/tcp 
msf auxiliary(scanner/portscan/tcp) > set RHOSTS 5.35.165.166
RHOSTS => 5.35.165.166
msf auxiliary(scanner/portscan/tcp) > run

Web services
ExploitDB - wiki for exploits
Shodan - port scan service

