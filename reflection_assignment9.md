# Reflection – Assignment 9

## Challenges Faced

Designing the domain model and class diagram required carefully balancing abstraction with completeness. One challenge was deciding which objects deserved to be their own entities. For example, at first I treated Recommendation as a simple text string. But upon review of earlier use cases, I realized it had its own behavior (generate, accept, reject) and should be modeled as a class.

Another challenge was defining clear relationships, especially between Device, VitalStat, and ActivitySession. Since data flows between all three, I had to simplify the class connections to avoid circular complexity while still capturing business logic. I used aggregation for syncing and simple associations elsewhere.

Choosing appropriate multiplicities (e.g., 1..*, 0..1) also took careful thought. For example, a User must have one FitnessProfile, but may or may not have AnalyticsReports. This required double-checking state diagrams from Assignment 8 to verify flow accuracy.

## Alignment with Previous Assignments

The class diagram strongly reflects what was built in Assignments 4 through 8:

- *Assignment 4 (Functional Requirements):* The methods like syncData() and generateReport() are taken directly from system needs such as syncing wearable devices and providing analytics.
- *Assignment 5 (Use Cases):* Actions like "Track Real-Time Activity" and "Monitor Vital Stats" influenced method and class selection.
- *Assignment 6 (User Stories):* Stories such as "As a user, I want to receive personalized fitness recommendations" directly resulted in the Recommendation class.
- *Assignment 8 (State & Activity Diagrams):* State transitions like "Synced", "Generated", and "Viewed" helped define class attributes and logic.

## Trade-Offs Made

To keep the diagram readable and focused, I chose to avoid deep inheritance. Instead of making Device, AnalyticsReport, and VitalStat subclasses, I treated them as distinct but related entities.

Another trade-off was reducing some behavioral complexity. For example, instead of modeling event-based triggers for syncing or report generation, I represented those processes as method calls (e.g., sync(), generateReport()).

## Lessons Learned

This assignment strengthened my understanding of object-oriented thinking. It helped me realize that every attribute or relationship should be justifiable by real-world logic or functional requirements.

I also learned that early diagrams (like state diagrams) aren’t throwaway — they are foundational to solid domain and class design. This reflection exercise also made me appreciate traceability: each diagram and file should connect like puzzle pieces to show the system's bigger picture.

Ultimately, this exercise made me more confident in mapping system requirements into scalable, maintainable, object-oriented designs.
