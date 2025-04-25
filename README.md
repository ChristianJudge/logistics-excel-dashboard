# Logistics Delivery Efficiency Dashboard (Excel Portfolio Project)

Welcome to my **Delivery Efficiency Dashboard** — a dynamic Excel-based analytics tool built to track, visualize, and optimize warehouse performance across key logistics KPIs.

This project demonstrates my ability to clean raw data, build automated calculations, construct multi-level pivot tables, and design a visually intuitive dashboard with KPIs and slicers for interactive reporting.

---

## Tools & Skills Demonstrated

- Microsoft Excel  
- Data Cleaning & Transformation  
- Advanced Formulas (`XLOOKUP`, `IFS`, `MAX`, `AVERAGEIFS`, etc.)  
- Pivot Tables  
- Slicers & Filters  
- KPI Dashboards  
- Dashboard Design & Layout Optimization

## Raw Data
![Alt text](https://github.com/ChristianJudge/logistics-excel-dashboard/blob/main/raw_data_ss.PNG)

## Data Cleaning Steps

Performed in the "Cleaned Data" sheet:
- Split dates into separate **Month**, **Day of Week**, and **Year-Month** fields using `TEXT()` function:
=TEXT(B2,"mmmm") / 
=TEXT(B2,"yyyy-mm") / 
=TEXT(B2,"dddd")
- Created **Delivery Category** using 'IF()' formula: =IF(G2<=24,"Fast",IF(G2<=72,"On Time","Delayed"))
- Order Delayed Category IF() formula: =IF(G2>72,"Yes","No")

![Alt text](https://github.com/ChristianJudge/logistics-excel-dashboard/blob/main/cleaned_data_ss.PNG)

## Pivot Tables

Created multiple pivot tables for deep operational insight:

- **Average Delivery Time by Month**
- **Average Delivery Time by Delivery Type**
- **Average Delivery Time by Warehouse**
- **Average Delivery Time by City**
- **Percentage of Orders Delayed**

![Alt text](https://github.com/ChristianJudge/logistics-excel-dashboard/blob/main/pivot_ss.PNG)
Each pivot table feeds into the dashboard and connects to slicers for interactivity.

## Interactive Dashboard

The dashboard is powered by the pivot tables and provides a detailed analysis of delivery performance, using pivot charts with slicers plus a KPI section in the top right.

Performed in the "Dashboard" sheet:
- Avg Delivery Time (hrs) KPI: =AVERAGE('Cleaned Data'!G2:G1001)
- % On-Time Deliveries KPI: =COUNTIFS('Cleaned Data'!J2:J1001,"No")/COUNTA('Cleaned Data'!J2:J1001)
- Fastest Warehouse KPI:
Helper cell - =XLOOKUP(AA4,'Pivot Tables'!F4:F6,'Pivot Tables'!E4:E6)
The 'Fastest Warehouse' box - =IFS(AA6="Warehouse A","A",AA6="Warehouse B","B",AA6="Warehouse C","C")



![Alt text](https://github.com/ChristianJudge/logistics-excel-dashboard/blob/main/dash_ss.PNG)

## Project Conclusion

This **Logistics Performance Dashboard** provides a comprehensive and interactive view of the company's delivery operations, offering insights into key performance metrics such as delivery time and late deliveries across different regions and warehouses.

By leveraging **Pivot Tables** and **KPI formulas**, the dashboard allows business stakeholders to:

- **Identify underperforming warehouses** that are affecting overall delivery efficiency.
- **Track delivery performance** over time and make data-driven decisions to improve operational efficiency.
- **Understand regional service breakdowns** to address delays in specific areas.
- **Enhance decision-making** with a data-driven approach to logistics, supporting continuous improvement in business strategy.

### Key Learnings:
- The use of **Excel Pivot Tables** and **Slicers** helped facilitate dynamic data analysis, allowing for quick insights into operational performance.
- Creating a **KPI Dashboard** helped highlight critical operational data points, making it easier for stakeholders to monitor and improve performance over time.
- This project showcased the value of **data visualization and interactivity** in business decision-making, demonstrating how dashboards can transform raw data into meaningful, actionable insights.

### Future Recommendations:
- Incorporating **real-time data updates** would ensure that the dashboard reflects the most up-to-date delivery information.
- Expanding the dashboard to include **predictive analytics** (e.g., forecasting delivery times based on historical trends) would further enhance its value to business users.
- Integrating data from **other systems** such as inventory management or customer feedback could provide a holistic view of the logistics process.

Overall, this dashboard not only simulates real-world logistics analytics but also provides a foundation for future business analysis and improvements in delivery operations.




