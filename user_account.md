### State Diagram – UserAccount

mermaid
stateDiagram-v2
    [*] --> Registered
    Registered --> Active: Email verified
    Active --> Locked: Too many failed attempts
    Locked --> Active: Admin unlocks
    Active --> Deactivated: User deletes account
    Deactivated --> [*]

Explanation:
	•	FR Reference: FR1 – User Registration and Authentication
	•	User Story: US-001 – “As a user, I want to register and log in”
	•	Kanban Link: “Implement Login Functionality” (In Progress)

---

