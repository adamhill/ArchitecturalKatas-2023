# ADR002 Entire Application Architecture 

## Title
Use the modular monolith architecture style

## Status
Proposed

## Context

Our application is designed to handle user management, camera settings control, receiving camera-triggered notifications, and multimedia processing. It can also integrate with partners and vendors. We are developing this application using a modular monolith architecture. As the plan to make the application open-source for end users, we are committed to ensuring that it remains easy to understand, build, deploy, and modify when needed.

## Decision

We have chosen to adopt the modular monolith architecture style for the development of our solution.

## Consequences

### Feasibility
This choice is cost-effective and will enable us to build the solution more swiftly compared to other architectural styles, aligning well with resource constraints and timelines.

### Domain Part Abstraction
In this approach, we isolate each domain, allowing them to communicate with one another through clear APIs. This design offers flexibility, enabling us to modify internal components as needed. In addition, by adopting a domain-centric design, our solution remains adaptable and can connect to various cloud services without being tied to a specific one.

### Simplicity
The chosen architecture is easily understandable, user-friendly, and straightforward to maintain. This enhances overall usability and reduces operational complexity, ensuring that our solution is approachable and efficient.
