###VIEWCONTROLLER.m:
Add GMBLBeaconManagerDelegate on top:
```
@interface ViewController () <GMBLPlaceManagerDelegate, GMBLCommunicationManagerDelegate>
@interface ViewController () <GMBLPlaceManagerDelegate, GMBLCommunicationManagerDelegate, **GMBLBeaconManagerDelegate**>
```

Add highlighted code after:
```
**@property (nonatomic) GMBLBeaconManager *beaconManager;**
@property (nonatomic) GMBLCommunicationManager *communicationManager;
```

Add highlighted code after:
```
self.communicationManager = [GMBLCommunicationManager new];
self.communicationManager.delegate = self;
**self.beaconManager = [GMBLBeaconManager new];**
    **self.beaconManager.delegate = self;**
    **[self.beaconManager startListening];**
```

Add highlighted code before:
```
# pragma mark - Gimbal PlaceManager delegate methods
(void)placeManager:(GMBLPlaceManager *)manager didEnterPlace:(GMBLPlace *)place date:(NSDate *)date
**- (void)beaconManager:(GMBLBeaconManager *)manager didReceiveBeaconSighting:(GMBLBeaconSighting *)sighting**
**{**
 **  NSLog(@"%@", sighting);**
**}**
```
