markdown
### Activity Diagram – Receive Personalized Recommendations

```mermaid
flowchart TD
    A([Start]) --> B[System checks user history]
    B --> C{Has enough data?}
    C -- Yes --> D[Generate personalized recommendations]
    C -- No --> E[Provide generic suggestions]
    D --> F[Display to user]
    E --> F
    F --> G([End])
```
Explanation:
	•	FR Reference: FR6 – Personalized Recommendations
	•	User Story: US-002
	•	Use Case: Receive Personalized Recommendations

---
