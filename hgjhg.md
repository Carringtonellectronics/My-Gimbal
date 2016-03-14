#Environment: STAGE (default package name)
##Default package name:
###AppService:
1-Add Endpoints
2-Add imports:
import java.util.HashMap;
import java.util.Map;

3-Add API key.

##Different package name:
###AndroidManifest.xml:
1-Replace ‘default package' to your package name (2 changes)
2-Click “Yes” when prompted to update Launch configurations
3-Refactor the package name (src/main/java) to the package name for the API key.
4-Click “Continue” when prompted.
5-Click on the project and do a cmd+shift+o (organize imports to fix errors).

AppService:
1.	Add Endpoints
2.	Add imports:
import java.util.HashMap;
import java.util.Map;

3.	Add API key.
GCM KEY:
AndroidManifest.xml:
1.	Add: 
<meta-data android:name="com.google.android.gms.version" android:value="6171000" />
<uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />

2.	Add google-play-services.jar: 

OptInActivity.java:
1.	Add:
 // Setup Push Communication
    	String gcmSenderId = "888494778239"; // <--- SET THIS STRING TO YOUR PUSH SENDER ID HERE (Google API project #) ##
    	registerForPush(gcmSenderId);


Environment: PRODUCTION (com.gimbal.android.sample)
Default package name:
AppService:
1.	Add API key.

[Gimbal setAPIKey:@"## PLACE YOUR API KEY HERE FROM MANAGER ##" options:nil];

Different package name:
AndroidManifest.xml:
1.	Replace ‘default package' to your package name (2 changes)
2.	Click “Yes” when prompted to update Launch configurations
3.	Refactor the package name (src/main/java) to the package name for the API key.
4.	Click “Continue” when prompted.
5.	Click on the project and do a cmd+shift+o (organize imports to fix errors).

AppService:
1.	Add API key.

[Gimbal setAPIKey:@"## PLACE YOUR API KEY HERE FROM MANAGER ##" options:nil];

GCM KEY:
AndroidManifest.xml:
1.	Add: 
<meta-data android:name="com.google.android.gms.version" android:value="6171000" />
<uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />

2.	Add google-play-services.jar: 

OptInActivity.java:
1.	Add:
 // Setup Push Communication
    	String gcmSenderId = "888494778239"; // <--- SET THIS STRING TO YOUR PUSH SENDER ID HERE (Google API project #) ##
    	registerForPush(gcmSenderId);

PushRegistrationHelper.java:
1.	Add: 


 // Setup Push Communication
    	String gcmSenderId = "888494778239"; // <--- SET THIS STRING TO YOUR PUSH SENDER ID HERE (Google API project #) ##
    	registerForPush(gcmSenderId);
