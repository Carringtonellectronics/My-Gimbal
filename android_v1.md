#Environment: STAGE (com.company)
##Default package name:
###Usercontext.properties:
1.	Add:
```
env=STAGE
place.state.available.on.server=true
```

2.	Add API key.

##Different package name:
###AndroidManifest.xml:
1.	Replace ‘default package' to your package name (2 changes)
2.	Click “Yes” when prompted to update Launch configurations
3.	Refactor the package name (src/main/java) to the package name for the API key.
4.	Click “Continue” when prompted.
5.	Click on the project and do a cmd+shift+o (organize imports to fix errors).

###Usercontext.properties:
1.	Add:
```
env=STAGE
place.state.available.on.server=true
````

2.	Add API key.

##GCM KEY:

Add google-play-services.jar: 

###AndroidManifest.xml:
Add: 
```
<meta-data android:name="com.google.android.gms.version" android:value="6171000" />
<uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />
```

###MallmartActivity:
1.	Add highlighted lines in contextConnectorEnabled() (Fix import):
```
private void contextConnectorEnabled() {
    setupListeners();
    startCompanyService();
    ContextPushNotificationsConnector.registerForRemoteNotification(this, "888494778239");
```

###OptInActivity.java:
```
1.	Add highlighted lines:
public void onCreate(Bundle savedInstanceState) {
       super.onCreate(savedInstanceState);
       this.setContentView(R.layout.optin);
    String gcmSenderId = "888494778239"; // <--- SET THIS STRING TO YOUR PUSH SENDER ID HERE (Google API project #) ##
}
```

```
public void onEnableClicked(View v) {
    Intent returnIntent = new Intent();
    setResult(RESULT_OK, returnIntent);
    finish();
       String gcmSenderId = "888494778239"; // <--- SET THIS STRING TO YOUR PUSH SENDER ID HERE (Google API project #) ##
```

#Environment: PRODUCTION (com.gimbal.android.sample)
##Default package name:
###Usercontext.properties:
1.	Add:
```
property.override.password=roto-type
place.state.available.on.server=true
```

2.	Add API key.
Different package name:
AndroidManifest.xml:
1.	Replace ‘default package' to your package name (2 changes)
2.	Click “Yes” when prompted to update Launch configurations
3.	Refactor the package name (src/main/java) to the package name for the API key.
4.	Click “Continue” when prompted.
5.	Click on the project and do a cmd+shift+o (organize imports to fix errors).

Usercontext.properties:
1.	Add:
property.override.password=roto-type
place.state.available.on.server=true

2.	Add API key.
GCM KEY:
AndroidManifest.xml:
1.	Add: 
<meta-data android:name="com.google.android.gms.version" android:value="6171000" />
<uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />

2.	Add google-play-services.jar: 

MallmartActivity:
1.	Add highlighted lines in contextConnectorEnabled() (Fix import):
private void contextConnectorEnabled() {
    setupListeners();
    startCompanyService();
    ContextPushNotificationsConnector.registerForRemoteNotification(this, "888494778239");


OptInActivity.java:
1.	Add highlighted lines:
public void onCreate(Bundle savedInstanceState) {
       super.onCreate(savedInstanceState);
       this.setContentView(R.layout.optin);
    String gcmSenderId = "888494778239"; // <--- SET THIS STRING TO YOUR PUSH SENDER ID HERE (Google API project #) ##
}

public void onEnableClicked(View v) {
    Intent returnIntent = new Intent();
    setResult(RESULT_OK, returnIntent);
    finish();
       String gcmSenderId = "888494778239"; // <--- SET THIS STRING TO YOUR PUSH SENDER ID HERE (Google API project #) ##

