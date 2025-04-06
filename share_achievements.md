markdown
### Activity Diagram – Share Achievements

mermaid
flowchart TD
    A([Start]) --> B[User hits milestone]
    B --> C[Prompt user to share]
    C --> D{Does user want to share?}
    D -- Yes --> E[Select sharing option]
    E --> F[Post to feed or social media]
    D -- No --> G[Store locally only]
    F --> H([End])
    G --> H

Explanation:
	•	FR Reference: FR7 – Community Integration
	•	Use Case: Share Achievements

---
