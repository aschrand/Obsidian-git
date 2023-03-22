---
created: 2023-01-19T15:25:34 (UTC +01:00)
tags: [security]
source: https://www.redhat.com/architect/nonfunctional-requirements-architecture?utm_campaign=refferal&utm_medium=refferal&utm_source=futurecx
author: Love Sharma
type: definitie
---

# Security

---
Security is the degree to which the software protects information and data so that people, other products, or systems have data access appropriate to their types and levels of authorization. This family of characteristics includes the following five attributes:

-   **Confidentiality:** Data is accessible only to those authorized to have access.
-   **Integrity:** The software prevents unauthorized access to or modification of software or information.
-   **Nonrepudiation:** Prove whether actions or events have taken place.
-   **Accountability:** Trace user actions.
-   **Authenticity:** Prove the user's identity.

Additional security requirements include:

-   **Auditability**: Audit trails track system activity so that when a security breach occurs, you can determine the mechanism and extent of the breach. Storing audit trails remotely, where they can only be appended, can keep intruders from covering their tracks.
-   **Legality**: This involves adherence to laws or other industry requirements.
    -   _Compliance:_ Adherence to data protection laws like GDPR, CCPA, SOC2, PIPL, or FedRamp
    -   _Privacy:_ Ability to hide transactions from internal company employees, such as encrypting transactions so that even database administrators and network architects cannot see them
-   **Authentication**: Security requirements ensure users are who they say they are.
-   **Authorization**: Security requirements ensure users can access only certain functions within the application (by use case, subsystem, web page, business rule, field level, and so forth).


See: [[Nonfunctional-requirements]]
