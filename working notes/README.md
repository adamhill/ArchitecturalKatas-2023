### Users
Biologists and nature enthusiasts (hundreds).

### Requirements


##  Assumptions

- Camera: The project takes advantage of the existing Wildlife.ai project, Wildlife Watcher, and assumes that its camera will be utilized. Furthermore, it establishes minimum hardware and software specifications for this camera.
  - Wildlife Camera
    - Hardware
      - Physical devices
      - Ultra-low-power microcontrollers (up to 512KB Flash)
      - Watertight 3D Printed Enclosure
     - Interchangeable modules including
        - optical sensors
        - IR lights
        - transceiver modules
        - batteries
    - Software
      - Triggered based on the movement of target animals
      - Sends small alert message to the users via LoraWan, 3G or satellite
      - Captures video footage
      - Processes video
      - Identifies  species
      - Provides an API or interface to control camera and settings and download models
      - Identifies species using models
      - Provides  (e.g. date, time, GPS location)
      - Records videos and images metadatametadata (e.g. date, time, GPS location, weather)

## Architecture Characteristics
Using https://www.developertoarchitect.com/downloads/architecture-characteristics-worksheet.pdf

- Scalability: Ensuring the system can support hundreds
- Availability, reliability, performance: Facilitating near real time communication
- Interoperability: Allowing seamless integration with third-party services and platforms such as Wildlife Insights, TrapTagger, iNaturalist, and GBIF. Interoperability enables users to work with their preferred tools and extends the project's reach by connecting it to established conservation and research networks. Since requirements state 
  - communicate with camera
  - analyze video using third party platforms
  - Publish to iNaturalist
  - Train model
  - Publish
- Security: To protect the data and prevent unauthorized access

## Identify Components
- System: Mobile App
  - Control camera
    - Turn on and off
    - Change settings
    - Upload models
  - Receives alerts from cameras
  - Receives video and images metadata from camera
  - Fetch video and images from camera
  - Analyzes videos using third-party platforms
  - Identify species
  - Trains edge models using labeled videos
  - Publishes frames to iNaturalist
  - Publishes species occurrences
  - Integration with databases of species to help in identification
  - Capture information that can shared along with the image are
  - Ability to run statistics on the data captured by the camera
    - GPS coordinates of the camera
    - Location, date and time information
    - Climatic data when the video is captured
    - Other sensor-based information.
  - Additional functionalities
    - Historic view of what actions have been taken after receiving the video. (Ex: Log)
    - Once you identify the species, the product should be able to run validation by connecting with other APIs.
  - Plan projects support by coordinating all players.
    - Ability to coordinate and plan projects in the portal with experts, students and non-profit organizations in a particular region
    - Ability to run statistics on the data captured by the camera to measure project success or other key success metrics
    - Coordinate with other enthusiasts who are part of other projects for community involvement.

- Wildlife Camera
  - Specs in the assumption section

- Notification System:
  - A push notification system that allows the camera to send a small piece of information

### Architecture Design Records
The linked ADRs contain the primary architectural decisions regarding the proposed design, including their context and rationale.

