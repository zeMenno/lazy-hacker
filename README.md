# Lazy scripts

Lazy scripts are scripts for everyone that want to do more with less commands. Here are some examples of a scripts that will make your pentesting faster, easier and more consistent in use. 

## Scans

### StartScan

StartScan is an easy to use scan that will automate your start of a pentest. StartScan has a couple of features that will help you make your life a bit easier. for example:
- StartScan will initiate an `nmap` scan and a `gobuster` scan on the given IP address
- GoBuster will use the given wordlist that you provide with the flag `-w`
  If you dont set one it will use the default one
- If you can't ping the system (for example if you are trying to enter a windows machine) you can use `-F`
- StartScan will automatically create a directory for `nmap` and `gobuster` 
- StartScan will create a init file with the outputs of the scans so you won't have to scan again.
- Gobuster can now scan recursively (it may take a while but it will give you all the results you wont find on your own) 

I personaly use this script all the time because it saves me a lot of time! 

### Help
```
$ startscan -h

Usage:
  startscan [FLAGS] [OPTIONS]

Flags: 
  -i    The Ip Address of the target machine
  -d    The directory where all the output will be
  -w    Add a custom wordlist for GoBuster
  -h    Display help information
  -t    Amount of threads GoBuster will use
  -r    All the response codes GoBuster will check (',' seperated)
  -l    Amount of levels dee GoBuster will scan
     	(The higher this amount the longer the scan will take)
        Don't use -R if you want fast results 

Options:
  -F    Force the scans even when the host can not be pinged
  -R    Recursively execute GoBuster (may tak a long time)
  -A    Will execute an aggressive nmap scan

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
