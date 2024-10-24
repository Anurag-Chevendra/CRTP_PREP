[[Enumeration Start]]
```
C:\AD\Tools\InviShell\RunWithRegistryNonAdmin.bat
```
```
. C:\AD\Tools\PowerView.ps1
```
```
Get-DomainComputer -Unconstrained | select -ExpandProperty name
```