[ADR 001](https://github.com/adamhill/ArchitecturalKatas-2023/blob/main/ADRs/ADR001-EventDriven) - Event-Driven Camera Alerts: A push notification system like Amazon SNS, Google Pub/Sub will allow the camera to send information via an simple http command. The message will include email address of the receipient (configurable in the camera settings) and the body message (e.g. camera activated, species xxx identifies, storage crossing threshold, etc)

ADR 002 - Modular monolith to allow for faster build and test system. If the system is a success and scale starts becoming an issue. Refactor to microservices. LINK TO BOOK

[ADR 003](https://github.com/adamhill/ArchitecturalKatas-2023/blob/main/ADRs/ADR003-Processing%20with%203rd%20Parties%20and%20Edge%20Computing) - Processing with 3rd Parties and Edge Computing (to save on costs and move this to open source), no websites, global databases, comprenhesive list of all cameras, and locations

[ADR 004](https://github.com/adamhill/ArchitecturalKatas-2023/blob/main/ADRs/ADR004%20-%20Ease%20of%20Use%20-%20Mobile%20App%20Only.md) - Ease of use, a mobile app should is simple enough to install and troubleshoot (we all use apps on our phones) and remove the burden of maintaing local infrastructure or running containers or vms

[ADR 005](https://github.com/adamhill/ArchitecturalKatas-2023/blob/main/ADRs/ADR005%20-%20Backend%20For%20FrontEnd.md) - Front End to the Back End

ADR 006 - Integrations: Do not re-invent, integrate

## Preliminary phase
Before proposing an architecture, a comprehensive understanding of the organization, its context, and its capabilities is essential

Wildlife.ai (from website)
- charitable trust that uses artificial intelligence to accelerate wildlife conservation.
- works with grassroots wildlife conservation projects and develop open-source solutions using machine learning.
- organises community events, seminars and educational activities to build and maintain machine learning solutions to reduce the current rate of species extinction.
### Our purpose
To ensure artificial intelligence is widely applied to protect biodiversity.
### Other projects
[Wildlife Watcher](https://wildlife.ai/projects/wildlife-watcher/) A wildlife camera that records animals and uses AI to identify them

[Spyfish Aotearoa](https://wildlife.ai/projects/spyfish-aotearoa/) A citizen science and machine learning approach to identify fish in baited underwater videos

[Pepeketua ID](https://wildlife.ai/projects/pepeketua-id/) A pattern recognition software that facilitates the individual identification of Pepeketua, New Zealand endemic frogs

[Nesher Bari](https://wildlife.ai/projects/nesher-bari/) Using data analytics to boost the protection of griffon vultures

[Koster Observatory](https://wildlife.ai/projects/koster-observatory/) A machine learning and citizen science approach to analyse underwater footage from Sweden’s first marine national park.

Most of these projects involve machine vision, open-source systems that rely on AI, and machine learning to track, identify, or study wildlife. Moreover, the projects can be considered the building blocks for this new project since they represent proof of concepts of several features. The success of these projects indicates that Wildlife.ai is well-prepared to embark on an initiative that leverages its existing capabilities and expands them with multiple integrations 

## Architecture Vision
### Architecture Project
This project garners the support of Wildlife Executive Director, Victor Anton, and Board member Joshua Yellin, ensuring the executive backing necessary for a project of this magnitude within the Wildlife organization.
### Stakeholders, Concerns, and Business Requirements
- Biologists: These stakeholders are keen to embrace new technologies that can aid their work in wildlife conservation. They have concerns about the costs and the learning curve associated with adopting new solutions. User-friendly solutions are strongly preferred.
- Enthusiasts: Those who harbor a genuine curiosity for wildlife are eager to engage with the project. However, they are also sensitive to financial considerations and the effort involved. The accessibility and user-friendliness of the system are of paramount importance to them.
- Wildlife.ai: As a charitable trust dedicated to using artificial intelligence for the acceleration of wildlife conservation, Wildlife.ai places utmost importance on the funding and success of projects, as they are pivotal to the organization's mission and its future.


### Overall Solution
The proposed solution entails the development of a mobile application compatible with leading operating systems, such as Windows, MacOS, and Android, offering the following features:
  - Camera control
    - Turn on and off
    - Change settings
    - Upload models
  - Receives alerts from cameras via email
  - Integrated with third-party platforms to analyzes videos
  - Allow to label videos to enable training edge models
  - Publishes frames to iNaturalist
  - Publishes species occurrences
  - Log metadata information (from camera data and user entered)
#### Phases
##### Near term
The initial phase focuses on specifying the required API for Wildlife cameras and developing a mobile app with a minimal feature set to demonstrate the project's viability. This feature set must encompass the following:
- Prioritize Android due to its significant share of the [mobile market share](https://gs.statcounter.com/os-market-share/mobile/worldwide)) 
- Camera control
  - Turn on and off
  - Change settings
  - Upload models
- Receives alerts from cameras via email
- Manual Integrations: During this phase, all integrations can be conducted manually by utilizing third-party platforms to upload images and videos for identification.
- Community Involvement: Release the code to engage the community and encourage contributions.
##### Mid term
In the intermediate phase, the focus shifts to developing crucial integrations, including
- Integrated with third-party platforms to analyzes videos
- Allow to label videos to enable training edge models
- Publishes frames to iNaturalist
- Publishes species occurrences
##### Long term
The long-term phase concentrates on further developing and expanding integrations, solidifying the project's capabilities and reach.

This phased approach ensures the project's incremental growth and the gradual realization of its objectives while aligning with stakeholder needs and concerns.