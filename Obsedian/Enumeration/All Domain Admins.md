[[Enumeration Start]]
```
. C:\AD\Tools\PowerView.ps1
```
To see details of the Domain Admins group:
```
Get-DomainGroup -Identity "Domain Admins"
```
To enumerate members of the Domain Admins group:
```
Get-DomainGroupMember -Identity "Domain Admins"
```
