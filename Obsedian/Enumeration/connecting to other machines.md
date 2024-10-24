[[to check if current user has local administrator access]]
[[Lateral Movement]]

```
cd C:\AD\Tools
```
here it is ==adminsrv==, but you can connect to any. over which you have access rights
```
winrs -r:dcorp-adminsrv cmd
```
or 
```
Enter-PSSession dcorp-adminsrv
```

[[Jenkins]]

