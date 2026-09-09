# ⚽ FIFA 20 Data Analysis & Player Clustering Project (PRCP-1004-Fifa20)

## 📌 Project Overview
Football (soccer) is one of the most popular sports globally, and the EA Sports FIFA series is its foremost simulation video game. This project leverages the **FIFA 20 Career Mode** dataset (`players_20.csv`) to conduct an end-to-end data analysis and unsupervised machine learning study[cite: 6].

---

## 🎯 Objectives & Tasks

### **Task 1: Complete Data Analysis Report**
* Perform data inspection, cleaning, preprocessing, and statistical distribution analysis on over 18,000 player records across 104 attributes[cite: 6].

### **Task 2: Football Skill Exploration & Player Clustering**
* Identify key physical and technical attributes to cluster outfield players into distinct stylistic archetypes (e.g., Target Strikers, Playmakers, Ball-Winning Defenders, Wingers) without allowing the `Overall` rating to artificially dominate the clusters[cite: 6].

### **Task 3: Key Research Questions**
1. **Top Football-Producing Nations:** Identify and rank-order the top 10 countries producing the most professional players in FIFA 20[cite: 6].
2. **Age vs. Overall Rating:** Plot the distribution of player overall rating against age to determine the career development curve and identify the typical peak/inflection age[cite: 6].
3. **Offensive Wage Disparities:** Compare wage distributions across offensive roles (Strikers vs. Right-Wingers vs. Left-Wingers) to evaluate which role commands higher compensation[cite: 6].

---

## 📊 Dataset Description

The dataset comprises **18,278 players** and **104 features**[cite: 6].

### Key Feature Categories[cite: 6]:
* **Demographics & Identification:** `Short_Name`, `Full_Name`, `Age`, `Date_of_Birth`, `Height_cm`, `Weight_kg`, `Nationality`, `Club`[cite: 6].
* **Performance & Valuations:** `Overall_Rating`, `Potential_Rating`, `Value_EUR`, `Wage_EUR`, `International_Reputation`[cite: 6].
* **Attacking & Skill Stats:** `Attacking_Crossing`, `Attacking_Finishing`, `Attacking_Heading_Accuracy`, `Attacking_Short_Passing`, `Attacking_Volleys`, `Skill_Dribbling`, `Skill_Curve`, `Skill_FK_Accuracy`, `Skill_Long_Passing`, `Skill_Ball_Control`[cite: 6].
* **Movement & Power:** `Movement_Acceleration`, `Movement_Sprint_Speed`, `Movement_Agility`, `Movement_Reactions`, `Movement_Balance`, `Power_Shot_Power`, `Power_Jumping`, `Power_Stamina`, `Power_Strength`, `Power_Long_Shots`[cite: 6].
* **Mentality & Defending:** `Mentality_Aggression`, `Mentality_Interceptions`, `Mentality_Positioning`, `Mentality_Vision`, `Mentality_Penalties`, `Mentality_Composure`, `Defending_Marking`, `Defending_Standing_Tackle`, `Defending_Sliding_Tackle`[cite: 6].
* **Goalkeeping:** `Goalkeeping_Diving`, `Goalkeeping_Handling`, `Goalkeeping_Kicking`, `Goalkeeping_Positioning`, `Goalkeeping_Reflexes`[cite: 6].
* **Positional Ability Ratings:** Base ratings across 26 positions on the pitch (`LS`, `ST`, `RS`, `LW`, `CAM`, `CB`, `LB`, etc.)[cite: 6].

---

## 🛠️ Data Preprocessing & Methodology

1. **Feature Renaming:** Converted raw snake_case database names to descriptive, standardized column headers[cite: 6].
2. **Positional Data Cleaning:** Extracted base numeric ratings from positional notation strings (e.g., converting `'68+2'` into `68`)[cite: 6].
3. **Missing Value Imputation:**
   * Numerical features were imputed with their respective medians to maintain skewness[cite: 6].
   * Categorical attributes were imputed using mode values[cite: 6].
4. **Feature Scaling & Dimensionality Reduction:** Scaled 29+ granular skill attributes using `StandardScaler` and applied **Principal Component Analysis (PCA)** for 2D visualization.
5. **Clustering:** Applied **K-Means Clustering** to segment outfield players based on multidimensional performance metrics.

---

## 🔍 Key Findings & Answers to Task 3

* **Top 10 Player-Producing Nations:** England, Germany, Spain, France, and Argentina lead player representations in FIFA 20[cite: 6].
* **Development & Inflection Age:** Player overall ratings rise rapidly between the ages of 17 and 24, plateauing near peak performance between ages 27 and 30 before gradual physical decline occurs[cite: 6].
* **Offensive Wages:** Strikers (ST/CF) and Right-Wingers (RW/RM) show higher top-end wage distributions compared to traditional left-wing roles[cite: 6].

---

## ⚙️ Tech Stack & Dependencies

* **Language:** Python 3.8+
* **Libraries:**
  * `pandas` & `numpy` (Data manipulation)[cite: 6]
  * `matplotlib` & `seaborn` (Data visualization)[cite: 6]
  * `scikit-learn` (StandardScaler, PCA, KMeans)

---

## 🚀 How to Run

1. Clone the repository and navigate to the project directory:
   ```bash
   git clone <repository_url>
   cd <repository_name>