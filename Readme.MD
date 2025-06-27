# ✈️ Airline Data Pipeline: Real-Time Flight Analysis

A fully open-source data pipeline project that fetches real-time airline and flight data via a free API, stores it in a PostgreSQL database, transforms it with Python, and visualizes insights using Power BI.

## 📌 Project Overview

This project focuses on analyzing flights to Japan using new tools and techniques. The goal is to collect data from online sources (via web scraping or APIs), automate its collection on a scheduled basis, and generate insights such as customer satisfaction, delay estimations, and pricing fluctuations. It uses Airtable and Zapier to integrate and automate parts of the pipeline, with Power BI for interactive visualization. PostgreSQL may be used optionally for structured data storage.

Key goals:
- Explore new tools: Airtable, Zapier, Power BI
- Focus on flights bound for Japan
- Automate data collection and integration
- Extract insights about airline operations and performance

## 🧱 Tech Stack

| Component         | Tool/Service                         |
|-------------------|--------------------------------------|
| Data Scraping     | AeroDataBox, OpenSky, Google Flights |
| Automation        | Zapier, Python                       |
| Storage           | Airtable                             |
| Transformation    | Python, SQL                          |
| Visualization     | Power BI Desktop                     |

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

1. **Collect flight data** using free APIs or scrape online sources like Google Flights.
2. **Schedule automatic pulls** using Zapier or Python.
3. **Store and manage data** in Airtable (or PostgreSQL if needed).
4. **Transform data** to calculate delay trends, pricing fluctuations, and satisfaction patterns.
5. **Visualize results** using Power BI with dashboards like:
   - Flight price trends by region
   - Delay patterns by airline
   - Popular routes to Japan
   - Correlation between booking time and delays or pricing

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