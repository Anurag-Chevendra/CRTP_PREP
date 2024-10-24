[[Enumeration Start]]
module 16.
1)users
```
. C:\AD\Tools\PowerView.ps1
```
```
Get-DomainUser -TrustedToAuth
```

look for "TRUSTED_TO_AUTH_FOR_DELEGATION" then check for the query "msds-allowedtodelegate". 

here you read it is:
if i am able to compromise the "user principle name" machine, i can access file system on "msds-allowedtodelegate" as any user including a domain admin.

2)computers

```
Get-DomainComputer -TrustedToAuth
```

to abuse any further, read [[S4U2self]]