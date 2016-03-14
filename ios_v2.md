#Environment: STAGE
###Appdelegate.m:
1.	Add Endpoints
2.	Add API key and change “nil” to “options”:
```
[Gimbal setAPIKey:@"## PLACE YOUR API KEY HERE FROM MANAGER ##" options:options];
````

###Info.plist:
1.	Change Bundle Identifier to your apps’ name.

#Environment: PRODUCTION
###Appdelegate.m:
1.	Add API key:
```
[Gimbal setAPIKey:@"## PLACE YOUR API KEY HERE FROM MANAGER ##" options:nil];
```
###Info.plist:
1.	Change Bundle Identifier to your apps’ name.

