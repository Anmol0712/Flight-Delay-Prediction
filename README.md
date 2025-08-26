# Flight Delay Analysis & Prediction  

This project analyzes **US airline flight delays** and builds models to understand and predict the factors that most impact delays.  
The dataset contains detailed information about flights, delays, and their causes (carrier, weather, NAS, security, late aircraft).  

---

## Dataset  

- **Source:** US Department of Transportation (Bureau of Transportation Statistics)  
- **Features Include:**  
  - Flight info: `year`, `month`, `carrier`, `carrier_name`, `airport`, `airport_name`  
  - Performance: `arr_flights`, `arr_del15` (delays ≥15 minutes), `arr_cancelled`, `arr_diverted`  
  - Delay causes: `carrier_ct`, `weather_ct`, `nas_ct`, `security_ct`, `late_aircraft_ct`  
  - Delay minutes: `carrier_delay`, `weather_delay`, `nas_delay`, `security_delay`, `late_aircraft_delay`  
- **Target Variable:** Arrival Delay (binary/continuous depending on task)  

---

## Analysis Performed  

1. **Delay distribution by cause** – which factors contribute most (carrier, weather, NAS, etc.)  
2. **Seasonality trends** – delays by year & month to spot seasonal patterns  
3. **Airline-level analysis** – identifying carriers most prone to delays  
4. **Airport-level analysis** – airports with highest delay frequencies  
5. **Correlation analysis** – relationship between delay causes & total delay time  

---

## Models Implemented  

- Linear Regression   
- Random Forest   
- Gradient Boosting (XGBoost)  

---

## Results  

| Model              | Performance | Notes |
|---------------------|-------------|-------|
| Linear Regression   | ~28% acc    | Good baseline, simple linear approach |
| Random Forest       | ~97.7% acc  | Strong performance, interpretable |
| XGBoost             | ~85.7% acc  | Generalizes better, avoids overfitting |

👉 **XGBoost was chosen as the final model** due to its balance of accuracy, generalization, and interpretability of feature importance.  

