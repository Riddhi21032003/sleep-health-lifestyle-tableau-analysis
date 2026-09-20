# Sleep Health & Lifestyle Analysis

## Project Overview

This project explores the relationship between sleep health, stress, physical activity, occupation, BMI, age, gender, and blood pressure using Tableau Public.

The main objective is to identify which lifestyle and demographic factors are most strongly associated with sleep quality and sleep duration.

The project demonstrates a complete data analysis workflow, including data cleaning, data preparation, exploratory analysis, data visualisation, dashboard development, and insight generation.

---

## Problem Statement

The main analytical question for this project is:

**Which lifestyle and demographic factors are most strongly associated with sleep quality and sleep duration, and which population groups show less favourable sleep and stress patterns?**

The analysis also investigates:

- How sleep duration relates to sleep quality
- How stress level relates to sleep quality
- Whether physical activity is associated with better sleep
- How sleep patterns differ across occupations
- How BMI categories compare in terms of sleep and blood pressure
- Whether age is associated with blood pressure
- Whether sleep duration differs by gender

---

## Dataset

The dataset contains **374 observations** and includes demographic, lifestyle, sleep, and health-related variables.

| Variable | Description |
|---|---|
| Person ID | Unique participant identifier |
| Gender | Participant gender |
| Age | Participant age |
| Occupation | Participant occupation |
| Sleep Duration | Average sleep duration in hours |
| Quality of Sleep | Sleep quality score |
| Physical Activity Level | Physical activity measurement |
| Stress Level | Stress score |
| BMI Category | BMI classification |
| Blood Pressure | Systolic and diastolic blood pressure |

---

## Tools Used

- Microsoft Excel
- Tableau Public
- GitHub

---

## Data Cleaning

The original dataset was provided as a CSV file.

Microsoft Excel was used for the initial data-cleaning step.

The `BMI Category` column contained both:

- `Normal`
- `Normal Weight`

These values represented the same category, so all `Normal Weight` values were replaced with `Normal`.

The cleaned dataset was then saved as an Excel workbook and used as the data source for Tableau Public.

---

## Tableau Data Preparation

Several calculated fields were created in Tableau to support the analysis.

### Systolic Blood Pressure

```text
INT(SPLIT([Blood Pressure], "/", 1))
```

### Diastolic Blood Pressure

```text
INT(SPLIT([Blood Pressure], "/", 2))
```

### Age Group

```text
IF [Age] < 30 THEN "20s"
ELSEIF [Age] < 40 THEN "30s"
ELSEIF [Age] < 50 THEN "40s"
ELSE "50s"
END
```

### Sleep Group

```text
IF [Sleep Duration] < 7 THEN "Short Sleep (<7h)"
ELSE "7+ Hours"
END
```

### Stress Category

```text
IF [Stress Level] <= 4 THEN "Low"
ELSEIF [Stress Level] <= 6 THEN "Moderate"
ELSE "High"
END
```

---

## Analysis Workflow

**Raw CSV Dataset → Excel Cleaning → Cleaned Excel Dataset → Tableau Data Preparation → Exploratory Analysis → Visualisation → Dashboard Development → Insight Generation**

---

## Visualisations Created

The Tableau project includes:

- KPI cards for total participants
- Average sleep duration
- Average sleep quality
- Average stress level
- Sleep Duration vs Sleep Quality scatter plot
- Stress Level vs Sleep Quality scatter plot
- Average Sleep Quality by Occupation
- Average Stress Level by Occupation
- Sleep Duration by BMI Category
- Physical Activity vs Sleep Quality scatter plot
- Age vs Blood Pressure analysis
- Sleep Duration by Gender
- Sleep Quality heatmap by Age Group and BMI Category

---

## Key Findings

### Sleep Duration and Sleep Quality

Sleep duration showed a strong positive relationship with reported sleep quality.

The correlation between sleep duration and sleep quality was approximately **0.88**.

Participants with longer sleep duration generally reported higher sleep-quality scores.

---

### Stress and Sleep Quality

Stress showed a strong negative relationship with sleep quality.

The correlation between stress level and sleep quality was approximately **-0.90**.

Participants with higher stress levels generally reported lower sleep quality.

---

### Stress and Sleep Duration

Higher stress levels were also associated with shorter sleep duration.

The correlation between stress and sleep duration was approximately **-0.81**.

---

### Short Sleep vs 7+ Hours

Participants sleeping fewer than 7 hours had approximately:

- **6.14 average sleep quality**
- **6.88 average stress level**

Participants sleeping 7 or more hours had approximately:

- **8.15 average sleep quality**
- **4.32 average stress level**

This shows a clear difference in both sleep quality and stress between the two groups.

---

### Occupational Differences

Differences in sleep and stress patterns were observed across occupational groups.

For example, Salespeople in the dataset recorded relatively shorter sleep duration and higher stress, while Engineers recorded longer sleep duration, higher sleep quality, and lower stress.

Some occupational groups contained relatively few observations, so these comparisons should be interpreted carefully.

---

### BMI and Sleep

Participants in the Normal BMI category recorded higher average sleep duration than the Overweight group.

Differences were also visible across BMI categories in sleep quality and blood-pressure measurements.

---

### Physical Activity

Physical activity showed a weaker relationship with sleep quality compared with sleep duration and stress.

Within this dataset, stress and sleep duration appear more strongly associated with reported sleep quality.

---

## Conclusion

The analysis suggests that **sleep duration and stress level are the variables most strongly associated with sleep quality in this dataset**.

Longer sleep duration is associated with higher reported sleep quality, while higher stress levels are associated with both poorer sleep quality and shorter sleep duration.

Differences were also observed across occupations and BMI categories.

Because the dataset is observational, the findings represent **associations rather than causal relationships**.

---

## Limitations

- The dataset contains 374 observations.
- Some occupational categories contain small sample sizes.
- The dataset is observational and cannot establish causation.
- Some lifestyle and sleep variables may be self-reported.
- Other factors that could influence sleep health may not be included.

---

## Repository Files

```text
README.md
Sleep_Health_Lifestyle_Raw.csv
Sleep_Health_Lifestyle_Cleaned.xlsx
Sleep_Health_Lifestyle_Analysis.twbx
Sleep_Health_Overview.png
Lifestyle_Health_Deep_Dive.png
```

---

## Tableau Dashboard

**[View Interactive Tableau Dashboard](https://public.tableau.com/views/SleepHealthLifestyleAnalysis_17897549699130/SLEEPHEALTHLIFESTYLEANALYSIS?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**

---

## Dashboard Preview

### Sleep Health Overview

<img width="1497" height="799" alt="Lifestyle_Health_Deep_Dive" src="https://github.com/user-attachments/assets/3eaed2e8-ef7b-4322-b84e-8d9a9d2b61c4" />


### Lifestyle & Health Deep Dive

<img width="1497" height="799" alt="Lifestyle_Health_Deep_Dive" src="https://github.com/user-attachments/assets/38063770-0b7a-4d5d-a15a-d0886a1be1d6" />


---

## Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis
- Tableau Calculated Fields
- Data Visualisation
- Dashboard Development
- Statistical Analysis
- Data Storytelling
- GitHub Documentation
- Microsoft Excel
- Tableau Public

---

## Author

**Riddhi Patel**

Data Analyst | Artificial Intelligence

[LinkedIn](https://www.linkedin.com/in/riddhi-patel-46a3762ab/)
