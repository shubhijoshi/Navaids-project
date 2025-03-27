# Predicting Navaid Power Levels Using Signal and Operational Characteristics

# Source of Data 
https://ourairports.com/data/

## Overview
Navigational Aids (Navaids) are essential for aviation safety, providing critical location and directional data for aircraft. This project develops a **machine learning model** to predict Navaid power levels based on multiple operational features.

## Objective
Predict Navaid power levels (**LOW, MEDIUM, HIGH**) using features like frequency, elevation, and magnetic variation. Accurate predictions enhance **aviation infrastructure planning, resource allocation, and navigation system reliability**.

## Why is Power Prediction Important?
- **Preventing Equipment Failure** – Aviation navigation relies on continuous signal availability. Low or excessive power levels can indicate potential equipment degradation or impending failure, allowing for proactive maintenance before critical failures occur.
- **Smart Predictive Maintenance** – By analyzing historical power data, the model can identify patterns leading to power failures, helping technicians schedule maintenance before a system goes down. This reduces unscheduled downtimes and keeps operations smooth.
- **Optimizing Power Consumption** – Many Navaid stations operate continuously, consuming significant power. Predicting optimal power levels can help reduce unnecessary energy usage, improving efficiency and lowering operational costs.

## Dataset Overview
| Feature                 | Description |
|-------------------------|-------------|
| **frequency_khz**       | Navaid operating frequency |
| **dme_frequency_khz**   | Frequency used for DME |
| **magnetic_variation_deg** | Magnetic deviation at the location |
| **slaved_variation_deg** | Additional magnetic variation |
| **elevation_ft**        | Elevation above sea level |
| **usageType**           | Classification of Navaid usage |
| **associated_airport**  | Related airport |
| **power (Target)**      | Categorized as "LOW", "MEDIUM", or "HIGH" |

##  Feature Relationships
1. Power vs. Frequency:
   - Higher frequencies may require more precise tuning and power adjustments due to increased atmospheric attenuation.
   - Lower frequencies can travel longer distances but may still need consistent power for stable transmission.
2. Power vs. Elevation:
   - Higher elevations often face less interference, reducing power needs.
   - Lower elevations may have more obstructions (terrain, buildings), requiring higher power levels for effective signal reach.
3. Power vs. Magnetic Variation:
   - Variations in Earth's magnetic field may impact signal calibration, requiring power adjustments for accurate transmission.
   - Sudden changes in magnetic variation might necessitate real-time power tuning to maintain system accuracy. 

## Tech Stack
### Libraries Used:
1. *Data Manipulation & Cleaning*
   - pandas – Used for loading the dataset, handling missing values, filtering data, and transforming categorical variables into numerical representations.

   - numpy – Utilized for numerical computations, array manipulations, and mathematical operations to process data efficiently.

2. *Data Visualization*
   - matplotlib – Used for creating plots and visualizing trends in the dataset, such as distributions and class imbalances.

   - seaborn – Employed for advanced statistical data visualization, including correlation heatmaps and feature relationships.
3. **Machine Learning**
   - `scikit-learn`
     - `RandomForestClassifier` – Model training.
     - `StandardScaler` – Feature scaling.
     - `GridSearchCV` – Hyperparameter tuning.
     - `accuracy_score` – Model evaluation.
   - `imbalanced-learn`
     - `SMOTE` – Handle class imbalance.

## Machine Learning Model
- **Random Forest with Hyperparameter Tuning**  
  The primary model used in this project is the Random Forest Classifier, which is an ensemble learning method that operates by constructing multiple decision trees and averaging their predictions to improve accuracy and reduce overfitting.
By leveraging hyperparameter tuning, the best-performing model was selected to maximize classification accuracy for predicting Navaid power levels.

## Challenges
- Handling missing values in key features like dme_frequency_khz and slaved_variation_deg.
- Scaling numerical data for better model performance.
- Selecting the optimal machine learning model to achieve the highest classification accuracy.

## Success Metric
The model will be evaluated based on classification accuracy, aiming to optimize prediction performance through feature engineering, data preprocessing, and hyperparameter tuning.
By accurately predicting Navaid power levels, this project enhances aviation reliability, reduces energy consumption, and supports proactive maintenance, ensuring safer and more efficient air navigation systems.

## Internship Completion Certificate
https://drive.google.com/file/d/1Qe4rv19icfesJ8UbJtxH9jGjHpF0acfi/view?usp=drivesdk

## About Airports Authority of India, Raipur
[AAI Official Website](https://www.aai.aero)  
**Industry**: Aviation & Air Navigation Services  
**Employees**: 5000+ (Across India)  
**Founded**: 1995  

The **CNS (Communication, Navigation, and Surveillance) department** ensures seamless air traffic communication, **advanced navigation aids, and robust surveillance systems** for safe flight operations. This project was undertaken under **AAI Raipur’s Navaids Department**, managing Navaid installation and maintenance.

---

## Contributions
Contributed by **Shubhi Joshi** (NITRR) and **Sneha Kumar** (NITRR) under the guidance of Sandeep Rathore Sir (AAI Raipur)



