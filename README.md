# Berkeley Police Calls for Service – Short-Term Demand Analysis

## Overview
This project analyzes **Berkeley Police Department (BPD) Calls for Service** data to understand short-term patterns in police service demand and to evaluate whether recent call volume contains useful information for **short-term forecasting**.

Rather than attempting to predict individual crimes or locations, this analysis focuses on **aggregate workload** (weekly total calls), which is the appropriate and ethical level for predictive analysis using calls-for-service data.

---

## Dataset
- **Source:** City of Berkeley Open Data Portal  
- **Dataset:** Berkeley PD – Calls for Service  
- **Unit of observation:** One call requesting police service  
- **Time span:** Approximately 180 days (April–October 2022)

### Important Notes on the Data
- One incident may generate multiple calls.
- Some records contain incomplete or defaulted timestamps (e.g., `12:00 AM`).
- Locations are reported at the **block level** or may be missing.

As a result, this analysis examines **service demand patterns**, not crime incidence.

---

## Methodology

### 1. Temporal Aggregation
- Event dates were converted into a numeric **WeekIndex**, representing the number of weeks since the first observation.
- Calls were aggregated by `WeekIndex` to produce **weekly call totals**.
- Weekly aggregation reduces daily noise while remaining appropriate for the short observation window.

---

### 2. Exploratory Analysis
The project examines:
- Distribution of calls across weeks
- Time-of-day patterns (with careful handling of default/unknown times)
- Spatial concentration at a **corridor level** rather than exact addresses

Spatial analysis avoids fine-grained mapping due to a high proportion of missing or anonymized location data.

---

### 3. Short-Term Demand Forecasting
A simple **autoregressive linear model** was used to assess short-term predictability:

#### Computed Statistics
- **Correlation coefficient (r):** Measures week-to-week persistence
- **Slope (β):** Indicates how strongly demand carries over from one week to the next
- **Intercept (α):** Represents baseline weekly demand

The model is used to generate a **one-week-ahead forecast** based on the most recent observed week.

---

## Results
- Weekly call volume exhibits **short-term persistence**, with a positive correlation between consecutive weeks.
- Predictability decreases rapidly as the lag increases beyond one week.
- The forecasting model provides a **reasonable short-term estimate**, but accuracy is limited by natural variability and the short data window.

The final forecast extends **beyond the dataset’s observation window** and therefore represents an **out-of-sample prediction** without available ground truth for direct validation.

---

## Limitations
- Short observation period (~6 months)
- No seasonal or long-term trend modeling
- Aggregate data only (no individual-level prediction)
- Missing and defaulted time/location fields
- Forecasts are **illustrative**, not operational recommendations

---

## Conclusion
This project demonstrates how calls-for-service data can be responsibly analyzed to understand short-term workload dynamics. While the data supports **limited short-term demand forecasting**, results should be interpreted cautiously and within the constraints of the dataset.

The analysis emphasizes:
- Appropriate aggregation
- Ethical framing of prediction
- Clear acknowledgment of data limitations

---

## Files
- `calls_for_service.ipynb` — Full analysis and forecasting workflow
- `Berkeley_PD_-_Calls_for_Service_20260105.csv` — Source dataset
