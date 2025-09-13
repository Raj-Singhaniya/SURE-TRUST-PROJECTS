# SURE-TRUST-PROJECTS
This repository contains three projects : Power BI mini project, Power BI Major Project, SQL Major Project
# Power BI Mini Project: Vehicle Sales Analysis
Sales Dashboard using Power BI Vehicle Sales Analysis- Power BI Mini Project This project presents an interactive Sales Dashboard built in Power BI, providing key insights into sales performance, deal sizes, regional trends, and product categories. It is ideal for business users, analysts, or managers looking to visualize and explore company sales data in a dynamic and user-friendly way. Dashboard Overview Page 1-Executive Summary KPIs: 🧾 Total Sales: 10.03M 📦 Total Quantity Sold: 99K 💰 Gross Margin: 48.15K

Visuals: 📈 Sales Trend Over Time (Line Chart) 🧮 Sales vs Deal Size (Pie Chart) 🖼️ Visual branding/images for engagement

Page 2 – Detailed Analysis

Visuals: Total Sales by Territory and Status (Stacked Bar) Countries with Maximum Orders (Donut Chart) Product vs Price vs Sales (Matrix Table) Order Volume by Product Code (Bar Chart) Sales by City (Geo Map): Includes tooltip showing NYC sales as $396,718.33.
*******************************************************************************************************************************************
# Retail Store Analysis Dashboard (Power BI Major Project)
Dashboard Overview 
The dashboard is divided into two interactive pages: Metric Value 💰 Total Revenue 242.70M 🧾 Total Orders 1000 🎁 Total Discount 27.62M 📦 Avg Order Value 242.70K 📈 Visuals:

Sales vs Category (Pie Chart) Electronics: 64.37% Accessories: 19.88% Furniture: 15.75% 📷 Store Image: "Smart Bazaar" branding Custom Icons and Visual Theme

📄 Page 2 – Detailed Sales Analysis 📊 Visuals: Sales by Customer Name (Bar Chart) Total Orders by Age Group (Bar Chart) Sales & Revenue by Month (Combo Chart) Sales by Payment Type (Donut Chart) Total Revenue vs State (Map) Total Discount (KPI) Stock Value Count (KPI) 💡 Uses filters by Quarter for dynamic analysis.
*******************************************************************************************************************************************
# SQL Major Project: Meeting_Feedback

Automated system to collect feedback via Google Forms, match it with Google Meet attendance data, and track processing status using a MySQL database. Designed for automation via Pabbly Connect and scheduled matching via a cron job. System Workflow: 
Feedback Collection
Google Form is used to collect participant feedback.
Responses are stored automatically in a linked Google Sheet.
Automated Sync: Feedback → MySQL
Pabbly Connect scheduled workflow:
Triggers every 1 hour.
Iterates over new rows in the feedback Google Sheet.
Inserts each row into the feedback table in FreeSQLDatabase.
Google Meet Attendance
Google Meet generates an attendance report after a session.
This data is exported to a separate Google Sheet.
Automated Sync: Attendance → MySQL
A separate Pabbly Connect workflow:
Iterates over the attendance sheet.
Inserts rows into the attendance table in the same MySQL database.Matching Job (Cron Script)
A scheduled Python script runs every hour:
Fetches all unprocessed feedback (processed = 0).
Attempts to match feedback email with attendance email.
If matched:
Updates processed = 1
Stores the matched_attendance_id
If not matched:
Logs an error in the error_log column
