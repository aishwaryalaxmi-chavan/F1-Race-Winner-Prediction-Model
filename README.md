# 🏎️ F1-Race-Winner-Prediction-Model

## Overview

This project is a **Jupyter Notebook** that predicts the results of the **2025 Formula 1 Austrian Grand Prix** using real F1 timing data, weather forecasts, and machine learning models. It demonstrates a complete workflow—from data acquisition and feature engineering to model training, evaluation, and prediction.

---

## 🚀 Features

### 📡 Data Sources

- **FastF1**: Official F1 session data (lap times, sector times, telemetry)
- **OpenWeatherMap API**: Real-time weather forecasts at the Red Bull Ring
- **Manual Inputs**: Driver & constructor points, tyre strategies, recent qualifying data

### 🔧 Feature Engineering

- Aggregates sector/lap times
- Computes clean air race pace
- Integrates weather metrics: air temperature, rain probability
- Derives performance consistency, tyre degradation, and driver form

### Features Used
- Qualifying Time: The driver's qualifying lap time for the Grand Prix.
- Rain Probability: Probability of rain at race time, sourced from live weather data.
- Temperature: Forecasted temperature at race time.
- Team Performance Score: A normalized score based on each team's season points.
- Clean Air Race Pace(s): Average lap time for each driver when running in clean air.
- Driver Consistency: Standard deviation of lap times for each driver, measuring how consistent their pace is.
- Team Boost: A calculated multiplier reflecting the relative performance advantage of each team.
- Driver Points: Each driver's championship points as a measure of form and performance.
- Total Tyre Degradation: Aggregate tyre degradation for each driver, based on stint data and compound-specific degradation rates

### 🤖 Machine Learning

- **K-Nearest Neighbors (KNN)**: Best-performing model based on MAE
- **Gradient Boosting Regressor** and **Support Vector Regression (SVR)** as benchmarks
- Feature importance plots for model interpretability

---

## 📊 Predicted Race Results (KNN Model)
🥇 **P1:** NOR  
🥈 **P2:** PIA  
🥉 **P3:** VER 

*Example predicted race times (seconds):*

| Driver | Predicted Race Time|
|--------|--------------------|
| NOR    | 71.584765          |
| PIA    | 71.584765          |
| VER    | 71.774480          |

> ℹ️ **Note**: Although the model predicted Verstappen to finish P3 based on pace, he **Did Not Finish (DNF)** in the actual race due to the crash. This highlights one of the model's limitations: it does not account for race-day incidents such as crashes or retirements.


## ⚠️ Limitations

- **Manual Inputs**: Tyre strategy and driver form are manually entered and subjective
- **Race Chaos Ignored**: Crashes, safety cars, and penalties are not modeled
- **Limited Training Data**: Smaller dataset may limit generalization across tracks
- **Model Simplifications**: Does not simulate full race strategy (e.g., pit stops, ERS deployment)

---

## 🛠️ Customization

To apply this project to a different race:

- Update session IDs and data sources
- Input new qualifying results, tyre strategies, and weather forecasts
- Experiment with different machine learning models and features






