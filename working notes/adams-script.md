# Kata Presentation Script - Fall 2023

## Front Matter
- Problem statement
- Particular charaqcteristics unique to the problem
  - Open Source
    - People can make their own camera or buy them from someone else that made them
    - Source code for apps is out on Github or someplace else. With Wildlife.ai doing lightweight admin and controlling releases.
  - Only 100's of users
  - People might sneakernet or email result to W.ai and can just upload to the other 3rd parties.
  - Resource contrainted
    -  Remoteness and **limited** connectivity of the cameras
    -  W.ai is a charity
> Hello
>
> We are Wonderous Toys and we are here to present our solution to the Wildlife.ai Kata. Wildlife.ai is a New Zealand charity that wants to build rugged, outdoor, Open Source cameras that anyone can download the plans for and build. The cameras can take pictures of small creatures, triggered by motion and get identified by a **local** AI module running on a microcontroller in the camera. They also would like to aggregate this identification data for sharing with other wildlife systems, retrain their AI models based on the local fauna observed and  periodically refresh the AI models on the camera.
>
> There are some particualr challenges we will address with our proposed solution. First off this is an open source solution so we will consider mainly open source systems, frameworks, languages and specifications when we are able to. Secondly, There are only 100's of users anticipated by Wildlife.ai so we wont need a very scalable infrastructure. In-fact we have the idea of Wildlife.ai's software team being able to break out modules as needed into server side components that could bw run in the cloud or at a nature area with their BYOC (bring your own computer) IT.
> 

**[CAN WE MAKE A VENN DIAGRAM OUT OF THIS]

## The Meat
(PubSub, Camera, Mobile)


- We have opted for a simple solution, that doesnt require large tech resource
  [Show star chart]
- The largest resource required, outside of the design and engineering of the camera specs and hardware, will be building the mobile app. But doing non-native app development will let a small team with a single code base build the mobile app more easily.

### PubSub / Event Driven
- Notifications from the camera
  - Pub-Sub - It-Just-Works(TM) - REST-like endpoints or email
    - They can chose to use which ever is more reliable / cost effective depending on location adn connectivity
  
### Camera
- Provisioning, adjusting, adding updated models and ad-hoc retrieval from remote camera
  - **Local Bluetooth** - Almost 30 years old and is on almost every mobile phone and tablet 
  - **TCP/IP over WiFi, Ethernet or LoRa radios** - A connection with a micro webserver exposing some API enpoints with REST / gRPC [Examples of microcontrollers that already do both or either]  [LoRaPipe](https://github.com/jgoerzen/lorapipe/blob/master/doc/lorapipe.1.md)

### Mobile
- A key idea is to write the mobile app within an ecosystem that allows you to:
  1. Use the same codebase for *at least* the Android and iOS app stores.
  2. If a server side Modular Monolith piece is needed, you can lift that domain out of the mobile code and not have to completely rewrite it for server use.
     1. The most suitble ecosystems for this are:
        1.  The Xamarin / MAUI (mobile) & Blazor(web) using C#
        2.  React Native (mobile) & React (web) using Typescript
        3.  Angular Web views (web) & Hosted Angular Web Views (mobile) using Typescript
    1.  These components need to be able to run inside of a container to support the Modular Monolith style of server apps  

We also want to use a microkernel architecture piece to provide a unified facade to the the external services that the user might want to interface with.
- Labeling and sharing services
- Model retraining

## Summary and Reinforcement
