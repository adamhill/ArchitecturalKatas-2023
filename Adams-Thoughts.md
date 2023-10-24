## Charity == inexpensive implementation

* Perhaps the web app (if we decide to build it) could be Containerized (SQLLite) so individuals / orgs can run a local collection system, that feeds into the “official” W.ai system.
* Could lower W.ai’s operational costs / burden.


## Geographically remote
* No or intermittent internet service. Definitely store and forward when connected or until retrieved.
* Cameras might be in *really* remote areas and be retrieved for en-mass download or visited by a ranger for mobile data collection (Satellite comms are expensive - Discussion point)
* Might need *aggregators* that can be *close by*. Than can funnel data back to Wildlife.ai home base / data stores.
* Small user base - reqs say 100’s But what would be the ratio of users to cameras? Could a refuge have a 1000 cameras supported by a few rangers?
* Might get away with Application Containers / Docker (cheap) for all non-edge services. Also might easily support the aggrefgator idea above 

## Mobile vs Mobile + desktop / web
* Biologists might need a desktop or web app (Discussion point)
Dashboard for observability into participating camera network.
* Cameras might misidentify things need to allow labelling or correction of videos ie. Fix bounding boxes + mis identification to allow re-training of models accurately
* Collect individual correct hits and send package them up for adding to the models.

## On-boarding 
* Cameras are going to be given to, purchased or even made by enthusiasts or remote biologists.
* So there might need to be some system so an enthusiast can onboard  their camera in a completely different continent with minimal interventions by W.ai into the camera network. *Question for judges*

## Mobile-ish / Networking
* I don’t think we need to limit the mobile app to Android. 
* I do Xamarin, we supported a 1.2MM DAU app for iOS and Android with a single team of 5 at Paycor. Adia has 50-60K users with just 2 of us. Flutter and React Native also let small teams or even 1 person handle two App stores.
* API or Bluetooth signaling for the camera talking to the mobile device (Ask Q about no WiFi in the specs)
* Maybe IoT edge style hub for signaling back to W.ai home base
* Will also need some minor error reporting for hardware errors and “flash is full” come get the data.
* Pictures won’t be transmitted back, they will only be collected **????**  *Question for judges*



*All mobile is a good ADR discussion point.*