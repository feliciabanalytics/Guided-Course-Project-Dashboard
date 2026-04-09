# Adventure Works KPI Dashboard
A comprehensive Power BI dashboard analyzing the peformance of Adventure Works, a cycling equipment and accesories manufacturer, translating transation and sales data into actionable KPIs ( sales, revenue, profit, & returns), product level trends, and high-value customer insights. 

## Executive Summary Page
<img width="950" height="536" alt="image" src="https://github.com/user-attachments/assets/f043666e-7c6f-4071-8c8f-5635b4293f31" />

## Country Page
<img width="962" height="539" alt="image" src="https://github.com/user-attachments/assets/0d8e3584-8d17-42ab-bfcd-ebef35a9fc94" />

## Product Detail Page
<img width="1002" height="567" alt="image" src="https://github.com/user-attachments/assets/6d2099fc-123f-486b-9819-db1c60f37e23" />


## Customer Detail Page
<img width="818" height="464" alt="image" src="https://github.com/user-attachments/assets/c3a62cfb-02cc-4a5e-b052-888f20fc1af9" />

## Dashboard Features
- KPI Cards
- Interactive Slicers
- Drill Through Capabilities
- Conditional Color Formatting
- Target Guage Comparison
- Adjustment Scenario 
- Interactive Map Vizualization
  
## DAX Calculations
- Total Orders = DISTINCTCOUNT('Sales Data'[Order Number])
- Total Revenue = SUMX('Sales Data','Sales Data'[Order Quanity]*RELATED('Product Lookup'[Product Price])
- Total Cost = SUMX('Sales Data','Sales Data'[Order Quanity]*RELATED('Product Lookup'[Product Cost])
- Total Profit = [Total Revenue] - [Total Cost]
- Total Returns = Count('Returns Data'[Return Quantity]
- Return Rate = DIVIDE( [Quantity Returned],[Quanity Sold],"No Sales")
- Quantity Returned = SUM('Returns Data'[Return Quantity']
- Quanity Sold = SUM('Sales Data'[Order Quanitiy])
- Previous Month Orders = CALCULATE ([Total Orders], DATEADD('Calendar Lookup'[Date],-1,MONTH)
- Previous Month Revenue = CALCULATE ([Total Revenue], DATEADD('Calendar Lookup'[Date],-1,MONTH)
- Previous Month Profit = CALCULATE ([Total Profit], DATEADD('Calendar Lookup'[Date],-1,MONTH)
- Previous Month Returns = CALCULATE ([Total Returns], DATEADD('Calendar Lookup'[Date],-1,MONTH)
- 
