# ADR001 Event-Driven Camera Alerts

## Title
Event-Driven Camera Alerts

## Status
Accepted

## Context
We are designing an architecture for the Wildlife.ai project, which involves open-source wildlife cameras that capture and report observations of wildlife. Due to limited internet access in remote camera locations and email delivery challenges, we need a reliable and cost-effective way to alert users (mobile app) when camera events occur

## Decision
We have decided to implement an event-driven architecture for camera alerts, utilizing a service similar to Google's GCP Pub/Sub. This decision was made to address the challenges of email delivery and ensure reliable communication with the cameras.
Amazon SNS or similar would also work but it seems wildlife.ai is hosting its site on Google's infrastructure so staying in the Google ecosystem makes more sense at this point

## Rationale
1. **Limited Internet Access**: Many camera locations have unreliable or almost non-existent internet access, making email-based alerts impractical.

2. **Email SPF Challenges**: Modern email systems have stringent SPF (Sender Policy Framework) requirements, making it difficult for the cameras to send email notifications reliably.

3. **Cost-Effective Solution**: By using a service like GCP Pub/Sub, we can establish a reliable and cost-effective way to handle camera alerts. With a relatively small user base of a few hundred users, we can leverage the free tier of such services.

4. **Reliable Communication**: Event-driven architecture ensures that camera alerts are reliably delivered to users, enabling near real-time communication.

5. **Maintaining Contact**: This approach allows Wildlife.ai to stay in contact with all the cameras, even in remote areas, ensuring the project's success.


## Implementation Details
The implementation will involve setting up a Pub/Sub service to manage camera alerts. Cameras will be able to pass an email address and a short message to the Pub/Sub service. This service will handle the delivery of alerts to the mobile app on the user's behalf.

## Benefits
- Reliable and real-time alerts to mobile app users.
- Overcoming challenges associated with email delivery.
- Cost-effective solution that can stay within the free tier with a limited user base.
- Maintains contact with all cameras, even in areas with limited internet access.

## Considerations
- Ensure that the Pub/Sub service is appropriately secured to prevent unauthorized access.
- Implement monitoring and logging to track alert deliveries and system health.
