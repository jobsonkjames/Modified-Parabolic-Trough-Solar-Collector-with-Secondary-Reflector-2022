# Modified-Parabolic-Trough-Solar-Collector-with-Secondary-Reflector-2022

![Status](https://img.shields.io/badge/Status-Fabricated_+_Validated-success)
![Domain](https://img.shields.io/badge/Domain-Concentrating_Solar_Power-orange)
![Simulation](https://img.shields.io/badge/Simulation-Tonatiuh_MCRT-blue)
![ML](https://img.shields.io/badge/ML-ANN_Performance_Prediction-purple)
![Project](https://img.shields.io/badge/Type-B.Tech_Final_Year-green)
 
A B.Tech final year project on **performance optimisation of parabolic trough solar collectors** through systematic secondary reflector design. Combines **Tonatiuh Monte Carlo ray tracing simulation**, experimental fabrication and outdoor validation, and **ANN-based performance prediction**.
 
## Overview
 
Conventional parabolic trough collectors (PTCs) concentrate solar flux non-uniformly on the receiver tube — most flux hits the bottom circumference, leaving the top barely irradiated. This creates a severe circumferential temperature gradient that bends the absorber tube off the focal axis over time, increasing optical loss and eventually causing structural failure.
 
This project investigated whether a **secondary reflector** placed above the receiver — combined with downward repositioning of the tube — could homogenise the flux distribution and improve reliability. The work systematically evaluated 14 secondary reflector geometries through Monte Carlo simulation, fabricated the optimal design, and experimentally validated it.
 
Led as part of a 4-member team under the supervision of Dr. Baiju V., Assistant Professor, Department of Mechanical Engineering, TKM College of Engineering.
 
## Highlights
 
- **Tonatiuh Monte Carlo ray tracing**: 2 million rays per simulation, 14 secondary reflector geometries evaluated
- Identified **6-strip 144°** configuration as the optimal practical geometry
- **77.07% improvement in heat flux uniformity** vs conventional PTC
- Fabricated optimised secondary reflector and installed on the campus PTC test rig
- **Experimentally validated** against on-site weather station data over multiple days
- **ANN-based performance prediction** model trained on collected weather + performance data
- Identified data volume as primary constraint for ML accuracy — informs future work scope
 
## Methodology
 
1. Literature review on PTC modifications and receiver flux homogenisation
2. PTC sizing — 2.8 m aperture × 2.5 m length, 1 m focal length, 70° rim angle, 7 m² aperture area
3. SolidWorks modelling of 14 candidate secondary reflector geometries (2-strip to 100-strip approximations + parabola)
4. Tonatiuh Monte Carlo ray tracing — 2M rays per configuration
5. Receiver tube position study — above, at, and below focal axis
6. Selection of optimal configuration balancing manufacturability and optical performance
7. Fabrication of the 6-strip 144° secondary reflector
8. Multi-day outdoor experimentation at TKMCE campus with on-site weather station
9. ANN model training for heat gain prediction from meteorological inputs
 
## Simulation Gallery
 
## Simulation, Experimental Validation & ML Analysis

### Secondary Reflector Geometry Development

<img src="Reflector_models.png" width="900">

Fourteen secondary reflector geometries were systematically designed in SolidWorks, ranging from simple 2-strip approximations to near-parabolic 100-strip configurations. The study evaluated how reflector geometry affects circumferential solar flux redistribution on the receiver tube while balancing manufacturability and optical performance.

---

### Monte Carlo Ray Tracing Simulation

<img src="Ray_tracing_simulations.png" width="900">

Tonatiuh Monte Carlo ray tracing simulations were performed using 2 million rays per configuration to analyse optical behaviour across all reflector geometries. The simulations evaluated how effectively each design redirected solar radiation onto the upper receiver surface to reduce local hot spots and improve flux uniformity.

---

### Heat Flux Distribution Analysis

<img src="Flux_distributions.png" width="900">

Circumferential heat flux distributions were analysed for each reflector geometry. The optimised 6-strip 144° configuration produced the most uniform flux profile, significantly reducing concentrated local heat flux regions responsible for thermal stress and absorber tube deformation in conventional parabolic trough collectors.

---

### Experimental Validation

<img src="Experimental_PTC.png" width="850">

The optimised secondary reflector geometry was fabricated and installed on the existing parabolic trough collector test rig at TKM College of Engineering. Outdoor experiments were conducted under real operating conditions using on-site weather station measurements including solar irradiance, ambient temperature, humidity, and wind velocity.

---

## Machine Learning Performance Modelling

### Feature Correlation Heatmap

<img src="Heatmap.png" width="700">

Correlation analysis was performed on collected meteorological and thermal performance data. Direct normal irradiance and heat loss showed the strongest positive correlation, helping identify the dominant parameters affecting collector performance.

---

### Feature Distribution Pairplot

<img src="pairplot.png" width="850">

Pairplot analysis was used to visualise relationships between weather variables and thermal output parameters. This supported feature selection and preprocessing for machine learning model development.

---

### Regression Model Comparison

<img src="ML_Models_1.png" width="850">

Multiple regression algorithms including K-Nearest Neighbour, Random Forest, and Linear Regression were evaluated for heat gain prediction using meteorological inputs.

<img src="ML_Models_2.png" width="650">

Additional regression techniques including Ridge and Lasso regression were tested to compare prediction stability and model generalisation behaviour.

---

### ML Model Performance Results

<img src="ML_results.png" width="750">

Performance comparison across regression models showed Random Forest achieved the best overall prediction accuracy, with the highest R² score and lowest prediction error metrics among the evaluated models.

---
 
## Results
 
### Optical Simulation
- **77.07% improvement** in heat flux uniformity (6-strip 144° vs conventional PTC)
- Receiver below focal axis with secondary reflector eliminates severe local hot spots
- Peak local heat flux reduced from ~73,600 W/m² to ~33,300 W/m²
 
### Experimental Validation
- Modified PTC fabricated and tested at TKMCE campus
- Heat gain measurements tracked simulation predictions closely over multiple days
- Performance evaluated under real outdoor conditions (varying irradiance, ambient temperature, wind, humidity)
 
### ML Performance Modelling
- Trained ANN regressor on weather + system performance data
- 60% prediction accuracy on collected dataset
- Identified data volume and multi-season coverage as the primary constraint for future work — single-season dataset insufficient to capture full weather variability
 
## Repository Structure
 
- `/simulations/` — Tonatiuh model files, SolidWorks reflector geometries, ray tracing outputs
- `/experimental/` — weather station data logs, temperature measurements, on-site test photos
- `/ml/` — ANN training data, model, training scripts
- `/cad/` — SolidWorks part and assembly files for all 14 reflector geometries
- `/report/` — full B.Tech project report (PDF)
- `/figures/` — heat flux distribution plots, uniformity charts, simulation visuals
- `README.md`
 
## Tech Stack
 
- **Optical Simulation:** Tonatiuh (Monte Carlo ray tracing)
- **CAD:** SolidWorks
- **ML:** Python, Scikit-learn (ANN regressor)
- **Analysis:** Excel, Matplotlib, NumPy
 
## Reference
 
Full project report available in `/report/P14_REPORT.pdf`. Performed under the supervision of Dr. Baiju V., Department of Mechanical Engineering, TKM College of Engineering, Kollam, India.
 
## Status
 
Project completed and submitted. Fabricated, experimentally validated, and ML-modelled. Awarded as part of B.Tech (Hons) Mechanical Production Engineering, TKM College of Engineering, 2022.
 
 
