markdown
### State Diagram – Recommendation

mermaid
stateDiagram-v2
    [*] --> Generated
    Generated --> Viewed: User opens suggestion
    Viewed --> Accepted: User accepts
    Viewed --> Rejected: User dismisses
    Rejected --> [*]
    Accepted --> [*]

Explanation:
	•	FR Reference: FR6 – Personalized Recommendations
	•	User Story: US-002 – “Get weekly personalized recommendations”

---
