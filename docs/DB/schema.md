# Database Schema

## User
- id (int, PK)
- name (string)
- email (string, unique)

## NetworkFlow
- id (int, PK)
- src_ip (string)
- dest_ip (string)
- protocol (string)
- timestamp (datetime)

## Prediction
- id (int, PK)
- flow_id (int, FK -> NetworkFlow.id)
- user_id (int, FK -> User.id)
- anomaly_score (float)
- predicted_at (datetime)
