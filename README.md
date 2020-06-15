# Lazy scans

Lazy scans are scans for everybody who want  to do more with less commands. Here is an example of a script that will make your start of pentesting faster, easier and more consistent in use. 

### StartScan

StartScan is an easy to use scan that will automate your start of a pentest. StartScan has a couple of features that will helkp you make your life a bit better. for example:
- StartScan will initiate an NMap scan and a GoBuster scan on the given IP address
- GoBuster will use the given wordlist that you provide with the flag `-w`
- If you can't ping the system (for example if you are trying to enter a windows machine) you can use `-f`
- StartScan will automatically creat a directory for namp and gobuster 
- StartScan will create a init file with the outputs of the scans so you want have to scan again.

I personaly use this script all the time because it saves me a lot of time! 

## Help
```
$ startscan -h

Usage:
  startscan [FLAGS] [OPTIONS]

Flags: 
  -i 		The Ip Address of the target machine
  -d 		The directory where all the output will be
  -w 		Add a custom wordlist for GoBuster
  -h    This will display the help information

Options:
  -f 		Force the scans even when the host can not be pinged

This command uses Nmap and Gobuster, make sure you have both of those installed and ready to use :D
```
