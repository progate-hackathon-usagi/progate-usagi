```mermaid
erDiagram
  users ||--|| profiles : ""
  profiles ||--o{ exercise_logs : ""
  
  %% https://supabase.com/docs/guides/auth/managing-user-data
  profiles {
    uuid id PK "references auth.users"
    text username
    timestamp created_at
    timestamp updated_at
  }

  exercise_logs {
    uuid id PK "UUID"
    uuid user_id FK
    timestamp created_at
    timestamp updated_at
  }
```
