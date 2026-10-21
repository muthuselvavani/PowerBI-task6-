# PowerBI-task6-
# 🏥 Healthcare Data Cleaning, Star Schema Modelling & Dashboard using Power BI

## 📌 Project Overview

This project focuses on cleaning healthcare data, building a **Star Schema Data Model**, and developing an interactive **Healthcare Dashboard** using Microsoft Power BI.

Power Query Editor is used to clean and transform healthcare records. Dimension tables and a central fact table are created to support structured data analysis. The final dashboard provides insights into patient demographics, medical conditions, hospital admissions, and admission trends.

## 🎯 Objectives

- Clean and transform healthcare data using Power Query.
- Correct data types and standardize text values.
- Remove exact duplicate records.
- Categorize patients into age groups.
- Create dimension tables for patients, doctors, hospitals, and dates.
- Build a central FactAdmission table.
- Establish relationships using a Star Schema model.
- Design an interactive dashboard using KPI cards, slicers, and charts.

## 🛠️ Technologies Used

- Microsoft Power BI Desktop
- Power Query Editor
- Power BI Model View
- Power BI Report View
- CSV Dataset

## 📂 Dataset Information

- **Dataset:** `healthcare_dataset(2).csv`
- **Original Records:** 55,500 rows
- **Columns:** 15

### Dataset Columns

- Name
- Age
- Gender
- Blood Type
- Medical Condition
- Date of Admission
- Doctor
- Hospital
- Insurance Provider
- Billing Amount
- Room Number
- Admission Type
- Discharge Date
- Medication
- Test Results

## 🧹 Data Cleaning and Transformation

The following operations were performed using Power Query:

1. Imported the healthcare CSV dataset.
2. Renamed the base query to `Healthcare_Cleaned`.
3. Assigned appropriate data types to the columns.
4. Applied Trim and Clean operations to text columns.
5. Standardized patient names using Capitalize Each Word.
6. Removed 534 exact duplicate records.
7. Created an `AgeGroup` column.
8. Standardized admission types as Emergency, Elective, and Urgent.

### Age Group Categories

| Age Range    | Category     |
| ------------ | ------------ |
| 0–17         | Pediatric    |
| 18–39        | Young Adult  |
| 40–59        | Middle Adult |
| 60 and above | Senior       |

## ⭐ Star Schema Data Model

The project includes six tables:

| Table Name           | Purpose                                      |
| -------------------- | -------------------------------------------- |
| `Healthcare_Cleaned` | Cleaned base dataset                         |
| `DimPatient`         | Patient details and PatientID                |
| `DimDoctor`          | Doctor details and DoctorID                  |
| `DimHospital`        | Hospital details and HospitalID              |
| `DimDate`            | Date, year, month, month number, and quarter |
| `FactAdmission`      | Admission records and measurable details     |

### Model Relationships

The `FactAdmission` table is connected to four dimension tables:

- `DimPatient[PatientID]` → `FactAdmission[PatientID]`
- `DimDoctor[DoctorID]` → `FactAdmission[DoctorID]`
- `DimHospital[HospitalID]` → `FactAdmission[HospitalID]`
- `DimDate[Date]` → `FactAdmission[Date of Admission]`

All four relationships use **one-to-many (1:\*) cardinality** with single-direction cross-filtering.

## 📊 Healthcare Dashboard

The interactive dashboard was developed in Power BI Report View.

### Dashboard Components

| Component                         | Visual Type            | Purpose                                                          |
| --------------------------------- | ---------------------- | ---------------------------------------------------------------- |
| Admission Type                    | Dropdown Slicer        | Filters admissions by type                                       |
| Insurance Provider                | Dropdown Slicer        | Filters by insurance provider                                    |
| Total Patients                    | KPI Card               | Displays the total patient count                                 |
| Average Age                       | KPI Card               | Displays the average patient age                                 |
| Age Group vs Medical Condition    | Matrix                 | Compares patient counts across age groups and medical conditions |
| Total Admission by Hospital       | Bar/Column Chart       | Compares admissions across hospitals                             |
| Total Admission by Year           | Line/Area Chart        | Displays yearly admission trends                                 |
| Total Admission by Admission Type | Pie Chart              | Shows the distribution of admission types                        |
| Total Admission by Age Group      | Pie Chart              | Shows the distribution of age groups                             |
| Gender by Year                    | Clustered Column Chart | Compares yearly patient counts by gender                         |

### Dashboard Preview

<img width="1332" height="751" alt="Screenshot 2026-10-21 124014" src="https://github.com/user-attachments/assets/6dd8b01a-33a6-4331-acad-733b63243c0d" />


### Design

- Dark navy background with a yellow header banner.
- KPI cards positioned at the top for quick insights.
- Dropdown slicers for interactive filtering.
- Charts and a matrix arranged for easy comparison.
- Consistent formatting for a professional healthcare analytics dashboard.

## 📈 Dashboard Insights

- Admissions are almost evenly distributed across Emergency, Elective, and Urgent categories.
- The Senior age group has the highest patient counts across the medical conditions analyzed.
- Admission volumes remain relatively steady from 2020 to 2023.
- The lower admission count in 2024 may be due to partial-year data.

*These insights are based on the dashboard analysis and should be validated against the dataset's date coverage and final report values.*

## ✨ Key Features

- Healthcare data cleaning and preprocessing.
- Duplicate record removal.
- Patient demographic categorization.
- Standardization of admission types.
- Surrogate key generation.
- Fact and dimension table creation.
- Star Schema data modelling.
- Date dimension with year, month, and quarter.
- Interactive dashboard with slicers and KPI cards.
- Visual analysis of hospital admissions, age groups, gender, and medical conditions.

## 🚀 How to Run the Project

1. Install and open Microsoft Power BI Desktop.
2. Obtain the healthcare CSV dataset.
3. Select **Home → Get Data → Text/CSV**.
4. Import `healthcare_dataset(2).csv`.
5. Select **Transform Data** to open Power Query Editor.
6. Perform the required data cleaning and transformation steps.
7. Create the dimension tables and `FactAdmission` table.
8. Create the `DimDate` table.
9. Select **Close & Apply**.
10. Open Model View and configure the four relationships.
11. Verify the Star Schema model.
12. Switch to Report View and create the slicers, KPI cards, matrix, and charts.
13. Apply the navy and yellow theme.
14. Save the Power BI report as `Healthcare_Dashboard.pbix`.

## 🎓 Learning Outcomes

- Understanding data cleaning using Power Query.
- Working with healthcare datasets.
- Creating fact and dimension tables.
- Generating surrogate keys.
- Understanding Star Schema architecture.
- Creating and managing Power BI relationships.
- Designing interactive dashboards.
- Developing data analysis and visualization skills.

## 📁 Repository Structure

```text
Healthcare-PowerBI-Project/
├── healthcare_dataset(2).csv
├── Healthcare_Dashboard.pbix
├── PowerBI_Healthcare_Star_Schema_Guide.pdf
├── images/
│   └── dashboard.png
└── README.md
```

## 📄 Documentation

Refer to `PowerBI_Healthcare_Star_Schema_Guide.pdf` for the detailed, step-by-step implementation guide.

## 👨‍💻 Project Information

**Project Title:** Healthcare Data Cleaning, Star Schema Modelling & Dashboard using Power BI

**Domain:** Healthcare Analytics

**Tools:** Microsoft Power BI, Power Query Editor, CSV

**Project Type:** Academic / Data Analytics Project

---

