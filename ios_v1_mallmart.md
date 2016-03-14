#Environment: STAGE
###Usercontext.plist:

SERVER_URL_OVERRIDE|string|https://ios-api-stage.gimbal.com/service/rest/v4/|-|
--- |---|---|---
API_KEY_OVERRIDE|string|API key|-|
SHOW_DEBUG_PANELS|boolean|YES|Optional(Recommended). Allows access to debug views|
CUSTOM_OPT_IN_FLOW|boolean|NO|Optional. By default it’s not included|
PLACE_STATE_AVAILABLE_ON_SERVER|boolean|YES|-|

##Mallmart-Info.plist:
1.	Change Bundle Identifier to your apps’ name.

#Environment: PRODUCTION
API_KEY_OVERRIDE|string|API key|-|
--- |---|---|---
SHOW_DEBUG_PANELS|boolean|YES|Optional(Recommended). Allows access to debug views|
CUSTOM_OPT_IN_FLOW|boolean|NO|Optional. By default it’s not included|
PLACE_STATE_AVAILABLE_ON_SERVER|boolean|YES|-|

##Mallmart-Info.plist:
1.	Change Bundle Identifier to your apps’ name.
