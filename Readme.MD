# ✈️ Airline Data Pipeline: Real-Time Flight Analysis

A fully open-source data pipeline project that fetches real-time airline and flight data via a free API, stores it in a PostgreSQL database, transforms it with Python, and visualizes insights using Power BI.

## 📌 Project Overview

This project demonstrates an end-to-end data pipeline using only free tools. It tracks airline flight status, delays, and performance over time using real-time API data and presents actionable insights through interactive dashboards.

## 🧱 Tech Stack

| Component       | Tool/Service               |
|----------------|----------------------------|
| Data Source     | AeroDataBox API (RapidAPI) / OpenSky Network |
| Ingestion       | Python (`requests`, `schedule`) |
| Storage         | PostgreSQL + pgAdmin      |
| Transformation  | Python + SQL              |
| Visualization   | Power BI Desktop          |
| Scheduling      | `cron` or `schedule` module in Python |

## 🗂️ Project Structure

```
.
├── data_ingestion/
│   └── fetch_flight_data.py
├── db/
│   └── schema.sql
├── raw_data/
│   └── flight_data_2025_06_17.json
├── dashboards/
│   └── flight_analysis.pbix
├── README.md
```

## 🚀 How It Works

1. **Fetch real-time flight data** from a free API (e.g., AeroDataBox).
2. **Store the data** in a local PostgreSQL database.
3. **Transform and clean** the data using Python and SQL.
4. **Visualize key metrics** in Power BI:
   - Average flight delay by airline
   - Most delayed routes
   - On-time performance by airport
   - Live snapshot of flight statuses (optional)

## 📊 Dashboard

> 

## ⚙️ Getting Started

### Prerequisites
- Python 3.9+
- PostgreSQL + pgAdmin
- Power BI Desktop (Windows)
- RapidAPI account (for AeroDataBox key)

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/airline-data-pipeline.git
cd airline-data-pipeline
```

### 2. Install Python dependencies
```bash
pip install -r requirements.txt
```

### 3. Set up the database
Run the schema file:
```sql
psql -U postgres -f db/schema.sql
```

### 4. Run the ingestion script
```bash
python data_ingestion/fetch_flight_data.py
```

### 5. Open the Power BI report
- Navigate to `dashboards/flight_analysis.pbix`
- Update data source if needed (PostgreSQL connection)


## 📄 License

This project is licensed under the [MIT License](LICENSE).

## 🙌 Acknowledgements

- [AeroDataBox](https://rapidapi.com/aedbx-aedbx/api/aerodatabox/)
- [OpenSky Network](https://opensky-network.org/)
- [Power BI](https://powerbi.microsoft.com/)