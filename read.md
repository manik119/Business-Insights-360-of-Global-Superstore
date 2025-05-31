# Global Superstore - 360° Business Insights Power BI Dashboard

## Guiding principle: "The best reports don’t look clever. They look obvious." The primary aim of this dashboard is to automate KPI tracking and provide a centralized, detailed view of business performance that allows for deeper dives when necessary.
## Business Problem:
The core business challenge is to effectively monitor and analyze multifaceted superstore operations to identify growth opportunities, mitigate risks, and optimize performance and automation across various departments. 

## Data Architecture
Conceptually, this project is best supported by a Snowflake Schema in the data warehouse.

Key Features & Technical Implementation: Parameters for Enhanced User Experience & Compactness.
* Category Filters: Parameters are used to allow users to filter the view by product categories (Technology, Furniture, Office Supplies) across multiple pages, making dashboards more compact and focused.
* Time Series Filters: Dynamic parameters (M/Q/Y buttons) enable switching chart views between Month, Quarter, and Year for trend analysis, providing clarity and flexibility without cluttering the dashboard. This design also enhances the scope for future automation of periodic reports.

## DAX Measures for Complex Calculations:
    * Time Intelligence: Extensive use of DAX time intelligence functions, such as `DATEADD`, `SAMEPERIODLASTYEAR`, `TOTALYTD/QTD/MTD` (conceptual, based on YoY, QoQ, MoM needs). 
      The importance of a comprehensive *Date Table* marked as such in Power BI is central to these calculations, enabling accurate comparisons like Sales Last Year (Sales LY), Profit Last Year (Profit LY), Month-over-Month (MoM) growth, and Quarter-over-Quarter (QoQ) growth.
    * KPI Development: Custom DAX measures were created for all key performance indicators, including:
        * YoY Growth % for Sales, Profit, Quantity, Orders (e.g., Total Sales +26.25% YoY).
        * Profit Margins (Overall, by Category, by Salesperson, by Product).
        * Average Order Value (AOV).
        * Median-based calculations for salesperson performance quadrants.

## Tech Stack:
* Power BI: Core tool for data modeling, DAX calculations, visualization, and dashboard creation.
* Power Query: Used within Power BI for data extraction, transformation, and loading (ETL) processes.
* Excel: Potential source for raw data or supplementary information.
* DAX Studio: Utilized for developing, testing, and optimizing complex DAX measures.

## Key Insights from the Dashboard:
* Critical Profitability Concern in Furniture: The Furniture category requires immediate attention for cost and price optimization, as its profit margins are notably low at 6.94%.
* Underperforming Salespeople Identified: Specific salespeople, consistently exhibit negative profit margins, averaging -21.87%, indicating a need for urgent review and intervention.
* Standout "Hero Product" Performance: The Canon imageCLASS 2200 copier is a significant "hero product," boasting an extremely high Average Order Value (AOV) of $12,319.96 and remarkable year-over-year sales growth of 137.8%.
