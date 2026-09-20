# Operations Information System for Production Management

## Overview

Designed and implemented an information system from scratch to centralize operational data and support decision-making within a production management area.

Before the solution was implemented, operational information was dispersed across different Excel files and individual controls maintained by process owners. Production and machine performance information was not readily available for management, and data had to be collected manually through phone calls and individual reports.

The solution integrated data capture, data storage, automation and business intelligence using Microsoft Power Platform, SQL and Power BI.

## Business Challenge

The management area did not have a centralized information system to monitor daily operations.

Key information such as:

* Daily production
* Production by shift
* Production by operator
* Production by machine
* Machine downtime
* Supply consumption

was managed independently by different process owners, mainly through Excel files.

Additionally, some operational data was stored in other systems and had to be manually exported to Excel before it could be analyzed.

This made it difficult for management to obtain timely and consistent information for decision-making.

## Solution

I designed and built an integrated information solution from scratch.

The first stage consisted of developing a Power Apps application that functioned as an ERP-like operational data capture system. Operators could register production information, machine downtime and supply consumption directly through the application.

The data was stored in SharePoint Lists, which served as the initial data repository.

The data repository was then connected to Power BI, where I designed the data model, created relationships and developed analytical reports that were periodically refreshed.

Power Automate was also incorporated to automate data management tasks, including backups and data cleaning processes to help manage SharePoint storage capacity.

### Second stage: SQL integration

A second stage expanded the solution by integrating data from a SQL database belonging to software used in one of the production processes.

Instead of requiring users to manually access the software and export Excel reports, I extracted the data from the SQL database using queries and connected it to Power BI datasets.

This allowed users to access updated information directly through Excel and Power BI without repeating the previous manual extraction process.

## Architecture


                  OPERATIONAL PROCESSES
                           │
             ┌─────────────┴─────────────┐
             │                           │
        Power Apps                   SQL Database
             │                           │
             ▼                           ▼
    SharePoint Lists              SQL Queries
             │                           │
             └─────────────┬─────────────┘
                           ▼
                      Power BI
                           │
                  Data Modeling
                           │
                           ▼
                  Reports & Datasets
                           │
             ┌─────────────┴─────────────┐
             ▼                           ▼
        Management                   Excel Users
       Decision-Making             Data Consultation

Power Automate → Backups & Data Management
```

## Technologies

* Microsoft Power Apps
* Microsoft Power Automate
* Microsoft Power BI
* SharePoint
* SQL
* Excel
* DAX / Data Modeling

## My Contribution

* Analyzed the information and reporting needs of the production area.
* Designed the information architecture of the solution.
* Developed the Power Apps application for operational data capture.
* Designed the SharePoint-based data repository.
* Built Power BI data models and relationships.
* Developed analytical reports and dashboards.
* Automated backup and data-cleaning processes using Power Automate.
* Integrated SQL database information into Power BI.
* Developed SQL queries for data extraction.
* Connected Power BI datasets with Excel for easier access to updated information.
* Designed the solution with a focus on reducing manual information handling and improving data availability.

## Impact

The project established a centralized information system where previously there was no integrated solution for management.

The solution enabled:

* Centralized access to operational information.
* Greater visibility into production and machine performance.
* Faster access to updated information.
* Reduced dependence on manual Excel-based reporting.
* Automated data management tasks.
* Easier access to information for decision-making.
* Integration between operational data sources and business intelligence tools.

## Portfolio Note

This project was developed in a real industrial environment. Due to confidentiality considerations, company data, internal files, databases and proprietary application screens are not included in this repository.

The project description focuses on the solution architecture, technologies used and my individual contribution.
