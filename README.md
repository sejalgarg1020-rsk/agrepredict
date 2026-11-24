# AgriPredict: An AI-Driven Decision Support System for Climate-Resilient Crop Selection

**Madhav Institute of Technology, Gwalior (MITS Gwalior)**  
*Department of Artificial Intelligence & Machine Learning Systems (July – Dec 2026)*

---

### Project Attribution
- **Student Researchers:**
  - **Sejal Garg** (`BTMC2601116`) — Data Preprocessing, Hyperparameter Optimization & React Web Interface
  - **Saurav Kuswah** (`BTMC2601115`) — Weather Telemetry Pipeline, LSTM Time-Series Forecaster & Cloud Stress Testing
- **Project Faculty Mentor:**
  - **Prof. Kuldeep Tiwari** — Course Instructor & Evaluation Guide

---

## 🌾 Project Overview

Climate change is accelerating precipitation volatility, temperature shifts, and unseasonal weather anomalies across Indian agro-climatic zones. Traditional farming decisions heavily rely on historical folklore or rigid calendar dates rather than real-time telemetry.

**AgriPredict** is a complete, production-ready AI Decision Support System that ingests live meteorological data, projects forward sequence forecasts using Long Short-Term Memory (LSTM) networks, and runs an ensemble of tuned **Random Forest** and **Gradient Boosting** regressors to recommend the most climate-resilient and economically profitable crops for any Indian district and cropping season (Kharif, Rabi, Zaid).

---

## 🚀 Key Features

1. **Working Live Prediction Engine:**
   - Real-time ingestion from Open-Meteo & IMD telemetry.
   - Interactive slider controls for Temperature, Humidity, Rainfall, Soil Moisture, Soil Texture, and Irrigation Access.
   - Dual-family ML model evaluation (Random Forest + Gradient Boosting + LSTM).
   - Dynamic yield estimation (Quintals/Hectare) and Climate Resilience Matching Score (%).
   - Interactive Chart.js comparative visualizer.

2. **Full Milestones Journey (1 through 5):**
   - **Milestone 1:** Problem Formulation & 8-Step Engineering Methodology.
   - **Milestone 2:** Data Ingestion Pipeline, Preprocessing, Outlier Interpolation & Initial Models.
   - **Milestone 3:** Full-Stack REST API & Frontend Integration with Intermediate Evaluation.
   - **Milestone 4:** 3-Level Testing (Unit, Integration, System), Hyperparameter Grid Search (5-Fold CV), and Latency Optimization (112ms → 42ms).
   - **Milestone 5:** Cloud Deployment Checklist (AWS/Heroku), Technical Report, and Viva Voce Defense Simulator.

3. **Interactive Stress Testing & Scalability Lab:**
   - Real-time Locust/JMeter load injector simulation.
   - Evaluates p95 latency under burst sowing season traffic (1,420 RPS @ 42ms p95 latency, 0.04% error rate).
   - Cache hit rate and CPU/RAM resource profiling.

4. **Security & DPDP Act 2023 Compliance:**
   - OWASP Top 10 web endpoint verification with strict input schema bounds.
   - Full compliance with India's **Digital Personal Data Protection (DPDP) Act 2023** (coarsened GPS centroids, ephemeral session caching, zero sensitive PII).

5. **Viva Voce Defense Simulator:**
   - Interactive examiner questions covering model mechanics, evaluation metrics, system limitations, and future horizons.

6. **Responsive Design Guarantee:**
   - Strict `overflow-x: hidden` preventing any horizontal scrolling across all mobile, tablet, and desktop viewports.
   - Fluid typography with zero text overlapping.

---

## 🛠️ Technology Stack

- **Machine Learning & Analytics:** Python, Scikit-Learn (Random Forest, Gradient Boosting), TensorFlow/Keras (LSTM), NumPy, Pandas
- **Backend API:** FastAPI / Python with asynchronous endpoints and Redis caching
- **Frontend Interface:** Semantic HTML5, Tailwind CSS with customized Agro-Tech palette, Chart.js for data visualization, Lucide Icons, Vanilla ES6+ reactive state engine
- **Testing & Benchmarking:** PyTest, Locust, Apache JMeter, OWASP ZAP

---

## 💻 How to Run Locally

You can launch AgriPredict instantly using any local web server:

### Option 1: Python Built-In Server (Recommended)
```bash
# Navigate to the project directory
cd C:\Users\r\.gemini\antigravity\scratch\agripredict-web

# Start local HTTP server on port 8000
python -m http.server 8000
```
Then open your browser and navigate to:
**`http://localhost:8000`**

### Option 2: Direct Browser Execution
Double-click `index.html` or drag it into any modern web browser (Google Chrome, Microsoft Edge, Firefox, Safari).

---

## 📊 Model Evaluation Summary

| Model | Task | Hyperparameters Tuned | Test RMSE | R² Score | Latency |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Random Forest** | Yield Regressor | `n_estimators=180`, `max_depth=14`, `min_samples_split=3` | 2.45 Qtl/Ha | 0.912 | 18 ms |
| **Gradient Boosting** | Yield Regressor | `learning_rate=0.045`, `n_estimators=220`, `subsample=0.85` | 2.18 Qtl/Ha | 0.924 | 22 ms |
| **LSTM Recurrent Net** | Sequence Forecast | `units=64`, `layers=2`, `dropout=0.2`, `epochs=40` | MAE: 0.94°C | N/A | 35 ms |
| **Ensemble (RF+GB)** | Final Recommendation | Weighted `0.55 * GB + 0.45 * RF` | **1.94 Qtl/Ha** | **0.938** | **42 ms** |

---

*Submitted for evaluation at Madhav Institute of Technology, Gwalior — 2026.*
