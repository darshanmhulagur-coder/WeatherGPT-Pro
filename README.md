# WeatherGPT — Multilingual Conversational AI for Weather Forecasting, Alerts & Climate Intelligence
### Smart India Hackathon (SIH Problem Statement: SIH26068)

---

## 🌟 Executive Overview
**WeatherGPT** is a production-grade, AI-driven meteorological intelligence platform engineered for pan-India coverage across all **28 States, 8 Union Territories, and ~800 Districts**. It unites real-time sensor fusion (IMD radar, INSAT-3DR geostationary satellite telemetry, and ECMWF numerical models), predictive physics-guided AI forecasting, route-based logistics risk modeling, crop & pest advisory systems, and a **Voice + Text Multilingual Conversational AI Agent**.

---

## 🌦️ Key Functional Modules & Features

### 1. Top Navigation & State/District Search Controls
- **SIH26068 Micro-Badge**: Dedicated problem statement badge with glowing neon accents.
- **Cascading State & District Selector**: Covers all 28 States, 8 UTs, and every Indian district with instant reactive state binding.
- **Universal Search Bar**: Autocomplete search supporting Indian cities, district names, and 6-digit Indian postal Pincodes.
- **Multilingual Support (6 Languages)**: Instant, zero-reload full-UI translation across:
  - English (`en`)
  - Kannada (`kn` - ಕನ್ನಡ)
  - Hindi (`hi` - हिंदी)
  - Telugu (`te` - తెలుగు)
  - Tamil (`ta` - தமிழ்)
  - Marathi (`mr` - मराठी)
- **Emergency Broadcast Marquee**: Real-time ticker for flash floods, cyclone watches, and river basin warnings.
- **Metric / Imperial Unit Toggle**: Instant switch between Celsius (°C) and Fahrenheit (°F).

### 2. Modern Hero Stage & Multilingual Audio Weather Bulletin
- **Live Microclimate Panel**: Real-time temperature, "Feels Like", Conditions, High/Low spans, and local network time sync.
- **🎙️ 1-Minute Daily Audio Bulletin**: 
  - Integrated speech engine powered by Web Speech API (`SpeechSynthesis`) with localized regional pronunciation tags (`kn-IN`, `hi-IN`, `te-IN`, `ta-IN`, `mr-IN`, `en-IN`).
  - Realistic audio chime on start and real-time animated audio equalizer / soundwave bars during broadcast.
- **📄 Official Print / PDF Advisory**: 1-click printable district weather report tailored for farmers, local gram panchayats, and logistics operators.
- **🚨 Severe Weather Nowcast Alerts**: Dynamic warnings triggering when precipitation risk > 65%, extreme heat > 38°C, or high gale winds > 35 km/h occur.

### 3. Hourly (24h) Interactive Timeline & Scrubbing Curve
- Interactive hourly timeline scrubber with smooth temperature curve, humidity, and condition simulation on hover.
- Time-travel scrubbing mode dynamically updates the hero stage's 3D weather glyph and metrics for any hour of the day.

### 4. 2x2 Microclimate Metric Grid
- **CPCB-Calibrated National Air Quality Index (NAQI)** with pollutant breakdowns (PM2.5, PM10, NO2, SO2, CO, O3) and health advisories.
- **Wind Compass**: Live compass bearing, wind velocity in km/h, and Beaufort scale status.
- **Atmospheric Pressure & Humidity Gauge**: Dew point and barometric trend indicator.
- **UV Index Meter**: Peak midday exposure advisory and sun protection alerts.

### 5. Dual-Engine Forecast Center: Synoptic Day Cards & Chart.js Curves
- **Dual View Mode Toggle**: Switch between **7-Day Synoptic Day Cards** (with min/max range sliders) and **Interactive Trend Charts** (Chart.js).
- **Interactive Metrics**: Toggle between:
  - Temperature Trend (°C / °F)
  - Precipitation Probability Curve (%)
  - Cloud Cover Saturation (%)

### 6. Sector-Specific Meteorological Intelligence (Tabbed Architecture)
- 🌾 **Agriculture & Farmers**: Root-zone soil moisture (0-30cm), Evapotranspiration (ET₀ mm/day), precision irrigation advisories, and an **AI Pest & Disease Alert Engine** (calculating fungal blast, downy mildew, and brown plant hopper risks with preventative fungicide prescriptions).
- 🚚 **Logistics & Route Weather Planner**: Origin-to-destination transit analyzer plotting route milestones, ETAs, elevation gradients, and severe weather road hazards (Ghat fog, aquaplaning risk, gale winds).
- ⚡ **Renewable Energy**: Global Horizontal Irradiance (GHI kWh/m²), 10kW rooftop daily yield, wind power generation potential, turbine capacity factor, and optimal solar panel tilt angles.
- 🚨 **Disaster Management & Safe Shelters**: District flood vulnerability index score, CWC river basin telemetry, nearby designated emergency shelters with capacities and medical aid badges, plus one-tap emergency helpline dialers (NDRF 1078, District EOC 1077, 108 Ambulance, 101 Fire).

### 7. Interactive Radar & Climate Anomaly Map
- Leaflet-powered dark map centered on India with real-time district marker pins.
- **Dynamic Layer Toggles**: Precipitation Radar, Temperature Heatmap, and Air Quality (AQI) zones.
- **Time Slider Playback**: -2 hours historical to +2 hours nowcast precipitation movement with automatic play/pause loop.
- **Crowdsourced "Weather Spotter"**: 1-tap local ground-truthing widget boosting model confidence score.

### 8. Multilingual WeatherGPT AI Agent (Text + Voice Chat)
- Native Web Speech API integration (`SpeechRecognition` / `webkitSpeechRecognition`) supporting regional language tags:
  - `kn-IN`, `hi-IN`, `te-IN`, `ta-IN`, `mr-IN`, `en-US`.
- Speech output toggle (`window.speechSynthesis`) to speak answers back automatically.
- Seasonal Analysis & Predictive Reasoning (monsoon tracks, humidity thresholds, rainfall onset times).
- **Explainable RAG (XAI) Pipeline Accordion**:
  - Step 1: Semantic Parsing & Named Entity Recognition (NER)
  - Step 2: Vector DB IMD & ECMWF Agro-bulletin Search
  - Step 3: INSAT-3DR Rapid-Scan Satellite & Radar Fusion
  - Step 4: Physics-Guided Microclimate Neural Inference
  - Displays citations, source references, and confidence percentage.

### 9. Progressive Web App (PWA) & Offline Resilience
- Service worker with stale-while-revalidate caching (`sw.js`).
- Web App Manifest (`manifest.json`) for desktop and mobile installation.
- LocalStorage caching ensuring last retrieved district weather metrics remain accessible during storm connectivity drops.

---

## 🛠️ Technology Stack
- **Framework**: React 18 (Vite SPA)
- **Styling**: Tailwind CSS with custom Glassmorphism design system (`#0b0f19` dark canvas, slate-800 glass panels, cyan/amber/emerald/violet neon glows)
- **Icons**: Lucide Icons
- **Data Visualization**: Chart.js & React-Chartjs-2
- **Mapping**: Leaflet with CartoDB Dark Matter tiles & animated radar overlays
- **Speech Technologies**: Native Web Speech API (`SpeechRecognition` & `SpeechSynthesis`)
- **Particle Engine**: Custom HTML5 Canvas physics engine

---

## 🚀 Running the Application Locally

```bash
# 1. Install dependencies
npm install

# 2. Start Vite development server
npm run dev
# The application will be live at http://localhost:3000

# 3. Production build
npm run build
```
