markdown
### State Diagram – VitalStats

mermaid
stateDiagram-v2
    [*] --> Monitoring
    Monitoring --> Synced: Data pushed to system
    Synced --> Flagged: Data anomaly detected
    Flagged --> Reviewed: Analyst checks data
    Reviewed --> Synced
    Synced --> [*]

Explanation:
	•	FR Reference: FR8 – Vital Statistics
	•	Use Case: Monitor Vital Statistics

---
