# Multimedia Domain: Proving Multimedia services to Mobila App 

The Multimedia capability enables the Wildlife AI Mobile App to receive images from the Wildlife AI cameras. The following features are provided by this capability:
- Store images and videos with their metadata in the Mobila App storage.

This design removes the need of central storage and allows each camera operator to store as little or as many images/videos as needed and as possible on their devices.

[**LINK TO DOMAIN DIAGRAM**]

## Components
The Bluetooth spec already has a well defined protocol stack for initiating communications and transfer with controllers and peripherals

[** Explaination about the BT capabilities model**]

[**LINK TO SIMPLE BLUETOOTH STACK DIAGRAM**]

### Plugins

We recommend that W.ai reuse the file transfer capabilities already present in the Bluetooth spec.

According to the current images on iNaturalist, images are only 640x480 and ~15K. Easily handlible by Bluetooth speeds.


### Core System
Core system has two components

#### 1. Bluetooth service

(Explanation of stuff already built in)

#### 2. Camera Multimedia features

The camera record the images and store them locally until a user transfer them to a device via the Mobile App


## Related ADRs

[ADR 003](https://github.com/adamhill/ArchitecturalKatas-2023/blob/main/ADRs/ADR003-Processing%20with%203rd%20Parties%20and%20Edge%20Computing)

## Summary
In summary, the Multimedia domain is the main image system for the Wildlife AI's Mobile App, ensuring that users can store images and videos for processing and cataloging.