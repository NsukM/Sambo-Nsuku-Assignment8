markdown
### State Diagram – AnalyticsReport

mermaid
stateDiagram-v2
    [*] --> Queued
    Queued --> Processing: Data analyzed
    Processing --> Completed: Report ready
    Processing --> Failed: Error occurred
    Failed --> Retried: Retry analysis
    Retried --> Completed
    Completed --> [*]

Explanation:
	•	FR Reference: FR5 – Fitness Analytics
	•	Use Case: Generate Fitness Analytics

---

## ACTIVITY DIAGRAM FILES

---
