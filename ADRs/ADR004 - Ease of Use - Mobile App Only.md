# ADR004 Ease of Use - Mobile Device Primarily

## Title
Easy of Use - Primarily use a Mobile App

## Status
Accepted

## Context
From the initial requirements, the mobile app for Wildlife.ai seems to be the most mentioned device next to the camera itself. Setting up, adjusting and retreving the photos all mention a mobile application

## Decision
We have decided that the primary interaction model will be an app, primarily built for mobile devices.

## Rationale
1. **Explicit mention** :Provisioning, model re-uploading & adjusting camera parameters explicitly will need a mobile device. 

2. **Remote location**: The cameras themselves are out in nature and requiring a laptop to be carried to the camera's site is unneccesary.

3. **Photo Retreival** Photo can also be offloaded from the camera with the mobile device as well. There should be no need to open up the camera to retrieve photos, reducing wear and tear on the weather sealing and possible camera failure. All mobile phones have WiFi and Bluetooth.

4. **Cost** By using a cross-platform framwork the app can be written using common codebase and simply recompiling for the needed platform (iOS, Android) and if the correct toolkit is chosen, Wildlife.ai can get a Windows, macOS with very little effort and a web app with a bit more effort if the need arises

## Implementation Details
The mobile app should be written in one of the many cross platform mobile toolkits that are available to build mobile apps. They can all acccess native API's (WiFi & Bluetooth) as needed.

These include:
- **Xamarin / Maui**: Can compile to iOS, Android, macOS, Windows, Hybrid-Web (easy control and business logic reuse from the mobile / deskop apps)
- **React (Native)**: iOS, Android, Windows, macOS, Hybrid-Web (once again thru control and business logic reuse)
- **Angular & Angular Web Views**: iOS, Android, macOS, Windows, Hybrid-Web


## Benefits
- Single app for operations by users
- Less user API and front-end development for Wildlife.ai
- Portability and Ease of Use out in the field
- Ubiquity, large percentage of enthusiasts and user will have access to a mobile device

## Considerations
- Pick the mobile framewwork that gives to most possibility for expansion to the web