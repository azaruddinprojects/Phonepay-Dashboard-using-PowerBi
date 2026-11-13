
# Digital Payments Analytics Dashboard

An interactive Power BI dashboard designed to analyze digital payment transactions, customer activity, service performance, and payment trends.

The project covers the complete analytics workflow, from data preparation and transformation to DAX-based KPI development and interactive dashboard reporting.

## Dashboard

![Digital Payments Analytics Dashboard](Screenshots/dashboard.png)

## Project Overview

The dashboard provides a consolidated view of payment activity and enables analysis across different dimensions such as time, payment status, customer segments, services, and user transaction value.

The report focuses on the following areas:

- Transaction volume and transaction value
- Monthly transaction trends
- Payment success rate
- Unique users
- Age segment contribution
- Service-wise transaction value
- Top users by transaction value
- Weekday vs. weekend usage

## Technology Stack

- **Power BI Desktop** – Dashboard development and visualization
- **Power Query** – Data cleaning and transformation
- **DAX** – KPI and analytical calculations
- **Excel / CSV** – Data source
- **GitHub** – Project documentation and version control

## Data Preparation

The source data was prepared using Power Query before developing the dashboard.

The main preparation steps included:

- Removing duplicate records
- Handling missing values
- Correcting data types
- Standardizing categorical fields
- Creating month and weekday fields
- Creating age segments
- Classifying weekday and weekend transactions
- Validating transaction and payment status data

## Data Modeling

The cleaned dataset was structured in Power BI to support analysis across:

- Transactions
- Users
- Payment services
- Payment status
- Transaction dates
- Customer segments

The data model was designed to ensure that filters and visuals interact correctly throughout the report.

## Key Performance Indicators

The dashboard tracks the following primary KPIs:

| KPI | Description |
|---|---|
| Total Transactions | Total number of recorded transactions |
| Total Transaction Value | Total monetary value of transactions |
| Unique Users | Number of distinct users |
| Success Rate | Percentage of successful transactions |

## DAX Measures

Example measures used in the dashboard:

```DAX
Total Transactions =
COUNTROWS('Transactions')
```

```DAX
Total Transaction Value =
SUM('Transactions'[Transaction_Value])
```

```DAX
Unique Users =
DISTINCTCOUNT('Transactions'[User_ID])
```

```DAX
Successful Transactions =
CALCULATE(
    [Total Transactions],
    'Transactions'[Payment_Status] = "Successful"
)
```

```DAX
Success Rate =
DIVIDE(
    [Successful Transactions],
    [Total Transactions],
    0
)
```

## Dashboard Analysis

### Transactions Over Time

A monthly trend analysis is used to monitor changes in transaction volume and transaction value and identify periods of higher or lower activity.

### Age Segment Contribution

Customer activity is analyzed across different age segments to understand their contribution to overall payment activity.

### Service Transaction Value

Transaction value is compared across payment services to identify the services generating the highest contribution.

### Top 5 Users

The dashboard identifies the top five users based on transaction value, providing visibility into high-value customer activity.

### Weekday vs. Weekend Usage

Transaction activity is compared between weekdays and weekends to identify differences in customer usage patterns.

## Dashboard Features

- Interactive month filter
- Payment status filter
- KPI cards
- Monthly transaction analysis
- Customer segmentation
- Service performance analysis
- Top 5 user analysis
- Weekday vs. weekend comparison
- Interactive cross-filtering
- DAX-based calculations
- Custom dashboard layout

## Project Workflow

```text
Raw Data
   ↓
Data Cleaning
   ↓
Data Transformation
   ↓
Data Modeling
   ↓
DAX Measures
   ↓
KPI Development
   ↓
Data Visualization
   ↓
Interactive Dashboard
   ↓
Business Insights
```

## Repository Structure

```text
digital-payments-analytics/
│
├── Dataset/
│   └── transactions.csv
│
├── Screenshots/
│   └── dashboard.png
│
├── Digital_Payments_Analytics.pbix
│
└── README.md
```

## Skills Demonstrated

**Power BI**
- Power Query
- DAX
- Data Modeling
- Interactive Reports
- KPI Development
- Data Visualization

**Data Analytics**
- Data Cleaning
- Data Transformation
- Trend Analysis
- Customer Segmentation
- KPI Analysis
- Business Reporting

## Key Takeaways

The dashboard provides a single view of payment performance and customer activity, making it easier to identify transaction trends, high-value users, service contribution, and usage patterns.

The project demonstrates the end-to-end Power BI workflow from **data preparation to business reporting**.

## Resume Description

**Digital Payments Analytics Dashboard | Power BI**

- Developed an interactive Power BI dashboard to analyze digital payment transactions, customer activity, service performance, and payment success rates.
- Cleaned and transformed transaction data using Power Query and created DAX measures for key performance indicators.
- Built interactive visualizations for transaction trends, customer segments, service-wise transaction value, top users, and weekday/weekend usage.

## Author

**Shaik Azaruddin**

Data Analyst | Power BI | SQL | Python | Excel | Tableau
