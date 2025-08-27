# 📊 Loan Default Risk Analysis – Power BI Project
## 🚀 Project Overview

This project is a Power BI dashboard that analyzes loan default risks using applicant demographics and financial data.
It helps banks and financial institutions identify high-risk borrowers, track trends, and make data-driven lending decisions.

## 🛠️ Tools & Technologies

Microsoft SQL Server – Data storage & import

Power BI Desktop – Data modeling, DAX, dashboards

Power BI Service – Dataflows, scheduled refresh, sharing

DAX Functions Used – SUMX, CALCULATE, FILTER, ALLEXCEPT, DIVIDE, MEDIANX, SWITCH, etc.

Excel – Data validation

## 📂 Project Workflow (Step-by-Step)
### 1) Setup & Connectivity

Installed and configured On-premises Data Gateway (Standard Mode).

Installed Microsoft SQL Server for data storage.

Imported raw loan dataset into SQL Server.

### 2) Build Dataflow in Power BI Service

Created a Dataflow in Power BI Service and connected it to SQL Server.

Defined tables/entities and saved them in the Dataflow.

Refreshed the Dataflow to make data available for Desktop.

### 3) Connect Power BI Desktop to Dataflow

In Power BI Desktop → Get Data → Power BI Dataflows → selected entities.

Loaded fact and dimension tables (Loans, Applicants, Dates, etc.).

### 4) Data Cleaning & Profiling (Power Query)

Set correct data types (numbers, dates, text).

Used Column Quality/Distribution/Profile to detect missing or invalid values.

Renamed columns and documented dataset fields.

### 5) Data Modeling (Star Schema)

Built a Fact Table (Loans) and Dimension Tables (Applicants, Dates, Purpose, Education, etc.).

Created relationships (e.g., Applicants[ApplicantID] → Loans[ApplicantID]).

Added a Date table and marked it as the official Date table.

### 6) DAX Measures (KPIs & Analysis)

Created several DAX measures, including:

Loan Amount by Purpose → SUMX, FILTER, NOT, ISBLANK

Average Income by Employment Type → CALCULATE, AVERAGE, ALLEXCEPT

Default Rate by Employment Type → COUNTROWS, DIVIDE, ALLEXCEPT, FILTER

Average Loan by Age Groups → AVERAGEX, VALUES

Default Rate by Year → CALCULATE, COUNTROWS, DIVIDE, FILTER, ALLEXCEPT

Median Loan Amount by Credit Score → MEDIANX

YOY Loan Amount & Defaults → Time Intelligence (SAMEPERIODLASTYEAR, CALCULATE)

YTD Loan Amount by Credit Score & Marital Status → TOTALYTD

Risk Buckets for Decomposition Tree → SWITCH

### 7) Dashboard Visuals

KPI Cards → Total Loans, Defaults, Default Rate %

Donut Chart → Loan Amount by Age Group & Marital Status

Clustered Column Chart → Loans by Education / Mortgage

Line Charts → YOY & YTD Loan and Default trends

Decomposition Tree → Risk segmentation (using SWITCH function)

Added Slicers (Age, Employment Type, Education, Credit Score, Year) for interactivity.

### 8) Data Validation

Cross-checked values for Average Loan, Median Loan, Default Rate, and YOY measures using Excel calculations.

Ensured Power BI results matched validation values.

### 9) Automation (Refresh)

Configured Scheduled Refresh in Power BI Service for Dataflow and Dataset.

Set up Incremental Refresh (using RangeStart/RangeEnd parameters) for large datasets.

### 10) Publish & Share

Published the final report to Power BI Service.

Set dataset credentials and verified scheduled refresh.

Shared the report with stakeholders through Workspace/App.

Also exported summary dashboards as PDF/PPT for presentation.
## 📊 Dashboard Insights

Default Rate Trends → Identified risky borrower categories (by age, income, employment).

YOY Analysis → Tracked loan growth and default rate changes over years.

Risk Segmentation → Credit score and marital status impact on defaults.

Decision Support → Helps banks reduce loan losses and improve lending policies.

## 🧑‍💻 Skills Demonstrated

Power BI Dashboard Design

Data Modeling (Star Schema)

DAX Functions (Advanced Calculations)

Data Cleaning & Profiling

SQL + Power BI Integration

Scheduled & Incremental Refresh

Storytelling with Data

## 📸 Screenshots

(Add 2–3 screenshots of your dashboard here: Home Page, Risk Analysis Page, YOY Trends)

