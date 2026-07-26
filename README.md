# 🌫️ Air Quality Index (AQI) Monitor & Safe Route Planner

A comprehensive, full-stack Air Quality Monitoring and Safe Route Navigation platform built for environmental awareness, health advisory, and real-time AQI forecasting.

---

## 🚀 Features

- **📊 Real-time AQI Dashboard**: Interactive visualization of current Air Quality Index, weather metrics, and major pollutants ($PM_{2.5}$, $PM_{10}$, $NO_2$, $SO_2$, $O_3$, $CO$).
- **🗺️ Interactive Map & Safe Navigation**: Integrated Leaflet map visualization coupled with GraphHopper OSM routing for calculating safer pathways based on air pollution intensity.
- **📈 Historical Analytics & Forecasting**: Calendar heatmaps, annual trend analysis, and an **LSTM Deep Learning model** for multi-step AQI forecasting.
- **🏥 Personalized Health Advisory**: Custom profile setup, health risk score meter, symptom tracking, and tailored safety advice based on ambient AQI levels.
- **🤖 Machine Learning Core**: Python-powered ML pipeline for AQI forecasting, feature scaling, and pollution source estimation.

---

## 🛠️ Tech Stack

### **Frontend**
- **Framework**: React 18 + Vite
- **Styling**: Tailwind CSS, Framer Motion
- **Data Visualization**: Recharts, Leaflet / React-Leaflet
- **Icons**: Lucide React

### **Backend**
- **Framework**: Java 17, Spring Boot 3.2
- **Database**: PostgreSQL / Spring Data JPA
- **Routing Engine**: GraphHopper Core & OSM Reader

### **Machine Learning Core**
- **Models**: TensorFlow / Keras (LSTM Forecaster), Scikit-Learn (Ensemble models & Source Estimators)
- **Data Utilities**: Joblib, Pandas, NumPy

---

## 📁 Project Structure

```
├── src/                        # React Frontend & Spring Boot Backend Source
│   ├── components/             # React Dashboard Components (Maps, Charts, Advisory)
│   ├── context/                # React State Contexts (Theme, Health Profile)
│   ├── main/java/com/aqi/      # Spring Boot Controllers, Models & Services
│   └── main/resources/         # Spring Configuration & Static Assets
├── ml_core/                    # Machine Learning Training Scripts & Models (.pkl, .keras, .joblib)
├── public/                     # Static Web Pages & Assets
├── osm/                        # OpenStreetMap Data (.osm.pbf) for GraphHopper
├── pom.xml                     # Maven Build Configuration (Frontend + Backend)
└── package.json                # React Frontend Dependencies
```

---

## 🚦 Getting Started

### Prerequisites
- **Node.js** (v18+)
- **Java Development Kit (JDK 17+)**
- **Python 3.10+** (for ML Core)
- **Maven** (Optional, bundled via wrapper/frontend-maven-plugin)

---

### Running the Frontend (Development)

```bash
# 1. Install dependencies
npm install

# 2. Start Vite development server
npm run dev
```

The application will be available at `http://localhost:5173`.

---

### Building & Running the Full-Stack Application

```bash
# Build Vite frontend and Spring Boot JAR together
mvn clean package

# Run the Spring Boot application
java -jar target/aqi-monitor-dashboard-1.0-SNAPSHOT.jar
```

---

### Running ML Core Scripts

```bash
cd ml_core

# Run source estimator verification
python verify_source_model.py

# Train LSTM forecaster model
python lstm_aqi_forecaster.py
```

---

## 📜 License

This project was developed for Makeathon. Shared under the MIT License.
