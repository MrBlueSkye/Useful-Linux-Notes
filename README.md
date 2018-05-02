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
**WIRELESS**

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
**METASPOIT**

msf > use auxiliary/scanner/portscan/tcp 
msf auxiliary(scanner/portscan/tcp) > set RHOSTS 5.35.165.166
RHOSTS => 5.35.165.166
msf auxiliary(scanner/portscan/tcp) > run

**Web services**
ExploitDB - wiki for exploits
Shodan - port scan service








...

...

...

#the below is not my own OC






**Handy Linux Commands**

cd	e.g. cd bin OR cd .. OR cd / OR cd
Change Directory

pwd
show the path of current directory you’re looking in

ls	e.g. ls –l OR ls -a
Display the contents of the directory you are working in

ls | more
Display the contents of the directory you are working in then pipe it to the more command. Useful when there is a long list of files

set
show all environment variables

echo <variablename> e.g. echo $OMNIHOME
show an individual environment variable

find <path> -name <filename wildcard> e.g. find / -name bi.*
find a file in the directory tree – the above example finds bi*.* from the root
http://www.linux-mag.com/2002-09/power_01.html

pgrep –fl <process-name-text>   e.g. pgrep –fl nco
find running processes that match <process-name-text>

ps –A
List all running processes

touch <filename>
Creates a new file in the current directory

cat >> <filename>
Append text to the specified file. End with ctrl-d

df
Show a list of disk usage for each partition

rpm –qa | grep <package name>
List all installed packages then grep the output for the specified name

du –a | sort –rn
Show a list of files & directories sorted by filesize (largest first). You may want to cd to the root directory first.

Init -<runlevel>
Init –6 is common, but user-defined
Init –4 should start up all processes including graphical interface
  
  
  
  **KEYBOARD SHORTCUTS & SHELL PROMPTS
  
  •	/ - root directory 
•	./ - current directory 
•	./command_name - run a command in the current directory when the current directory is not on the path 
•	../ - parent directory 
•	~ - home directory 
•	$ - typical prompt when logged in as ordinary user 
•	# - typical prompt when logged in as root or superuser 
•	! - repeat specified command 
•	!! - repeat previous command 
•	^^ - repeat previous command with substitution 
•	& - run a program in background mode 
•	[Tab][Tab] - prints a list of all available commands. This is just an example of autocomplete with no restriction on the first letter. 
•	x[Tab][Tab] - prints a list of all available completions for a command, where the beginning is ``x'' 
•	[Alt][Ctrl][F1] - switch to the first virtual text console 
•	[Alt][Ctrl][Fn] - switch to the nth virtual text console. Typically, there are six on a Linux PC system. 
•	[Alt][Ctrl][F7] - switch to the first GUI console, if there is one running. If the graphical console freezes, one can switch to a nongraphical console, kill the process that is giving problems, and switch back to the graphical console using this shortcut. 
•	[ArrowUp] - scroll through the command history (in bash) 
•	[Shift][PageUp] - scroll terminal output up. This also works at the login prompt, so you can scroll through your boot messages. 
•	[Shift][PageDown] - scroll terminal output down 
•	[Ctrl][Alt][+] - switch to next X server resolution (if the server is set up for more than one resolution) 
•	[Ctrl][Alt][-] - change to previous X server resolution 
•	[Ctrl][Alt][BkSpc] - kill the current X server. Used when normal exit is not possible. 
•	[Ctrl][Alt][Del] - shut down the system and reboot 
•	[Ctrl]c - kill the current process 
•	[Ctrl]d - logout from the current terminal 
•	[Ctrl]s - stop transfer to current terminal 
•	[Ctrl]q - resume transfer to current terminal. This should be tried if the terminal stops responding. 
•	[Ctrl]z - send current process to the background 
•	reset - restore a terminal to its default settings 
•	[Leftmousebutton] - Hold down left mouse button and drag to highlight text. Releasing the button copies the region to the text buffer under X and (if gpm is installed) in console mode. 
•	[Middlemousebutton] - Copies text from the text buffer and inserts it at the cursor location. With a two-button mouse, click on both buttons simultaneously. It is necessary for three-button emulation to be enabled, either under gpm or in XF86Config. 

  
  


