# **US Debt Tracker Project**

## **Scenario**
A small debt agency in Washington, D.C. specializing in market debt analysis has been commissioned by the **U.S. Government** to analyze **public and governmental debt** and answer key questions regarding debt trends and projections.

## **Data Dictionary**
- **Debt Held by the Public** - US public debt owned by individuals, corporations, foreign government
- **Intragovernmental Holdings** - US public debt held by other US government agencies
- **Total Public Debt Outstanding** -  The sum of the Debt Held by the Public and Intragovernmental Holdings.

## **Key Questions Addressed**

1. What is the **Year-over-Year Percentage Increase** in debt?
2. Which **months historically show the highest and lowest** Total Debt increases?
3. What is the **projected growth** of publicly held debt in the next few years?

## **Data Cleaning Process**

**Purpose**: The raw dataset is not structured for **Pivot Table analysis** due to uts **7000+ columns**.

**Steps Taken**:

✅ **Transpose data** – Convert vertical headers to horizontal.  
✅ **Format cells** – Improve readability.  
✅ **Apply filters** – Enable efficient data exploration.  
✅ **Remove blank rows** – Eliminate unnecessary data.  
✅ **Replace null values** – Use **Ctrl+H** to clean missing entries.  
✅ **Adjust number formats** – Convert scientific notation to standard numbers.  

---

## **Questions 1: Yearly Debt Percentage Increase**
📌 **Approach**
- Extract **year-end debt values** for **2015–2023**.  
- Since **2023** only contains **two months of data**, the last available value (February) is used.  
- Calculate **percentage change** for Debt Held by the Public, Intragovernmental Holdings, and Total Public Debt Outstanding:

  ```
  Percentage Change = (Current Year Debt - Previous Year Debt) / Previous Year Debt * 100
  ```

📊 **Visualization**: **Line Chart**  

🔍 **Insights**:  
- From **2016 to 2019**, the average annual debt increase was **~5%**.  
- **2020** saw a **sharp spike** in debt, likely due to **pandemic response measures**.  

---

## **Question 2: Monthly Debt Trends**  
📌 **Approach**  
- Extract **month** from Record Date using `MONTH()` function.  
- Create a **Pivot Table**:  
  - **Rows:** Month  
  - **Values:** Average Total Public Debt Outstanding  

📊 **Visualization**: **Bar Pivot Chart**  

🔍 **Insights**:  
- **Highest debt increase months**: **January, February, November, and December**.  
- **Lowest debt increase months**: **April, May, June, and July**.  
- **Possible explanation**:  
  - **High-spending months** (holidays like Thanksgiving & Christmas) may lead to **increased borrowing**.  
  - **Low-spending months** with fewer holidays see **reduced borrowing activity**.  

---

## **Question 3: Debt Growth Projection (2023–2027)**  
📌 **Approach**  
- Create a **Pivot Table**:  
  - **Rows:** Year  
  - **Values:** Max Debt Held by the Public  
- **Remove years with null values**.  
- Use `FORECAST.ETS()` to **predict debt growth** for **2023–2027**.  

📊 **Visualization**: **Stacked Area Chart**  

🔍 **Insights**:  
- **1997–2007**: Publicly held debt increased by **$1T**.  
- **2008–2019**: Debt rose from **$6T → $17T**.  
- **2020–2022**: Debt surged from **$21.5T → $25T**.  
- **2023–2027 Projection**: Debt is expected to **reach $33T**, continuing a **steady growth trend**.  
- **Further research areas**:  
  - **Stock Market trends**   
  - **Housing Market fluctuations**   
  - **Credit Card spending patterns**   
  - **Unemployment rate impact**   

---

### **Conclusion**  
This project analyzes **historical and projected trends** in U.S. public debt using **Excel-based data transformation, calculations, and visualization techniques**. The findings highlight **key economic factors influencing debt growth**, providing valuable insights for policymakers and financial analysts.










