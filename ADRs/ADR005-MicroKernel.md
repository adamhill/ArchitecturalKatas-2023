# ADR005 Entire Application Architecture

## Title
Use the micro kernel architecture style for the integrations module

## Status
Proposed

## Context
Our application needs to connect with other partners and vendors because Wildlife AI users want to share their data with other ecosystem members. In the future, we may need to add more ways for our app to connect with new partners as the community gets bigger.

## Decision
We have chosen to adopt the micro kernel architecture style explicitly for the development of this module.

## Consequences
### Feasibility
This choice is cost-effective and will enable us to build the solution more swiftly compared to other architectural styles, aligning well with resource constraints and timelines.

### Domain Part Abstraction
In this approach, we treat each integration as a separate plugin. These plugins act as connectors that is capable of connecting to their respective API's and handle data transfer between our system and the partner or vendor we want to share information with.

### Configurability
Provides us with flexibility when dealing with the various configurations required for integrating with partner APIs.

### Interoperability
This module offers an easy way to connect with partners and vendors, and it can be easily expanded to meet future business requirements.
