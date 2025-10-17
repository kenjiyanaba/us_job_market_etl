U.S. Job Market ETL & Analytics Dashboard

An end-to-end Data Engineering & Analytics project that collects, cleans, and visualizes job market data from the [Adzuna API](https://developer.adzuna.com/).  
The pipeline simulates a real-world ETL (Extract, Transform, Load) process — from raw data ingestion to interactive visualization — using Python, Pandas, and Streamlit.

---

Project Overview

This project demonstrates the full data pipeline lifecycle:

1. Extract — Pull real-time job listings from the Adzuna API.
2. Transform — Clean and normalize the data using Pandas.
3. Load — Save processed data into structured CSV files (can be extended to databases like PostgreSQL or SQLite).
4. Visualize — Explore job trends interactively in a Streamlit dashboard.

The dashboard lets users explore:
- Top companies hiring  
- Most common job titles  
- Job distribution by state  
- Salary distributions across roles  

---

## Architecture

Adzuna API → 
Extract (Python Requests)

↓
Transform (Pandas)

↓
Load (CSV)

↓
Visualize (Streamlit Dashboard)

---

## Tech Stack

| Layer | Tools Used |
|-------|-------------|
| Language | Python 3.10 |
| Data Extraction | `requests`, `.env` for secure API key storage |
| Data Transformation | `pandas`, `numpy` |
| Visualization | `streamlit`, `plotly` |
| Storage | CSV (local), easily extendable to SQL |
| Version Control | Git + GitHub |

---

## Setup Instructions

1. Clone the repository
git clone https://github.com/kenjiyanaba/us_job_market_etl.git
cd us_job_market_etl

3. Set up a virtual environment
python3 -m venv venv
source venv/bin/activate   # (Mac/Linux)
venv\Scripts\activate      # (Windows)

4. Install dependencies
pip install -r requirements.txt

5. Add your API credentials
Create a .env file in the project root:

ADZUNA_APP_ID=your_app_id
ADZUNA_APP_KEY=your_app_key

5. Run the ETL pipeline
python etl/extract_jobs.py
python etl/transform_jobs.py
python etl/verify_data.py

6. Launch the Streamlit dashboard
streamlit run dashboard.py
Then open your browser to http://localhost:8501
