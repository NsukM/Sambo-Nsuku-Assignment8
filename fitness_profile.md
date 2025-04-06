markdown
### State Diagram – FitnessProfile

```mermaid
stateDiagram-v2
    [*] --> Created
    Created --> Updated: User edits profile
    Updated --> Updated: More edits
    Updated --> Deleted: User removes profile
    Deleted --> [*]
```
Explanation:
	•	FR Reference: FR2 – Profile Management
	•	User Story: US-002 – “As a user, I want to personalize my fitness experience”

---
