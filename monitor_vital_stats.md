markdown
### Activity Diagram – Monitor Vital Stats

mermaid
flowchart TD
    A([Start]) --> B[Wearable collects sleep/HRV]
    B --> C[Data syncs to mobile app]
    C --> D[Display stats in dashboard]
    D --> E{Data anomaly detected?}
    E -- Yes --> F[Flag for review]
    E -- No --> G[Log normally]
    F --> H([End])
    G --> H

Explanation:
	•	FR Reference: FR8 – Vital Statistics
	•	Use Case: Monitor Vital Statistics

---
