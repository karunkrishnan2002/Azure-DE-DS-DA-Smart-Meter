# ⚡ IoT Smart Meter Data Engineering Project

This project simulates a **real-time IoT Data Pipeline** for smart meters using **Azure Data Engineering + ML Lakehouse** architecture.  
It demonstrates how to ingest, process, transform, and analyze IoT telemetry data for **energy consumption forecasting**.

---

## 🚀 Architecture Overview

🔹 IoT Smart Meter → Azure IoT Central  
🔹 IoT Hub (Event Hub-compatible) → Azure Event Hub (Basic Tier)  
🔹 Stream Ingestion → Azure Databricks (Structured Streaming)  
🔹 Bronze → Silver → Gold Lakehouse Architecture  
🔹 ML Forecasting (LightGBM) → Azure Synapse + Power BI for analytics  

![Architecture Diagram](diagrams/IoT_Smart_Meter_Flow.png)

---

## 📂 Repo Structure

- **data/** → Sample IoT data (raw & processed)  
- **notebooks/** → Jupyter notebooks (ingestion, transformation, ML)  
- **src/** → Python scripts for ingestion, transformation & ML  
- **diagrams/** → Flowcharts & architecture diagrams  

---

## ⚙️ Tech Stack

- **Cloud**: Azure IoT Central, Event Hub, Databricks, Data Lake Gen2, Synapse  
- **Streaming**: PySpark Structured Streaming  
- **Storage**: Delta Lake (Bronze, Silver, Gold)  
- **Machine Learning**: LightGBM (Forecasting UsageKWh)  
- **Visualization**: Power BI / Synapse SQL  

---

## 📊 Dataset Schema

Sample IoT Telemetry (JSON):

```json
{
  "DeviceId": "meter-001",
  "Timestamp": "2025-09-01T10:15:00Z",
  "UsageKWh": 5.6,
  "Voltage": 230.5,
  "Current": 12.4,
  "Location": {
    "City": "Bangalore",
    "Region": "KA"
  }
}
