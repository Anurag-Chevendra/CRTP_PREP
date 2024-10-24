[[Enumeration Start]]
```
Invoke-SessionHunter -NoPortScan -RawResults | select Hostname,UserSession,Access
```
OR
To make the above more opsec friendly
```
cat C:\AD\Tools\servers.txt
```
```
Invoke-SessionHunter -NoPortScan -RawResults -Targets C:\AD\Tools\servers.txt | select Hostname,UserSession,Access
```
