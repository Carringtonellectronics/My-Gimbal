#Environment: STAGE
SDK MUST be downloaded from Stage environment (the environment it points to is hardcoded in the frameworks and can't be changed).

###Appdelegate.m:
1.	Add data:
```
[FYXsetAppId:@"057dbcbdc88adcc60ff62737b37b868dbc6d24c07de7d3157cb357f783a53460"
appSecret:@"f2934a25672b4660561ab7a6ee1200f08183746359b0f5fdd60de59e3dfd498a"
callbackUrl:@"comunosquarearantxatest://authcode"];
[FYXLogging setLogLevel:FYX_LOG_LEVEL_INFO];
```

###FindMyStuff-Info.plist:
1.	Change Bundle Identifier to your apps’ name.

#Environment: PRODUCTION
SDK MUST be downloaded from Production environment (the environment it points to is hardcoded in the frameworks and can't be changed).

###Appdelegate.m:
1.	Add data
```
[FYXsetAppId:@"057dbcbdc88adcc60ff62737b37b868dbc6d24c07de7d3157cb357f783a53460"
appSecret:@"f2934a25672b4660561ab7a6ee1200f08183746359b0f5fdd60de59e3dfd498a"
callbackUrl:@"comunosquarearantxatest://authcode"];
[FYXLogging setLogLevel:FYX_LOG_LEVEL_INFO];
```

~~###FindMyStuff-Info.plist:~~

~~1.	Change Bundle Identifier to your apps’ name.~~


