# 🌊 Intelligent Fault Diagnosis for AUV Using Neural Networks

This repository contains the simulation and implementation of intelligent control, identification, and fault diagnosis for an **Autonomous Underwater Vehicle (AUV)** system using neural networks. The study focuses on building robust models to handle actuator and sensor faults in nonlinear dynamic environments.

## 🚢 System Overview

- **Platform:** 2-DOF planar AUV model
- **States:** Linear and angular position/velocity
- **Faults Simulated:**
  - Actuator faults (e.g. loss of effectiveness)
  - Sensor faults (e.g. bias and failure)
- **Objectives:**
  - Accurate system identification
  - Robust control using inverse models
  - Fault estimation via dedicated neural models

## 🧠 Methodology

### 🟩 Neural Models:

- **MLP-based Controller:** Generates control inputs using desired trajectories
- **MLP-based Identifier:** Learns the nonlinear forward dynamics
- **Fault Estimators:**
  - `T_A`: Estimates actuator faults
  - `T_S`: Estimates sensor faults
  - These models receive current states, estimated values, and errors as input

### 🔁 Workflow:

1. Generate normal AUV data via simulation
2. Train identifier and inverse controller networks
3. Simulate fault scenarios (sensor/actuator)
4. Use trained `T_A` and `T_S` models to detect & estimate faults in real time


## 🔧 Requirements

- Python 3.8+
- TensorFlow or PyTorch
- NumPy
- Matplotlib


## 📊 Sample Results

* ✅ Accurate tracking with MLP controller
* ⚠️ Faults in actuator/sensor cause system degradation
* 🛠️ `T_A` and `T_S` models successfully detect and estimate fault values
* 🔄 Real-time adaptation to fault scenarios with minimal loss in performance

## 🧑‍💻 Contributors

* **Ali Nezamivand Chegeni**
* Supervisor: Dr. Farzaneh Abdollahi
* Spring 1404 – Faculty of Electrical Engineering, AUT
