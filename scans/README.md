## Lazy scans

# StartScan

StartScan is an easy to use scan that will automate your start of a pentest. StartScan has a couple of features that will helkp you make your life a bit better. for example:
- StartScan will initiate an NMap scan and a GoBuster scan on the given IP address
- GoBuster will use the given wordlist that you provide with the flag `-w`
- If you can't ping the system (for example if you are trying to enter a windows machine) you can use `-f`
- StartScan will automatically creat a directory for namp and gobuster 
- StartScan will create a init file with the outputs of the scans so you want have to scan again.

I personaly use this script all the time because it saves me a lot of time! 