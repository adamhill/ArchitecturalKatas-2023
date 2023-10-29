# ADR005 BFF

## Title
Backend For FrontEnd
## Status
Approved

## Context
We have decided to primarily use a mobile app to provision, adjust and retrieve photos from the camera

## Decision
We will use outward facing API's for user interaction apps

## Rationale
1. **Primarily Mobile App**: We have a mobile app for all camera interactions and a microkernel pattern for integrating with 3rd party API's and services. The MC can be hosted on the mobile monolith and provide more complex logic as needed (ex. GBIF & Model retraining)

## Implementation Details


## Benefits


## Considerations
