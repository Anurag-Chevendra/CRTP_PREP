[[Enumeration Start]]

```
. C:\AD\Tools\PowerView.ps1
```
To enumerate members of the Enterprise Admins group
```
Get-DomainGroupMember -Identity "Enterprise Admins"
```
```
Get-DomainGroupMember -Identity "Enterprise Admins" -Domain moneycorp.local
```
