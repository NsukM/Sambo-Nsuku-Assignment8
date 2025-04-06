markdown
### Activity Diagram – Sync Device Data

mermaid
flowchart TD
    A([Start]) --> B[Device connects to app]
    B --> C{Is device authorized?}
    C -- Yes --> D[Initiate data sync]
    D --> E{Sync successful?}
    E -- Yes --> F[Update database]
    E -- No --> G[Retry or log error]
    F --> H([End])
    G --> H

Explanation:
	•	FR Reference: FR4 – Device Integration
	•	Use Case: Sync Device Data

---
