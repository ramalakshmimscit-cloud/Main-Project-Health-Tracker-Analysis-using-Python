
# Health Tracker Analytics Using Python

## 📌 Project Overview
This project focuses on analyzing health tracker and wearable technology metrics using Python for data cleaning, text transformation, statistical evaluation, and exploratory visualization. The project uncovers user behavioral profiles, fitness habits, dietary preferences, and subscription trends across different demographic groups and wearable device hardware.

The analysis was performed using core data science libraries such as Pandas, NumPy, Matplotlib, and Seaborn to process 5,000 user activity logs, revealing clear trends and data-driven insights.

---

## 🎯 Project Objectives
* Analyze health tracker behavior and premium subscription patterns.
* Identify major lifestyle habits affecting user choices and service tiers.
* Understand user engagement levels and device hardware usage trends.
* Perform detailed descriptive and grouping statistical analyses on behavioral metrics.
* Generate production-grade exploratory data visualizations and trend charts.
* Extract actionable data insights from physical activity and lifestyle logs.

---

## 📊 Dataset Information

### Domain
* Healthcare Informatics
* Wearable Technology Analytics
* User Behavior & Lifestyle Analytics

### Features Included in Dataset
* **user_id**: Unique identifier for each tracked user.
* **age**: The age of the individual user.
* **gender**: Identified gender category.
* **country**: Geographic location of the user.
* **device_model**: Name of the wearable fitness tracker model.
* **activity_type**: Main exercise logged during that session.
* **active_minutes**: Duration of active exercise in minutes.
* **sleep_duration_mins**: Total sleep tracked during the night cycle in minutes.
* **sync_time**: Timestamp showing when data synced to the server.
* **has_premium**: Boolean flag (`TRUE`/`FALSE`) for premium subscriptions.
* **logged_food_tags**: Dietary preferences or logs tagged by the user.
* **steps_counted**: Total physical steps recorded by the tracker.

---

## 🛠️ Technologies Used
* **Language**: Python 3.8+
* **Environment**: Jupyter Notebook
* **Data Manipulation**: Pandas, NumPy
* **Data Visualization**: Matplotlib, Seaborn

---

## ⚙️ Core Analytics & Processing Steps

### 1. Data Cleaning & Preprocessing
* Removed duplicate records and handled outlying variables.
* Imputed missing user ages via cohort median statistics to preserve dataset integrity.
* Sanitized empty dietary metadata blocks into structured text tags.
* Standardized column names and corrected structural data types.

### 2. Feature Engineering & Transformation
* Parsed nested string fields (`logged_food_tags`) into individual flag columns (`is_keto`, `is_vegan`, `is_low_carb`).
* Deconstructed complex timestamp strings (`sync_time`) into operational metrics (`sync_hour`, `is_weekend`).
* Created derived activity indicators combining active minutes and step frequencies.

### 3. Statistical Analysis
* Calculated descriptive metrics including Mean, Median, Mode, and Standard Deviation.
* Performed cross-tabulation and Pivot table analyses comparing categories like Country vs. Subscription status.
* Executed comprehensive correlation analysis across continuous health metrics (steps, sleep, active minutes).
* Generated GroupBy summary matrices mapping performance benchmarks across device hardware models.

---

## 🖼️ Visualizations Created

### Matplotlib & Seaborn
* **Box Plot**: Distribution of Daily Step Counts across unique Wearable Device Models.
* **Scatter Plot**: Exercise Intensity (`active_minutes`) vs. Total Tracked Sleep Duration.
* **Histogram**: Age Distribution of tracker users segmented by Gender.
* **Bar Plot**: Premium Subscription Rates across different Dietary Tag Profiles.
* **Heatmap**: Correlation Matrix highlighting dependencies between activity, sleep, and step metrics.
* **Count Plot**: Activity Type distribution mapped across Weekend vs. Weekday core sync times.
* **Pie Chart**: Global distribution of users by Country core demographics.

---

## 💡 Key Insights

* **Activity vs. Sleep Dynamics**: A clear correlation exists between moderate daily active minutes and consistent, optimal sleep durations (~7–8 hours). However, extreme, unpaced activity spikes occasionally correlated with shorter sleep windows.
* **Dietary Affinities**: Users tagging their meals with `#keto` and `#low_carb` displayed higher average step counts and were statistically more likely to hold premium subscriptions compared to non-tagging groups.
* **Hardware Performance Gaps**: Metrics such as daily steps showed noticeable variance across unique `device_model` options, indicating potential calibration differences or specific model preferences among high-activity users.
* **Temporal Syncing Trends**: Application syncing activity heavily peaks during late evening hours on weekdays, while shifting toward early morning slots on weekends.

---

## 🎓 Learning Outcomes
Through this project, the following skills were developed:
* Constructing complete programmatic data manipulation pipelines in Python.
* Transforming unstructured textual elements (hashtags) into structured data frames.
* Handling missing values logically using statistical grouping distributions.
* Developing complex multi-variable exploratory plots to explain behavioral habits.
* Utilizing advanced Pandas indexing, merging, and grouping mechanisms on large arrays.
* Turning messy tracking metrics into intuitive, well-structured analytical observations.

---

## 🏁 Conclusion
This project successfully demonstrated how core Python data analytics can be applied to derive comprehensive health informatics clarity from wearable device logs. By mapping out clear relationships between daily exercise, hardware performance, and dietary lifestyles, the resulting analysis proves how raw telemetry data can be translated into readable user patterns, actionable segment metrics, and clear data-driven decisions.

---

## 📁 Repository Structure
```text
├── data/
│   └── health_tracker_analytics_5000.csv  # Raw Source Dataset
├── notebooks/
│   └── health_analytics_pipeline.ipynb    # Python Jupyter Notebook (Data Cleaning & EDA)
└── README.md                              # Project Documentation Report
```

---

## 🚀 How to Execute the Project

1. **Clone this repository** to your local workspace.
2. **Install required packages**:
   ```bash
   pip install numpy pandas matplotlib seaborn
   ```
3. **Open Jupyter Notebook** and run `notebooks/health_analytics_pipeline.ipynb` sequentially to view the code execution, statistical outputs, and generated trend plots.
