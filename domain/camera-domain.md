# Camera Domain: Camera settings and Notification

This domain has the following responsibilities in allowing users to:

* Remotely adjust camera settings, removing the necessity for physical interaction with the camera.
* Establish notification links for the camera to alert the service as required.
* Manage minimal user information related to camera ownership.
* Stores minimal camera hardware specifications.

### Camera Settings:

* To set the cameras on/off,
* Adjust settings without opening the cameras

### Notification:

The domain must handle two types of messages:

#### Identification Notification:
* Sending a payload containing information about the identified species and image metadata.

#### Camera Health
* Send messages indicating various status conditions, such as:
    * Errors
    * Low battery
    * Full SD card
    * Camera movement or tilt detection, etc.,

### User Attributes:
* Manage minimal user attributes associated with camera ownership

### Camera Hardware Specifications:
* Handles hardware specifications and technical information as is.

## Related ADRs
[ADR 001 - Modular Monolith](../ADRs/ADR002-ModularMonolith.md)

[ADR 001 - Mobile Application](../ADRs/ADR004%20-%20Ease%20of%20Use%20-%20Mobile%20App%20Only.md)

[ADR 001 - Event Driven](../ADRs/ADR001-EventDriven.md)

## Summary
In summary, the Camera domain empowers users by enabling remote adjustment of camera settings and configure notification for timely alerts.