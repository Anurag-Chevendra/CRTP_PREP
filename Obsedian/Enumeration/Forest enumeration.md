[[Enumeration Start]]
```
Get-ForestDomain -Verbose
```
to map all trusts of the dollarcorp domain
```
Get-DomainTrust
```
To List only external trusts in a particular forest 
```
Get-ForestDomain | %{Get-DomainTrust -Domain $_.Name} | ?{$_.TrustAttributes -eq "FILTER_SIDS"}
```
To enumerate another forest:
1) it should be bidirectional or
2) trust should be from target to source. 
==eurocorp.local==
```
Get-ForestDomain -Forest eurocorp.local | %{Get-DomainTrust -Domain $_.Name}
```