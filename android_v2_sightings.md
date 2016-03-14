/*AppService.java:*/
```
//Add highlighted code in the onCreate method:
    @Override
    public void onCreate() {
        events = new LinkedList<GimbalEvent>(GimbalDAO.getEvents(getApplicationContext()));
        Gimbal.setApiKey(this.getApplication(), "fd6e1bd0-5379-4225-8d29-eb2b0e5d0551");
        // Setup PlaceEventListener
        placeEventListener = new PlaceEventListener() {
        
        //***************************HIGHLIGHTED***************************/
        public void onBeaconSighting(BeaconSighting sighting, List<Visit> visits) {
        Log.e("BeaconSighting1: {}", sighting.getBeacon().getIdentifier() + " " + sighting.getRSSI()) ;
        Iterator<Visit> itr = visits.iterator();
        while (itr.hasNext()) {
        Log.e("BeaconVisits: {}", itr.next().getPlace().getName());
        }
        }
        //***************************HIGHLIGHTED***************************/
```
