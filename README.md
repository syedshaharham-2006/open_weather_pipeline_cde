# Airflow-OpenWeather-Pipeline

## Overview
This project provides an automated **ETL pipeline** using **Apache Airflow** to collect, process, and store weather data from the **OpenWeather API**.  
The workflow runs on a scheduled basis, supports **Dockerized deployment**, and can integrate with cloud storage or database backends for persistent data storage.

---

## Features
- Scheduled extraction of weather data from **OpenWeather API**
- Data cleaning and transformation using **Python scripts**
- Automated loading to **cloud storage** (e.g., AWS S3) or a **relational database** (Snowflake, RDS, etc.)
- **Task orchestration**, monitoring, and retry logic using Apache Airflow
- **Dockerfile** for containerized setup

---

## Setup and Installation

### 1. Clone the repository
```bash
git clone https://github.com/ayanhussain81/Airflow-OpenWeather-Pipeline.git](https://github.com/syedshaharham-2006/open_weather_pipeline_cde
cd open_weather_pipeline_cde
```

---

### Directory

├── dags/
│ └── openweather_dag.py
├── scripts/
│ ├── extract.py
│ ├── transform.py
│ └── load.py
├── Dockerfile
├── requirements.txt
└── README.md

---

### 2. Set your OpenWeather API Key
Create a `.env` file in the root directory:

```bash
OPENWEATHER_API_KEY=your_api_key
```

---

### 3. Install dependencies
pip install -r requirements.txt

---

### 4. Initialize Airflow

```bash
airflow db init
```

---

### 5. Start Airflow Scheduler and Webserver

```bash
airflow scheduler
airflow webserver --port 8080
```

---

### 6. Access Airflow UI
Open your browser and go to:

```bash
👉 http://localhost:8080
```

---

### 7. Trigger the DAG
You can start the DAG manually via Airflow UI or CLI.

### 🔧 Configuration

API keys, cloud/database credentials, and location settings can be updated in the .env file or via Airflow Connections.

Choose which cities or regions to collect data for inside the DAG configuration.

### 🔁 Pipeline Steps

Extract: Collect weather data from OpenWeather API on a schedule

Transform: Clean and standardize the weather data

Load: Save processed data to cloud or database

Notify / Monitor: (Optional) Send alerts or email notifications

