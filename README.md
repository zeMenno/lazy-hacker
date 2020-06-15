# Lazy scans

Lazy scans are scans for everybody who want  to do more with less commands. Here is an example of a script that will make your start of pentesting faster, easier and more consistent in use. 

## Scans

### StartScan

StartScan is an easy to use scan that will automate your start of a pentest. StartScan has a couple of features that will help you make your life a bit better. for example:
- StartScan will initiate an NMap scan and a GoBuster scan on the given IP address
- GoBuster will use the given wordlist that you provide with the flag `-w`
- If you can't ping the system (for example if you are trying to enter a windows machine) you can use `-f`
- StartScan will automatically creat a directory for namp and gobuster 
- StartScan will create a init file with the outputs of the scans so you want have to scan again.

I personaly use this script all the time because it saves me a lot of time! 

### Help
```
$ startscan -h

Usage:
  startscan [FLAGS] [OPTIONS]

Flags: 
  -i 		The Ip Address of the target machine
  -d 		The directory where all the output will be
  -w 		Add a custom wordlist for GoBuster
  -h 		Display help information

Options:
  -f 		Force the scans even when the host can not be pinged

This command uses Nmap and Gobuster, make sure you have both of those installed and ready to use :D
```

## Generic

### doc-exec
Doc-Exec is a command that will make a directory and output file and lets you execute any command you want and have the rights for. It will also put the output of that command to the output file created 

### Help
```
$ doc-exec -h

Usage:
  doc-exec [FLAGS]

Flags: 
  -c 		Command to execute
  -d 		The directory where all the output will be
  -h 		Display help information
```
