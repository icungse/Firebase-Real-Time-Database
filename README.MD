# Firebase-Real-Time-Database  
Simple Firebase Real Time Database for simple journaling app from [Kodeco tutorial](https://www.kodeco.com/29394678-firebase-real-time-database-tutorial-for-ios)
## Coverage

- Implement authentication with Firebase.
- Protect data access with security rules.
- Implement, listen to and store data with the Real-Time Database.
- Persist data offline.

  

## Firebase’s Security Rules

```
{
  "rules": {
    "users": {
      "$uid": {
        "thoughts": {
          ".read": "auth != null && auth.uid == $uid",
          ".write": "auth != null && auth.uid == $uid",
        }
      }
    }
  }
}
```