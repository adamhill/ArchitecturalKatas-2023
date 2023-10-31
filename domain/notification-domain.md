# Notification Domain: Proving notification services 

The Notification capability enables the Wildlife AI cameras to send short notifications to the mobile app. The following features are provided by this capability:
- Camera uses an API to specify the email address to alert and the short message to transmit

This design allows to easily extend the short messages the camera can send based on new developments of the mobile app and the camera itself.

## Components

### Plugins

Each integration with partners and vendors is encapsulated within an individual plugin, with each plugin exposing its distinctive set of APIs. Internally, these plugins are configurable, enabling them to efficiently communicate with their respective partner APIs and function as adapters for data manipulation when exchanging information between image data and partner APIs. The module is constructed to smoothly accommodate future integrations, facilitating the incorporation of new plugins into the ecosystem.

### Core System
Core system has two components

#### 1. Google's Pub/Sub service

Pub/Sub is an asynchronous and scalable messaging service that decouples services producing messages from services processing those messages. Pub/Sub allows services to communicate asynchronously, with latencies on the order of 100 milliseconds. Pub/Sub will relay the API calls to email messages to the camera operators.

#### 2. Camera notification settings

The camera notifiation settings record the email address of its operators as well as the Wildlife AI's Pub/Sub service so the cameras can make the API calls to send messages.


## Related ADRs

[ADR 001](ADRs/ADR004%20-%20Ease%20of%20Use%20-%20Mobile%20App%20Only.md)

## Summary
In summary, the notification domain is the main communication system for the Wildlife AI's cameras, ensuring that they can transmit short messages in near real time.