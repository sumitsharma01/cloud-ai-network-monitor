# API Design for Anomaly Detection System

This document describes the planned REST API endpoints for the Anomaly Detection system.  
It serves as a low-level design specification before implementation.

---

## Base URL
http://localhost:8000/api

*(This will change when deployed)*

---

## Endpoints

### 1. Predict Anomaly
**Description:**  
Submit a network flow or feature data to get anomaly predictions from the trained model.

| Method | URL             | Auth Required | Description                  |
|--------|-----------------|---------------|------------------------------|
| POST   | /predict        | No            | Get anomaly prediction       |

**Request Body (JSON):**
```json
{
  "feature1": "value1",
  "feature2": "value2",
  "feature3": "value3",
  "...": "..."
}
```

**Response (JSON):**
```json
{
  "prediction": "anomaly",
  "confidence_score": 0.92
}
```

**Error Responses:**
- 400 Bad Request – Invalid input data
- 500 Internal Server Error – Server error or model not loaded

### 2. Get Model Info
**Description:**  
Retrieve metadata about the deployed model (version, features, training info).

| Method | URL          | Auth Required | Description            |
|--------|--------------|---------------|------------------------|
| GET    | /model-info  | No            | Get model metadata     |

**Response (JSON):**
```json
{
  "model_name": "AnomalyDetectionModel",
  "version": "1.0.0",
  "features": ["feature1", "feature2", "feature3", "..."],
  "training_dataset": "UNSW-NB15"
}
```

**Error Responses:**
- 500 Internal Server Error – Server error or model metadata unavailable

### Future Endpoints
- `/retrain` – Endpoint to retrain the model with new data
- `/metrics` – Endpoint to fetch performance metrics or logs
- `/dashboard-data` – Endpoint to provide summarized data for frontend

## Notes
- All requests and responses will use JSON format.
- Error handling should follow standard HTTP codes.
- Authentication may be added in future iterations (e.g., API keys, JWT).
- This API is designed to work with a microservices architecture.

**Document last updated:** 2025-08-13