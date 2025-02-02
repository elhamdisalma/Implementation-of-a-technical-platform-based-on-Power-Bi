# Maven-Market Dashboard  

### Dashboard Link :https://um5sma-my.sharepoint.com/:u:/g/personal/salma_elhamdi2_um5_ac_ma/ETCmJPYrytdDtkjluN58kScBDE03qYJpCKNNnWk4KrFauw?e=zJ6o3n

## Problem Statement  

This dashboard enables Maven Market to analyze sales performance and better understand customer behavior. It provides insights into total transactions, revenue trends, and product performance, assisting in strategic decision-making.  

### Steps Followed   

- **Step 1**: Load data into Power BI Desktop. The dataset includes multiple sources, such as Excel files and databases.  
- **Step 2**: Open Power Query Editor. In the View tab under Data Preview, check "Column Distribution", "Column Quality", and "Column Profile" options.  
- **Step 3**: Ensure that column profiling is based on the entire dataset, not just the default 1000 rows.  
- **Step 4**: Check for errors and empty values. It was observed that no columns had errors or empty values, except for the column named "Return Rate".  
- **Step 5**: For calculating average values, null values were not considered as they constituted less than 1% of the data.  
- **Step 6**: In the report view, select a theme under the View tab to maintain visual consistency.  
- **Step 7**: Add a new visual to represent the total transactions by brand, utilizing various colors for easy identification.  
- **Step 8**: Integrate visual filters (Slicers) for key fields such as "Product Brand", "Customer Age", and "Transaction Date".  
- **Step 9**: Add card visuals to represent key metrics, such as total revenue and total transactions.  
- **Step 10**: Include a bar chart to display the performance of different brands, highlighting the top products.  
- **Step 11**: Use visualizations to represent customer demographics, including age and gender breakdowns.  
- **Step 12**: Insert text boxes to display the report title and key insights.  
- **Step 13**: Add shapes and logos to enhance the visual appeal of the report.  
- **Step 14**: Create calculated columns #### House Number Extraction :The following DAX code creates a new column **House Number**, which extracts the house number from the `customer_address` field in the `Customers` table.   

  ```DAX  
   House Number = LEFT('Customers'  [customer_address], SEARCH(" ", 'Customers'[customer_address], 1, 0) - 1)
![Image](https://github.com/user-attachments/assets/2c56e718-6a3f-4e8e-af4f-3a8debd1598e)


- **Step 15**: This measure calculates the total number of transactions by removing any existing filters on the `Transaction_Data` table.  

  ```DAX  
  All Transactions = CALCULATE([Total Transactions], ALL(Transaction_Data))

- **Step 16**: This measure classifies products into three price tiers—"High", "Mid", and "Low"—based on their retail price: 
   ```DAX  
    Price_Tier = IF(Products[product_retail_price] > 3, "High", IF(Products[product_retail_price] > 1, "Mid", "Low"))

- **Step 17**: This measure sums the total quantity of products returned from the Return_Data table:
   ```DAX  
   Quantity Returned = SUM(Return_Data[quantity])

- **Step 18**:This measure calculates the last day of the month for a given date in the Calendar table.
   ```DAX  
        End of Month = EOMONTH('Calendar'[date], 0)
        


#### Weekly Revenue Trending  
![Image](https://github.com/user-attachments/assets/69d09f55-1692-45bb-8bba-16066d98418b)

#### Total Transactions by Product  
![Image](https://github.com/user-attachments/assets/c228bd82-e1b1-4809-bc28-301dc5f1eec0)

#### Customer Performance Analysis  
![Image](https://github.com/user-attachments/assets/24df9069-cb23-443d-b71f-ffef8e128439)

![Image](https://github.com/user-attachments/assets/c041c9d3-8229-494f-8f6e-cb02518ae320)

#### Data Model Overview  
![Image](https://github.com/user-attachments/assets/cc3ccd5e-51a8-4794-845a-1f8b0f446d0b)

#### Total Transactions by Brand  

The **Total Transactions by Brand** table visualizes the total number of transactions for each product brand. Each color represents a different brand, allowing users to quickly identify the top-selling products. Brands are ranked based on transaction volume, providing a clear overview of performance across the product portfolio. This visual tool is essential for assessing brand effectiveness and identifying those that may require targeted marketing or optimization strategies.  

![Image](https://github.com/user-attachments/assets/c97c9631-a82c-4229-8d8d-c87489812bb6)


# Snapshot of Dashboard (Power BI Desktop)

![Image](https://github.com/user-attachments/assets/e9c1a7c2-4ed7-4820-b97c-4043431560d7)

![Image](https://github.com/user-attachments/assets/3ee26cfa-46b6-4f5e-ae11-4437468f725b)

![Image](https://github.com/user-attachments/assets/38408ae5-4411-4abe-a608-ae490a338c29)



- **Step 19**: Publish the report to Power BI Service for broader access.
![Image](https://github.com/user-attachments/assets/0992d13a-5346-45f8-bb62-a001e0c1bdd4)



# Insights  

Three pages, reports were created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;
### [1] Total Transactions  

   Total Transactions Recorded = 10,786  

   - **Top Brand by Transactions**: Hermanos with 513 transactions  
   - **Lowest Brand by Transactions**: Fort West with 302 transactions  

   Thus, "Hermanos" is the top-performing brand based on transaction volume.  

### [2] Weekly Profit Trends  

   - The current month profit stands at **$39,854.09**, with a profitable weekly trend showing consistent growth.  
   - Highest profit recorded was over **$20,000** during certain weeks highlighted in the graph.  

### [3] Total Revenue  

   - Current total revenue generated = **$143,465.26**  
   - **Top Customer**: Ida Rodriguez contributing notably to revenue.  

### [4] Profit Margin  

   - Average Profit Margin across brands = **59.86%**  
   - Highest Profit Margin = **63.31%** recorded by "Plato"  
   - Lowest Profit Margin = **59.86%** recorded by "Fort West"  

### [5] Customer Demographics  

   **Transactions by Gender**:   
   - Female Customers = 49%   
   - Male Customers = 50%  

   This indicates a balanced gender distribution among customers.  

### [6] Transactions by Age Group  

   - Majority of transactions are from the **26-35 age group**, followed closely by **36-45 age group**.  
   - The data reflects age diversity among the customer base, with a significant number of transactions coming from younger customers.  

### [7] Returns and Customer Behavior  

   - Current Month Returns = **474**, indicating some levels of dissatisfaction or product issues.  
   - Return Rate stands at **1.07%** which is relatively low.  

### [8] Performance Against Targets  

   - Current revenue target stands at **$6,640K**, and actual revenue is **$6,580K**, indicating a healthy performance against set goals.  


### Conclusion  

The Maven Market dashboard provides a comprehensive overview of sales performance and customer insights, enabling data-driven decision-making for enhanced business outcomes.

# Maven-Market.md.txt
Affichage de # Maven-Market.md.txt
