[[Enumeration Start]]
1) check if applocker present. 
```
winrs -r:dcorp-<user> cmd
```
```
reg query HKLM\Software\Policies\Microsoft\Windows\SRPV2
```
```
reg query HKLM\Software\Policies\Microsoft\Windows\SRPV2\Script\06dce67b-934c-454f-a263-2515c8796a5d
```
exit winrs
```
Enter-PSSession dcorp-<user>
```

```
$ExecutionContext.SessionState.LanguageMode
```

```
Get-AppLockerPolicy -Effective | select -ExpandProperty RuleCollections
```
disable defender
```
Set-MpPreference -DisableRealtimeMonitoring $true -Verbose
```
