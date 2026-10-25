# Automotive Engine Remaining Useful Life (RUL) Prediction

A Deep Learning and predictive maintenance framework designed to forecast the **Remaining Useful Life (RUL)** of automotive engines using multi-sensor time-series telemetry data.

## 📌 Features & Highlights
- **Multi-Sensor Telemetry:** Simulates real-world engine degradation using 6 key parameters: Oil Pressure, Engine Temperature, Vibration, RPM Deviation, Fuel Flow, and Exhaust Temperature.
- **Time-Series Sequence Data:** Formats sensor logs into temporal sequences ($seq\_len = 30$ cycles) for sequential model training (LSTM / GRU / Transformer).
- **Target Normalization:** Normalizes RUL targets to $[0, 1]$ range for optimal neural network convergence and accurate life-cycle estimation.

## 📊 Dataset & Sensor Parameters
| Sensor Name | Initial Baseline | Degradation Behavior | Unit / Metric |
| :--- | :--- | :--- | :--- |
| **Oil Pressure** | 4.0 bar | Non-linear decrease over time | Pressure (bar) |
| **Engine Temp** | 90.0 °C | Exponential increase under stress | Temperature (°C) |
| **Vibration** | 0.1 g | Gradual wear-and-tear increase | Acceleration ($g$) |
| **RPM Deviation** | 5.0 RPM | Rapid fluctuation growth | Deviation |
| **Fuel Flow** | 8.0 L/h | Increasing consumption efficiency drop | Rate (L/h) |
| **Exhaust Temp** | 300.0 °C | Thermal elevation | Temperature (°C) |

## 🛠️ Tech Stack
- **Languages:** Python
- **Data & Numeric Processing:** NumPy, Pandas, Scikit-Learn
- **Deep Learning & Modeling:** PyTorch / TensorFlow, Keras
- **Environment:** Google Colab / Jupyter Notebook
