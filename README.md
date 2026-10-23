# Project Setup
    
    To run this project, follow these steps:
    
    1. Extract the zip file.
    2. Run `npm install` to install dependencies.
    3. Run `npm run dev` to start the development server.
    
    This project was generated through Alpha. For more information, visit [dualite.dev](https://dualite.dev).

# 🌱 Smart Crop Prediction System

[![React](https://img.shields.io/badge/React-18.3-61DAFB?logo=react&logoColor=black)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-6.3-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Firebase](https://img.shields.io/badge/Firebase-Firestore-FFCA28?logo=firebase&logoColor=black)](https://firebase.google.com/)

An intelligent agricultural decision-support web application designed to help farmers and agronomists identify the most suitable crops for cultivation based on real-time climate telemetry, soil properties, and seasonal cycles.

---

## 📌 Overview

Traditional farming often relies on guesswork or outdated historical habits, leading to crop failure and financial losses. The **Smart Crop Prediction System** bridges this gap by combining live weather API data with an agricultural expert decision engine, providing data-driven crop recommendations, harvest schedules, and fertilizer guidance.

---

## ✨ Key Features

- **🌤️ Automated Weather Integration:** Auto-fetches live temperature, humidity, and atmospheric conditions using the OpenWeatherMap API.
- **🧪 Soil & Regional Intelligence:** Recommends benchmark topsoil pH levels across major agricultural zones and evaluates soil textures (Clay, Loam, Sandy Loam).
- **🧠 Multi-Criteria Prediction Engine:** Employs a weighted penalty scoring algorithm (evaluating soil, temperature, pH, and season) to calculate a 0–100% suitability score.
- **📅 4-Stage Cultivation Planning:** Generates an automated farming calendar (Land Preparation, Sowing, Growing & Maintenance, and Harvesting) with estimated dates.
- **🌾 Fertilizer Advisory:** Suggests optimal fertilizers (Urea, DAP, MOP, SSP) with application timings and estimated market prices.
- **📄 PDF Export:** Generates downloadable, print-friendly advisory reports using `jsPDF`.
- **🔐 Cloud Authentication & History:** Secure sign-in/sign-up powered by Firebase Auth, with past predictions saved to Cloud Firestore.
- **📊 Admin Portal:** Dedicated administrative dashboard to monitor platform usage, user counts, and system metrics.

---

## 🛠️ Tech Stack

- **Frontend:** React 18, Vite, Tailwind CSS, Framer Motion, Lucide Icons
- **Decision Engine:** Custom JavaScript Multi-Criteria Decision Analysis (MCDA) Rule Engine
- **Database & Auth:** Google Cloud Firestore (NoSQL), Firebase Authentication
- **External APIs:** OpenWeatherMap API, YouTube Data API, SoilGrids API
- **Utilities:** Axios, jsPDF, Gh-Pages

---

## 📁 Project Structure

```text
Smart-Crop-Prediction/
├── public/                 # Static assets
├── scripts/                # Standalone test & demo scripts
├── src/
│   ├── components/         # UI screens (Home, Dashboard, Login, Modals)
│   ├── config/             # Firebase SDK setup
│   ├── context/            # Global Auth & State Context
│   ├── data/               # Agricultural datasets (crops, fertilizers, city pH)
│   ├── services/           # Prediction algorithm, Weather & PDF services
│   ├── App.jsx             # Main router & layout controller
│   └── main.jsx            # Application entry point
├── .env.example            # Sample environment variables
├── index.html              # HTML shell
├── package.json            # Project dependencies & scripts
├── tailwind.config.js      # Tailwind CSS configuration
└── vite.config.ts          # Vite bundler configuration
