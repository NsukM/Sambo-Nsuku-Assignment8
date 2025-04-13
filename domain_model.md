# Domain Model – NsukuSambo Fitness Tracker

This domain model describes the core entities, their attributes, methods, relationships, and business rules.

---

## Entity Overview

| Entity            | Attributes                                           | Methods                                | Relationships                                              |
|-------------------|------------------------------------------------------|----------------------------------------|------------------------------------------------------------|
| *User*          | userId, name, email, password, fitnessGoal           | register(), login(), updateGoal()      | Has one FitnessProfile, Owns many ActivitySessions         |
| *FitnessProfile*| age, weight, height, activityLevel                   | calculateBMI(), updateProfile()        | Belongs to User                                            |
| *ActivitySession*| sessionId, date, duration, steps, calories          | startSession(), endSession(), sync()   | Belongs to User, Linked to Device                          |
| *Device*        | deviceId, brand, model, isConnected                  | connect(), disconnect(), syncData()    | Connects to User, Syncs data to ActivitySession            |
| *Recommendation*| recId, type, content, status                         | generate(), accept(), reject()         | Linked to FitnessProfile                                  |
| *VitalStat*     | statId, heartRate, sleepQuality, HRV, timestamp      | analyzeStat(), flagAnomaly()           | Logged by Device, Viewed by DataAnalyst                   |
| *AnalyticsReport*| reportId, reportDate, summary, trends               | generateReport(), export()             | Generated for User, Managed by DataAnalyst                |
| *DataAnalyst*   | analystId, name, accessLevel                         | reviewStat(), manageReports()          | Reviews VitalStats, Generates Reports                     |

---

## Business Rules

- A *User* must have one and only one *FitnessProfile*.
- A *User* can own multiple *ActivitySessions*.
- A *Device* must be connected to sync data into an *ActivitySession*.
- A *Recommendation* is personalized and linked to a *FitnessProfile*.
- Only a *DataAnalyst* can review flagged *VitalStats* and generate *AnalyticsReports*.
- An *ActivitySession* must contain valid time and calorie data to be synced.

