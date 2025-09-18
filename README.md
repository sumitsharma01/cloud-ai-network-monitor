# Cloud AI Network Monitor

## Project Vision
Build a cloud-native, event-driven network monitoring platform leveraging AI/ML for real-time anomaly detection and incident response.  
Utilises microservices, containerization, secure APIs, and React dashboard. Demonstrates Agile best practices, CI/CD, and cloud architecture.

## Tech Stack
- Python (FastAPI) for backend microservices.  
- PyTorch/TensorFlow for anomaly detection.  
- Kafka for event streaming.  
- PostgreSQL for incident data.  
- React.js for the frontend dashboard.  
- Docker & Kubernetes for containerization. 
- GitHub Actions for CI/CD.

## Dataset: UNSW-NB15

This project uses the UNSW-NB15 dataset, a modern benchmark dataset for network intrusion detection research. It was created by the Australian Centre for Cyber Security (ACCS) in 2015 using the IXIA PerfectStorm tool to generate hybrid real and synthetic network traffic.

### Dataset Highlights
- **Size**: ~2.5 million records across training and test sets.
- **Features**: 49 total (numeric & categorical), including flow characteristics, content-based features, and time-based features.
- **Classes**:
  - Normal traffic
  - Attack traffic grouped into 9 categories:
    - Fuzzers
    - Analysis
    - Backdoors
    - DoS (Denial of Service)
    - Exploits
    - Generic
    - Reconnaissance
    - Shellcode
    - Worms
### File Structure
- `UNSW-NB15_1.csv` – `UNSW-NB15_4.csv`: Raw packet-based datasets (100k records each).
- `UNSW_NB15_training-set.csv`: 175,341 records for training.
- `UNSW_NB15_testing-set.csv`: 82,332 records for testing.

### Why This Dataset?
- Realistic simulation of modern cyber-attacks and normal network behaviour.
- Widely used in intrusion detection and anomaly detection research.
- Supports both supervised (classification) and unsupervised (anomaly detection) approaches.
  
### Source
The dataset is publicly available via the [UNSW-NB15 Official Page](https://research.unsw.edu.au/projects/unsw-nb15-dataset).
