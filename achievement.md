
markdown
### State Diagram – Achievement

mermaid
stateDiagram-v2
    [*] --> Earned
    Earned --> Shared: User posts to community
    Earned --> Ignored: User skips sharing
    Shared --> [*]
    Ignored --> [*]

Explanation:
	•	FR Reference: FR7 – Community Integration
	•	User Story: “As a user, I want to share my achievements”

---
