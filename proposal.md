# 1. Team Members (intro and bio)

# 2. Problem Space

## 2.1 Purpose
## 2.2 Requirements
## 2.3 High Level Overview

![Business Overview](figures/business-overview.drawio.png "Business Overview")

## 2.4 Assumptions
* Camera will be purchased outside the application portal, could be either through phone order or directly from the Wildlife.ai
* When user purchases the physical camera device they will get access to the application to access all resources.
* Admin user have to register the end user up so that user can access the application
* Any integrations with partners and vendors applications can be configured in the application.


# 3. Solution Space

## 3.1 Context - Key Business Drivers

In the pursuit of business success, several critical factors stand out as the driving forces propelling Wildlife AI's operations forward. These key drivers encompass the core principles and objectives behind our team's technical solution to guide Wildlife AI's strategies and actions.

**Rapid Market Penetration And Prototype Testing**

One of the foremost drivers is the need for swift market access and the ability to introduce Wildlife AI's product for the testing of prototypes and ideas. This imperative arises from the desire to observe how Wildlife AI's innovations resonate with a wide spectrum of life forms inhabiting diverse ecosystems, including forests, oceans, and avian habitats. By quickly immersing Wildlife AI's solutions in these diverse environments, invaluable insights are gained into what works and what doesn't. This agile approach enables Wildlife AI to respond promptly to feedback, refining the product based on real-world usage and ensuring its suitability for various species and ecosystems across the globe.

**Species Conservation With Community/Government Collaboration**

Another pivotal driver Wildlife AI is the commitment to species conservation. Wildlife AI actively monitors the well-being and potential endangerment of various species, taking proactive measures when necessary. These actions may include engaging with local communities and collaborating with governmental authorities to protect and preserve threatened species. This reflects their dedication to sustainable practices and environmental protection, aligning core objectives with broader societal and ecological goals.

**Future-ready Integration Support**

In an ever-evolving technological landscape, the ability to adapt and evolve is paramount. Recognizing this, our solutions team is dedicated to enabling Wildlife AI to gear towards supporting future growth and innovation through robust integrations. This forward-thinking approach ensures that Wildlife AI's systems remain flexible and adaptable, accommodating emerging trends and technologies. By doing so, Wildlife AI can position itself to stay ahead of the curve and continue providing state-of-the-art solutions to support its mission.

### Summary
In summary, focusing on rapid market access, ecological conservation, and future-proofing systems that allow to shape the core values and actions of Wildlife AI the solution our team proposes should meet the needs of Wildlife AI's business today but also anticipate and address the challenges and opportunities of tomorrow.


## 3.2 Architecture Characteristics

After conducting a thorough analysis of Wildlife AI's requirements and key business drivers, we have identified the primary architectural characteristics that the system should incorporate. These key characteristics include Feasibility, Domain Part Abstraction, and Simplicity.

1. **Feasibility:** This architectural attribute ensures that the system's design aligns with the practicality of implementation within the available resources, budget, and time constraints. It underscores the significance of achieving rapid market access and supporting ecological conservation to further Wildlife AI's mission.

2. **Domain Part Abstraction:** The incorporation of domain part abstraction simplifies interactions within the system by hiding complex technical details and providing an intuitive interface with the help of API's. This abstraction streamlines the user experience, making it more user-friendly and reducing the learning curve.

3. **Simplicity:** Simplicity highlights the value of a clear and efficient system design. It advocates for an architecture that is easily comprehensible, user-friendly, and maintainable, ultimately improving overall usability and reducing operational complexity. If the solution is to be open-sourced, it should cater to a broad range of users, spanning from individuals with limited technical knowledge to highly skilled professionals.

Furthermore, we aim to provide the following additional architectural features:

4. **Security:** Furthermore, security being an implicit characteristic, is a crucial part of the system design. We are determined to put strong protections in place to keep all data in our systems safe, making sure data stays private and shielding it from any possible threats.

5. **Interoperability:** Interoperability means that our system can easily talk to and work with the tools and services our partners and vendors use. It helps Wildlife AI users to work well together with partners, vendors, and other ecosystem members to enhance wildlife conservation efforts.

6. **Workflow:** The introduction of workflow capabilities into the system streamlines processes and optimizes the flow of data and actions. It enhances operational efficiency and ensures that tasks are automated and well-coordinated within the solution.

By prioritizing these architectural characteristics, we aim to develop a system that not only aligns with Wildlife AI's current requirements but also offers adaptability for future growth and evolution. Our approach is geared towards delivering a feasible, user-friendly, and secure system that seamlessly interacts with external services and optimizes workflow processes where necessary.

## 3.3 Architecture Style Proposed

Based on the architectural characteristics we've identified, we suggest a combination of **Modular Monolith** and **Micro kernel architecture** to build the application. In this approach, we organize the different aspects of the business into modules and one of these modules uses micro-kernel design. Each of these modules has its own well defined API's that serve as a way for them to communicate with one another and the user interface components. This setup makes sure that the application is well-structured and can efficiently work with different integrations to support the business requirements.

![System Architecture Overview](figures/system-architecture-basic.drawio.png "System Architecture")



## 3.4 Other Considerations

Additionally, we recognize the importance of the system's ability to adapt and grow, especially when some users in the Wildlife AI's open-source community require more resources than others. In situations like these, as business needs change, the system should be capable of supporting growth by seamlessly scaling, potentially moving one or more services outside of the (modular-monolithic) application ecosystem to microservices. This flexibility guarantees that Wildlife AI's technical setup stays in sync with user's growing mission and operational requirements.



# 4. Domain Design

	## Overview 

	## Identification Of Domains

	## Domain Capabilities In-depth
		### User Domain
		### Camera Domain
		### Multimedia Domain
		### Notification Domain
		### Integration Domain


# System Architecture
	# Workflow api
	# Api's for other


# Long Term Expansions
* User purchasing can be done in the same portal by eliminating user registration by admin person
* Create and coordinate projects in the portal for community togetherness
* Sucess metrics of the camera
* Build strict boundaries so there is no direct communication between modules



# ADR's


# References
1. Software Architecture Patterns, 2nd Edition by Mark Richards
2. https://www.kamilgrzybek.com/blog/posts/modular-monolith-domain-centric-design
3. Architecture style worksheet https://www.developertoarchitect.com/downloads/architecture-styles-worksheet.pdf
4. https://github.com/Sairyss/domain-driven-hexagon





