# Class Diagram – Fitness Tracker

```mermaid
classDiagram

class User {
    -userId: String
    -name: String
    -email: String
    -password: String
    -fitnessGoal: String
    +register()
    +login()
    +updateGoal()
}

class FitnessProfile {
    -age: Int
    -weight: Float
    -height: Float
    -activityLevel: String
    +calculateBMI()
    +updateProfile()
}

class ActivitySession {
    -sessionId: String
    -date: Date
    -duration: Int
    -steps: Int
    -calories: Float
    +startSession()
    +endSession()
    +sync()
}

class Device {
    -deviceId: String
    -brand: String
    -model: String
    -isConnected: Boolean
    +connect()
    +disconnect()
    +syncData()
}

class Recommendation {
    -recId: String
    -type: String
    -content: String
    -status: String
    +generate()
    +accept()
    +reject()
}

class VitalStat {
    -statId: String
    -heartRate: Int
    -sleepQuality: String
    -HRV: Float
    -timestamp: Date
    +analyzeStat()
    +flagAnomaly()
}

class AnalyticsReport {
    -reportId: String
    -reportDate: Date
    -summary: String
    -trends: String
    +generateReport()
    +export()
}

class DataAnalyst {
    -analystId: String
    -name: String
    -accessLevel: String
    +reviewStat()
    +manageReports()
}

User "1" -- "1" FitnessProfile
User "1" --> "0..*" ActivitySession
User "1" --> "0..1" AnalyticsReport
Device "1" --> "0..*" ActivitySession
FitnessProfile "1" --> "0..*" Recommendation
Device "1" --> "0..*" VitalStat
DataAnalyst "1" --> "0..*" AnalyticsReport
DataAnalyst "1" --> "0..*" VitalStat

