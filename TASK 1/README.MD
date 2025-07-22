🔍 Nmap Basic Network Scan Report

🎯 Target: 45.33.32.156

✅ Objective:
To identify open ports and analyze services on a host using Nmap.




📂 Scan Command Used:

nmap -Pn 45.33.32.156 -oN nmap_scan_results.txt



Port	    State	           Service	Notes

22/tcp   	Open	           SSH	Secure shell login, commonly used for remote admin

23/tcp   	Filtered	       Telnet	Insecure remote login protocol (mostly outdated)

25/tcp   	Filtered	       SMTP	Used for email transfer

80/tcp	  Open	           HTTP	Web server; accessible through a browser

135/tcp	  Filtered	       MSRPC	Windows Remote Procedure Call

139/tcp	  Filtered	       NetBIOS-SSN	Windows file/printer sharing

445/tcp 	Filtered	       Microsoft-DS	Used in SMB file sharing (potential vulnerability)

593/tcp	  Filtered         HTTP-RPC-EPMAP	Remote call endpoint mapping (Windows)

1900/tcp	Filtered	       UPNP	Universal Plug and Play (IoT, home devices)

2323/tcp	Filtered	       3d-nfsd	Possibly alternate telnet; uncommon service

3005/tcp	Filtered	       deslogin	Unknown service; likely closed or firewalled

5555/tcp	Filtered	       FreeCiv	Often Android Debug Bridge or game server port

8600/tcp	Filtered	       Asterix	DNS service (Google Cloud)

9929/tcp	Open	           nping-echo	Used by Nmap's nping tool; usually test/debug only

31337/tcp	Open	           Elite	Backdoor/remote shell (common in CTFs or malware)

52869/tcp	Filtered	       Unknown	Unrecognized; blocked or not responding



