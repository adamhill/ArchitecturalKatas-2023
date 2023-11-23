# Kata Presentation Script - Fall 2023

## 1. Front Matter
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

[**Wonderous Toys slide**]
>
> Hello
>
> We are Wonderous Toys and we are here to present our solution to the Wildlife.ai Kata.
>
> [**PRETTY PICTURES OF WILDLIFE.AI's CAMERA AND PUBLICITY MATTER**]
>
> Imagine a world where our wildlife is at risk, and conservation efforts are hindered by challenges like limited internet access in remote areas and the complexities of identifying animal species,
>
>Welcome to Wildlife.ai, a charitable trust using artificial intelligence to accelerate wildlife conservation. Our current project involves open-source wildlife cameras capturing and identifying species, a critical initiative for global conservation efforts.
>
> They are a New Zealand charity that wants to build rugged, outdoor, Open Source cameras that anyone can download the plans for and build and run the software for free. The cameras take pictures of small creatures, triggered by motion and get identified by a **local** AI module running **in** the camera.
>

> They would also like to aggregate this identification data for sharing with other wildlife systems, retrain their AI models based on the local fauna observed and periodically refresh the AI models on the camera.
>
>[**Show Sharing bits - iNaturalist, Edge Impulse, GBIF**]
>

>
> There are some particular considerations and constraints from the Wildlife.ai we are addressing with our proposed solution.
>
> This is an open source solution so we will mainly consider open source systems, frameworks, languages and specifications when we are able to.
>
> [**Open source image build**]
>
> There are only 100's of users anticipated by Wildlife.ai so we don't need a hightly scalable infrastructure.
>
> [**People Pictures, maybe people, rangers and biologists**]
>
> Next we anticipated the need to possibly expand the system, becoming more distributed as needed.
>If Wildlife.ai's software team, follows our mobile framework recommendations the software team could break out modules as needed into server side components that could be run in application containers running the cloud or at a nature area with their BYOC (bring your own computer) IT infrastructure.
>
>[**Show build of components being lifted out of the mobile app and into a container**]
>
> This is also a very cost effective solution. By only using mobile apps we can harness the power of modern phones to let park rangers, biologists and nature enthusiasts to harness the Wildlife.ai ecosystem.
>
> [**Mobile phone pics build**]
>
>Our solution emphasizes: **Simplicity**, **Frugality** and **Autonomy**

>[**Build these words?**]

## 2. The Meat
(PubSub, Camera, Mobile)
>Our phased approach ensures a sustainable, user-friendly solution. We start with the essential features, gradually expanding to more integrations, making Wildlife.ai a leader in AI-driven wildlife conservation.
>
>[**Transition to Architecture Overview**]
>
>Now, let's delve into the architecture that powers this solution.
>
> We have opted for a simple solution, that doesn't require a large amount tech resources.
>
> [**Show star chart**]
>
> The largest resource required, outside of the design and engineering of the camera itself and hardware costs, will be building the mobile app.
>
> But doing the mobile app development with the correct framework will let a small team with a single code base build the mobile app more easily.
>
> There does not need to be any re-occuring costs other than the PubSub Notification System

### PubSub / Event Driven
- Notifications from the camera
  - Network connection over straight-up WiFi, WiFi Mesh, Satellite or LoRa radios
  [** Build these ideas, *show* what Mesh means**]
  - Pub-Sub - It-Just-Works(TM) - REST-like endpoints or email
    - They can choose to use which ever combination are more reliable / cost effective depending on location adn connectivity

### Camera
- Provisioning, adjusting, adding updated models and ad-hoc retrieval from remote cameras can be done with a single mobile app
  - **Local Bluetooth** - Almost 30 years old and is on almost every mobile phone and tablet
  - **TCP/IP over WiFi or Ethernet** - A connection with a micro webserver exposing some API enpoints with REST / gRPC [Examples of microcontrollers that already do both or either]  [LoRaPipe](https://github.com/jgoerzen/lorapipe/blob/master/doc/lorapipe.1.md)

### Mobile
- Another key idea is to write the mobile app within an ecosystem that allows you to:
  1. Use the same codebase for *at least* the Android and iOS app stores.
  2. If a server side Modular Monolith piece is needed, you can lift that domain out of the mobile code and not have to completely rewrite it for server use.
     1. The most suitble ecosystems for this are:
        1. The Xamarin / MAUI (mobile) & Blazor(web) using C#
        2. React Native (mobile) & React (web) using Typescript
        3.  Angular Web views (web) & Hosted Angular Web Views (mobile) using Typescript
    1.  These components need to be able to run inside of a container to support the Modular Monolith style of server apps

>We will also use a microkernel architecture piece to provide a unified facade to the the external services that the user might want to interface with this includes:
>
> [**Build Microkernel modules list**]
>
> - Labeling and sharing services
>   - iNaturalist, GBIF
> - Model retraining
>   - Edge Impulse, Tensorflow
>- ?? ?? ??

## 3. Summary and Reinforcement of the Solution
[**Build lots of Wildlife.ai, pics and Nature Pics as we read**]
>
>This proposed solution for Wildlife.ai, is not just addressing the challenges of today; it will help  shape the future of wildlife conservation. Join us in this journey towards a world where AI empowers us to protect and preserve the incredible biodiversity that surrounds us.

[**Thank You Slide with all of Our Pics and Names**]

- Circular pics of us with our names. (First or last??)
> Thanks for the opportunity to present our solution in the Semifinals