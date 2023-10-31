# ADR 003: Processing with 3rd Parties and Edge Computing

## Title
Processing with 3rd Parties and Edge Computing

## Status
Proposed

## Context
The Wildlife.ai project involves open-source wildlife cameras that capture, identify species, and report observations. To ensure cost-efficiency, sustainability, and leverage open-source resources, a decision needs to be made regarding the processing of data, specifically moving away from central websites, global databases, and maintaining a comprehensive list of all cameras and locations.

## Decision
We have decided to move data processing to 3rd parties and leverage edge computing for the Wildlife.ai project. This decision is based on several factors:

## Rationale
1. **Cost Efficiency**: Hosting and maintaining central websites and global databases can be costly. By moving processing to 3rd parties, we can reduce infrastructure costs and optimize resource allocation.

2. **Sustainability**: Leveraging edge computing allows cameras to process data locally, reducing the need for continuous, high-bandwidth internet connections. This approach supports sustainability, especially in remote or off-grid camera locations with limited internet access.

3. **Open Source**: The use of open-source third-party solutions for data processing aligns with the project's open-source nature. It encourages collaboration and contributions from the community.

4. **Scalability**: Edge computing allows cameras to operate independently, making the system scalable to accommodate a growing number of cameras and locations.

5. **Data Security**: Processing data locally on the cameras enhances data security and privacy, reducing the need to transmit sensitive information over the internet.

6. **Reduced Complexity**: Eliminating the need for a central website and global databases simplifies the architecture, reducing potential points of failure and operational complexity.

## Implementation Details
- Utilize open-source third-party services for data processing, such as TensorFlow Lite for on-device machine learning.
- Cameras will process video footage and identify species locally using edge computing capabilities.
- Implement secure data transfer protocols for transmitting minimal essential data to the mobile app and third-party services.
- Integrate with third-party services for analysis, species identification, and other data processing tasks.

## Benefits
- Cost-efficient infrastructure with reduced hosting expenses.
- Enhanced sustainability, particularly in areas with limited internet access.
- Alignment with open-source principles, fostering community collaboration.
- Scalable and independent camera operation.
- Improved data security and reduced privacy risks.
- Simplified architecture with lower complexity.

## Considerations
- Ensure that third-party services are reliable, secure, and align with the project's goals.
- Develop data synchronization and update mechanisms to maintain accurate data records.

