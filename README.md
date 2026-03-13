# Power BI – Advanced HR Analytics Dashboard

## Project Overview
Organizations need to monitor and anticipate their workforce to improve talent management and strategic decision-making.

This project builds an **interactive HR analytics dashboard in Power BI** that allows executives to explore workforce trends, employee retention, and turnover using a clean and professional interface.

The dashboard is built on a **star schema data model**, with advanced **DAX measures** and **interactive visualizations** to provide deep insights into the workforce.

---

# Business Objectives

The goal of this project is to provide leadership with an intuitive dashboard that answers key HR questions:

- What is the current **headcount**?
- How is the workforce distributed across **departments and job levels**?
- What are the **demographic characteristics** of employees?
- How strong is employee **retention**?
- What is the **turnover trend over time**?
- What are the main **reasons for employee termination**?

---

# Dataset

The HR dataset contains several categories of information:

### Employee Data
- Employee ID
- Full Name
- Gender
- Race
- Date of Birth
- Marital Status

### Employment History
- Hire Date
- Termination Date
- Department
- Job Level
- Manager hierarchy

### Compensation
- Salary
- Bonus

### Location
- City
- Country

### Education
- Education Level

---

# Data Modeling

The data model follows a **Star Schema architecture** to optimize performance and simplify analysis.

## Fact Table
**People Fact**

Contains core employment records including:
- Employee ID
- Hire Date
- Term Date
- Department
- Job Level
- Salary
- Manager hierarchy

## Dimension Tables

- **Department Dim**
  - Department
  - Sub-Department

- **Job Level Dim**
  - Job Level

- **Termination Dim**
  - Termination Type
  - Termination Reason

- **Demographic Dim**
  - Gender
  - Race
  - Age

- **Education Dim**
  - Education Level

- **Location Dim**
  - City
  - Country

- **Marital Dim**
  - Marital Status

- **Manager Dim**
  - Manager Level 1 → Level 4 hierarchy

---

# Data Preparation

Data preparation was performed using **Power Query**.

Steps included:

- Importing CSV files
- Cleaning null and inconsistent values
- Calculating **Age from Date of Birth**
- Converting salary fields to **Currency type**
- Standardizing employee **Active Status (Yes / No)**
- Cleaning manager hierarchy identifiers
- Disabling source table loading for model optimization

