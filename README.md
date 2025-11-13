# Airflow-OpenWeather-Pipeline

## 🌦️ Overview
This project provides an automated **ETL pipeline** using **Apache Airflow** to collect, process, and store weather data from the **OpenWeather API**.  
The workflow runs on a scheduled basis, supports **Dockerized deployment**, and can integrate with cloud storage or database backends for persistent data storage.

---

## 🚀 Features
- Scheduled extraction of weather data from **OpenWeather API**
- Data cleaning and transformation using **Python scripts**
- Automated loading to **cloud storage** (e.g., AWS S3) or a **relational database** (Snowflake, RDS, etc.)
- **Task orchestration**, monitoring, and retry logic using Apache Airflow
- **Dockerfile** for containerized setup

---

## ⚙️ Setup and Installation

### 1. Clone the repository
```bash
git clone https://github.com/ayanhussain81/Airflow-OpenWeather-Pipeline.git
