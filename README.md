# 🌾 AgriDecision-TN
**The Geotemporal Bio-Climatic Atlas**

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.0-green.svg)](https://flask.palletsprojects.com/)
[![React](https://img.shields.io/badge/React-18.2-blue.svg)](https://reactjs.org/)

---

## 📋 Overview

**AgriDecision-TN** is a multidimensional digital platform designed to support Tunisian smallholder farmers by digitalizing intangible agrarian heritage. In an era of rapid climate change, traditional planting calendars often fail due to **"Thermal Lag"**—the disconnect between historical wisdom and current bioclimatic realities.

This system bridges that gap using a **Geotemporal Bio-Climatic Atlas**. By combining the traditional **Tunisian Agrarian Calendar** (e.g., *Azara*, *Gharien*) with real-time meteorological data and a **Bayesian-Wilson Hybrid Engine**, AgriDecision-TN provides precise, location-specific prescriptive advice without requiring expensive hardware sensors.

---

## ✨ Key Features

### 🧠 Prescriptive Logic (The "Brain")
-   **Bayesian-Wilson Engine**: A hybrid probabilistic model that updates crop success rates based on historical outcomes and real-time weather anomalies.
-   **Thermal Lag Mitigation**: Detects shifts in planting windows by calculating Growing Degree Days (GDD) and comparing them to traditional period thresholds.

### 🌍 Geotemporal Atlas
-   **24 Governorates Covered**: From the humid North/West (Bizerte, Beja) to the arid South (Tataouine, Tozeur).
-   **Digitalized Heritage**: Maps 8 distinct traditional agricultural periods (e.g., *Smat*, *Qorra*) to modern ISO dates.

### 🛡️ Secure & Scalable Architecture
-   **Risk Heatmaps**: Visualizes potential drought, frost, or pest risks using an intuitive "Museum-Style" dashboard.
-   **Composite Resource Bundling**: Optimized for rural 3G networks to ensure fast load times in the field.
-   **State-Level Security**: JWT Authentication and RBAC (Role-Based Access Control) for administrative oversight.

---

## 🛠️ Technology Stack

The system follows a **Three-Tier Decoupled Architecture**:

-   **Frontend**: React 18 (Vite) with Axios Interceptors and Leaflet.js for geospatial mapping.
-   **Backend**: Python Flask RESTful API with extensive use of Marshmallow for validation.
-   **Database**: PostgreSQL with **PostGIS** extensions for geospatial data and complex multidimensional querying.
-   **External APIs**: Integration with **ECMWF (ERA5)** for GRIB2 weather data parsing and OpenWeatherMap for forecasts.
-   **Deployment**: Fully containerized using **Docker** for consistent staging and production environments.

---

## 🚀 Quick Start

### Prerequisites
-   Python 3.9+
-   Node.js 16+
-   Docker 

### Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt

# Configure Environment
cp ../.env.example .env
# Update .env with your specific secret keys

# Initialize Database & Simulation Data
python -c "from app import create_app; from models.base import db; from services.init_db import init_database; app = create_app(); app.app_context().push(); db.create_all(); init_database()"

python app.py
```

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

---

## 🌍 Supported Crops & Periods

**Crops:**
Wheat, Barley, Oats (Field Crops); Tomato, Potato, Pepper (Vegetables); Olive, Citrus, Almond, Date Palm (Perennials).

**Agrarian Periods:**
1.  **Liely (The White Nights)**: Jan 1 - Jan 20
2.  **Azara**: Jan 21 - Feb 15
3.  **Gharien**: Feb 16 - Mar 14
4.  **Hsoum**: Mar 15 - Mar 31
5.  *...and others covering the full bioclimatic year.*

---

## 👨‍💻 Authors & Academic Context

**Elaborated By:**
### Takwa Dalensi
*Major: Business Analytics | Minor: Information Technology*

**Supervisor:**
### Prof. Montassar Ben Messaoud

*This project was developed as the IT325 Final Project for the University of Tunis / Tunis Business School, Academic Year 2025/2026.*

---

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a Pull Request.  
For major changes, please open an issue first to discuss what you would like to change.

