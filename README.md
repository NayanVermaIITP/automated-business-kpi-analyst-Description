# Automated Business KPI & Performance Analyst

An end-to-end business analytics automation built with n8n that transforms raw sales data into automated KPI analysis, business insights, and management-ready reports.

## Project Overview

Businesses often spend significant time manually cleaning data, calculating KPIs, analyzing performance, and preparing reports.

This project automates that entire workflow.

The system takes raw sales data from Google Sheets, validates the data, calculates important business KPIs, analyzes category and monthly performance, uses Gemini AI to generate business insights, and automatically sends the final report through Gmail.

## Workflow

Google Sheets
      ↓
Data Validation
      ↓
KPI Calculations
      ↓
Overall Business KPIs
      ↓
Category Performance
      ↓
Monthly Performance
      ↓
Data Quality Analysis
      ↓
Gemini AI Business Analyst
      ↓
Automated Gmail Report

## Key Features

- Automated data validation
- Revenue analysis
- Cost analysis
- Marketing spend analysis
- Gross profit calculation
- Net profit calculation
- Net profit margin
- Overall ROAS
- Category-level performance analysis
- Monthly performance analysis
- Data quality monitoring
- AI-generated business insights
- Automated management report
- Scheduled workflow execution
- Automated email delivery

## Data Quality Testing

To test the robustness of the workflow, I intentionally introduced data-quality issues into a dataset containing 500 records.

Results:

| Metric | Result |
|---|---:|
| Total Records | 500 |
| Valid Records | 491 |
| Invalid Records | 9 |
| Data Quality Rate | 98.2% |

The workflow successfully identified the invalid records before performing the business analysis.

## KPIs Calculated

### Revenue

Total revenue generated from valid business records.

### Gross Profit

Revenue minus Cost.

### Net Profit

Revenue minus Cost minus Marketing Spend.

### Net Profit Margin

Net Profit as a percentage of Revenue.

### Overall ROAS

Total Revenue divided by Total Marketing Spend.

Using overall totals instead of averaging individual order-level ROAS provides a more meaningful business-level marketing efficiency metric.

## AI Business Analysis

After the numerical analysis is completed, the workflow sends the structured results to Gemini AI.

The AI generates a management-level report containing:

- Executive Summary
- Key Performance
- Category Insights
- Monthly Trend
- Data Quality
- Business Observations
- Recommended Areas to Investigate

The AI is instructed to use only the calculated workflow data and avoid inventing business metrics.

## Technology Stack

- n8n Cloud
- Google Sheets
- Google Gemini
- Gmail
- No-code workflow automation

## Development Journey

I spent approximately **20 days learning n8n** before starting this project.

After learning the fundamentals, I spent **2 days building the complete workflow**.

The goal was not to create another basic tutorial automation, but to build a practical business analytics system that could demonstrate how automation, data analytics, and AI can work together.

## What I Learned

Through this project, I learned how to:

- Design multi-branch n8n workflows
- Validate business data automatically
- Build KPI calculations
- Aggregate analytical data
- Combine multiple workflow branches
- Structure data for AI analysis
- Use AI for business reporting
- Automate report delivery
- Build an end-to-end analytics automation

## Project Structure

```text
automated-business-kpi-analyst/
│
├── README.md
│
├── workflow/
│   └── automated-business-kpi-analyst.json
│
├── screenshots/
│   ├── workflow.png
│   ├── validation.png
│   ├── kpi-analysis.png
│   └── ai-report.png
│
└── sample-data/
    └── business_sales_sample.csv
