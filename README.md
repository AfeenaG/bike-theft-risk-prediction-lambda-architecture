# 📌 Project Overview

Designed and implemented a scalable end-to-end data pipeline to predict bike theft risk in Toronto using Lambda Architecture.
# Project Structure

```text
bike-theft-risk-prediction-lambda-architecture
│
├── README.md
├── Conde_Snippets
│   └── MongoDB_Live_stream_record_count.png
│   └── MongoDB_query1_return_1_row_partC.png
│   └── MongoDB_query1_return_1_row_partB.png
│   └── MongoDB_query1_return_1_row_partA.png
│   └── Parquet_folder_path.png
│   └── Parquet_write.png
│   └── ML_ModelB.png
│   └── ML_ModelA.png
│   └── Stream_setup.png
│   └── MongoDB_write.png
├── Images
│   └── App1.png
│   └── App2.png
│   └── BikeThefts.png
│   └── Big_Data_Pipeline_Writeup.png
│   └── Theft by the hour of day.png
│   └── Thefts by Location Type at Night.png
│   └── Thefts by time of day.png
├── Notebooks
│   ├── Random Forest Stream to Mongo.ipynb
│   ├── DataCleaning_final.ipynb
│   ├── DataVisualization_RDMS.ipynb
│   ├── SyntheticStream_final.ipynb
└── report
    └──Predicting Bike Theft: A Case Study on Toronto Bicycle Theft.pdf
```

---
# Data Source	Toronto Open Data
📂 Dataset

Source: Toronto Open Data

Records: 39K → 31K after cleaning

Time Range: 1975–2025

This system combines:

# 📊 Batch analytics for historical insights

⚡ Real-time streaming for instant predictions

# 🤖 Machine learning for risk classification

➡️ Outcome: Enables data-driven policing strategies and a real-time risk prediction app for users

# 🎯 Business Impact
- Identified high-risk theft zones (Downtown waterfront, condos)
- Discovered peak theft window (nighttime)
- Highlighted misalignment in policing strategies
- Proposed targeted patrol optimization (6 PM – Midnight)


🏗️ Architecture (Lambda Design)

![Architecture](Images/Big_Data_Pipeline_Writeup.png)


🔹 Key Design
- Cold Path (Batch): Historical processing + model training
- Hot Path (Streaming): Real-time inference pipeline
- Serving Layer: MongoDB for fast access to predictions

# 📊 Data Visualizations

## 🕒 Theft by Time  of Day

![Theft By Time of Day](Images/Thefts%20by%20time%20of%20day.png)


## 🕒 Theft by Hour of Day

![Theft By Hour of Day](Images/Theft%20by%20the%20hour%20of%20day.png)

## 🏢 Theft by Location Type

![Theft By Location](Images/Thefts%20by%20Location%20Type%20at%20Night.png)

## 📍 Geographic Hotspots

![Theft By Geographic Hotspot](Images/BikeThefts.png)


⚙️ Tech Stack

| Category | Tools  | 
|---|---|
| Big Data | Apache Spark, PySpark | 
|Streaming | Spark Structured Streaming | 
|Machine Learning | Random Forest (pyspark ML) | 
|Databases |MongoDB (NoSQL), SQLite (RDBMS) | 
|Machine Learning | Random Forest (pyspark ML) | 
|Databases |MongoDB (NoSQL), SQLite (RDBMS)) | 
|Environment|	Ubuntu, Oracle VirtualBox | 
|Visualization libraries|	folium, matplotlib| 


# 🤖 Machine Learning

## Model Comparison


| Model | Accuracy | Issue | Status |
| :--- | :--- | :--- | :--- |
| Model A (with location) | 100% | Data Leakage | ❌ Rejected |
| Model B (no location) | 88.76% | Generalizable | ✅ Deployed |


## 🔍 Key Insight

- Perfect accuracy ≠ good model
  
➡️ Removing location features improved real-world reliability

🔄 Real-Time Simulation

# Simulation
To validate scalability, a clickstream simulator was built using PySpark:

- 25,000+ simulated user events
- Realistic behavioral patterns
- Time-based event generation
- Stress-tested streaming pipeline
  
# 🧠 Feature Engineering

📍 Neighborhood Risk Segmentation (Quantiles)

⏰ Temporal Feature Engineering (Time Buckets)

🚲 High-Cardinality Reduction (Top-N encoding)

⚡ Real-Time Risk Prediction API-ready pipeline


# 🚀 Why This Project Stands Out

✔ End-to-end pipeline (data → ML → streaming → serving)

✔ Real-world problem with actionable insights

✔ Handles both batch + real-time workloads

✔ Demonstrates data engineering + ML + analytics

✔ Addresses data leakage (advanced ML concept)

📸 Application Concept

![App 1](Images/mockups.png)


“Bike Guard” App

- Users input bike details and premise/location type
- Clicks on "Submit Assessment"
- System returns instant theft risk level
- Designed for simplicity + real-world usability

🧪 Key Learnings
- Data quality directly impacts ML performance
- Feature selection is critical for generalization
- Lambda Architecture enables scalable hybrid systems
- Real-time systems require trade-offs between latency and accuracy

👤 Author

Afeena Gafoor

Master’s in Business Analytics & AI

