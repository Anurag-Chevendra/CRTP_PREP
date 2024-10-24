[[Enumeration Start]]

```
. C:\AD\Tools\PowerView.ps1
```
All OUs
```
Get-DomainOU
```
```
Get-DomainOU | select -ExpandProperty name
```
All computers in OUs
```
(Get-DomainOU -Identity StudentMachines).distinguishedname | %{Get-DomainComputer -SearchBase $_} | select name
```
All GPOs
```
Get-DomainGPO -Identity (Get-DomainOU -Identity StudentMachines).gplink.substring(11,(Get-DomainOU -Identity StudentMachines).gplink.length-72)
```

