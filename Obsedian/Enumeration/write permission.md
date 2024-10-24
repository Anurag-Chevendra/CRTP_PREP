[[Enumeration Start]]
After trying from multiple users or using BloodHound we would know that the user ciadmin has Write permissions on the computer object of dcorp-mgmt:
```
Find-InterestingDomainACL | ?{$_.identityreferencename -match 'ciadmin'}
```

