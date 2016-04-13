//ANDROID
```
Map<String, String> options = new HashMap<String, String>();
        options.put("Context_Base_Url", "https://android-api-stage.gimbal.com/service/");
        options.put("Proximity_Base_Url", "https://proximity-stage.gimbal.com/");
        options.put("Beacon_Resolve_Base_Url", "https://resolve-stage.gimbal.com/");
        options.put("Place_Bubble_Base_Url", "https://placebubble-stage.gimbal.com/service/");
        options.put("Sighting_Base_Url", "https://sightings-stage.gimbal.com/");
        options.put("Registration_Base_Url", "https://registration-stage.gimbal.com/service/");
        options.put("Communicate_Search_Base_Url", "https://communicate-stage.gimbal.com/service/");
	options.put("Sdk_Configuration_Base_Url", "https://sdk-configuration-stage.gimbal.com/service/");
	options.put("Analytics_Base_Url", "https://analytics-server-stage.gimbal.com/service/");  
	options.put("Experience_Base_Url", "https://cep-stage.gimbal.com/autoJoin/");
Gimbal.setApiKeyWithOptions(this.getApplication(), "YOUR API KEY", options);
```

//IOS
```
NSDictionary *options = @{ @"GIMBAL_SERVER_BASE_URL":
                                   @"https://ios-api-stage.gimbal.com/service/",
                               @"PROXIMITY_SERVER_BASE_URL":
                                   @"https://proximity-stage.gimbal.com/",
                               @"BEACON_RESOLVE_SERVER_BASE_URL":
                                   @"https://resolve-stage.gimbal.com/",
                               @"PLACE_BUBBLE_SERVER_BASE_URL":
                                   @"https://placebubble-stage.gimbal.com/service/",
                               @"SIGHTINGS_SERVER_BASE_URL":
                                   @"https://sightings-stage.gimbal.com/",
                               @"REGISTRATION_SERVER_BASE_URL":
                                   @"https://registration-stage.gimbal.com/service/",
                               @"COMMUNICATION_SEARCH_SERVER_BASE_URL":
                                   @"https://communicate-stage.gimbal.com/service/",
                               @"SDK_CONFIGURATION_SERVER_BASE_URL":
                                   @"https://sdk-configuration-stage.gimbal.com/service/",
                               @"ANALYTICS_SERVER_BASE_URL":
                                   @"https://analytics-server-stage.gimbal.com/service/",
                               @"EXPERIENCE_SERVER_BASE_URL":
                                   @"https://cep-stage.gimbal.com/autoJoin/"};
                               [Gimbal setAPIKey:@"YOUR API KEY" options:options];
```

//IOS SWIFT
```
var options = [
            "GIMBAL_SERVER_BASE_URL" : "https://ios-api-stage.gimbal.com/service/",
            "PROXIMITY_SERVER_BASE_URL" : "https://proximity-stage.gimbal.com/",
            "BEACON_RESOLVE_SERVER_BASE_URL" : "https://resolve-stage.gimbal.com/",
            "PLACE_BUBBLE_SERVER_BASE_URL" : "https://placebubble-stage.gimbal.com/service/",
            "SIGHTINGS_SERVER_BASE_URL" : "https://sightings-stage.gimbal.com/",
            "REGISTRATION_SERVER_BASE_URL"  :  "https://registration-stage.gimbal.com/service/",
            "COMMUNICATION_SEARCH_SERVER_BASE_URL":"https://communicate-stage.gimbal.com/service/",
            "SDK_CONFIGURATION_SERVER_BASE_URL" :"https://sdk-configuration-stage.gimbal.com/service/",
            "ANALYTICS_SERVER_BASE_URL":"https://analytics-server-stage.gimbal.com/service/",
            "EXPERIENCE_BASE_URL" :"https://cep.gimbal.com/autoJoin/"
        ]
        Gimbal.setAPIKey("248ff365-78f9-44f3-b6aa-a464a52ba524", options: options);      
```
