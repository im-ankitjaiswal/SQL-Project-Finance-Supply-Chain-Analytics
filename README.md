# Finance and Supply Chain Analytics for AtliQ Hardware

### Explanation of the Project

#### **About AtliQ Hardware:**  
AtliQ Hardware is a globally recognized company specializing in manufacturing PCs, printers, mice, and related computer hardware. Due to increasing data sizes and performance issues in Excel-based systems, AtliQ initiated this project to leverage MySQL as a database management system. The goal was to analyze data effectively, address inefficiencies, and derive actionable insights.

---

Here's a more concise and professional breakdown of the **Financial Analytics Project**:

---

### **Project Overview:**
This project involves creating a comprehensive financial analytics solution that focuses on **Net Sales Calculation** and optimizing performance for sales data retrieval. The goal is to analyze transaction data, calculate net sales by applying pre- and post-invoice deductions, and optimize query performance.

---

### **Key Concepts and Process:**

1. **Net Sales:** The revenue a company generates after accounting for discounts, returns, and allowances.
2. **Cost of Goods Sold (COGS):** Direct costs related to the production of goods sold, including materials and labor.
3. **Gross Margin:** A profitability metric calculated as the difference between net sales and COGS, indicating operational efficiency.
4. **Profit:** Final earnings after deducting all expenses (including operating costs, taxes, and interest).

---

### **Process:**

1. **Data Extraction:**
   - Pull sales data from tables like `fact_sales_monthly`, `dim_product`, and `fact_pre_invoice_deductions`.
   - Join these with relevant product and deduction tables for a comprehensive view.

2. **Net Invoice Sales Calculation:**
   - **CTE (Common Table Expressions)** are used to calculate **Net Invoice Sales** by factoring in gross sales and pre-invoice discounts.
   - Optimization is done to speed up data retrieval, reducing query time from 5 seconds to optimized performance.

3. **Post Invoice Sales & Final Net Sales Calculation:**
   - A **Database View** is created for post-invoice deductions and net sales to simplify reporting and streamline query performance.

4. **Stored Procedures:**
   - Developed **stored procedures** to automate repetitive tasks, such as generating monthly reports or calculating gross sales for specific customers (e.g., Chroma India).
   - Stored procedures offer flexibility by allowing parameterized queries to be executed for different customers.

---

### **Performance Optimization:**

1. **CTE Optimization:**  
   By using a **CTE** to calculate **Net Invoice Sales** in a modular way, the query performance improved significantly.
   
2. **Database Views:**  
   Replaced CTEs with **Database Views** to improve maintainability, simplify the query structure, and eliminate the need for physical table storage, ensuring faster execution.

3. **Final Report Creation:**  
   Created views such as `sales_postinv_discount` and `net_sales` to enable quick and accurate reporting on **Net Sales** without complex query construction.

---

### **Outcome and Insights:**

1. **Top Performing Markets & Customers:**  
   After calculating net sales, the project identifies the top-performing markets and customers, offering valuable business insights.

2. **Customer Segmentation:**  
   Reports and views are created to assess **Top Customers by Net Sales**, enabling targeted decision-making and strategy development.

---

This **Financial Analytics Project** uses database optimization techniques and advanced SQL functionality (e.g., **Stored Procedures**, **CTEs**, and **Views**) to efficiently process large-scale sales data and calculate key financial metrics like **Net Sales** for informed decision-making in sales and marketing.
