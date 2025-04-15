# Optimizing revenue by leveraging insights from top-selling products, customer behaviors and time-based revenue analysis.

## 1. Purpose and Outcome
**Purpose:**
- Identify the top-selling products
- Identify the customer behaviors: frequency, monetary and recency
- Identify time-based revenue (e.g Monthly, Weekday and Hour)
- 
**Outcome:**
- Determine which products sell the most and suggest approaches to further increase their sales.
- Understand how customers behave to create effective campaigns for each group.
- Explore time-based revenue trends to optimize customer outreach timing.

## 2. Technologies Used
**Python:**
- Clean data
- Extract cleaned data

**Power BI:**
- Analyse the dataset extracted from Python to get insights
- Visualize key insights

## 3. Data Sources
The dataset for this study originates from data.world and can be found publicly on Kaggle

Dataset: https://www.kaggle.com/datasets/thedevastator/online-retail-transaction-data

## 4. Data Overview
**Dataset Name:** UK Online Retail Sales and Customer Transaction Data

**Description:** 
- **InvoiceNo:** A 6-digit number uniquely assigned to each transaction. If the number is prefixed with 'c', it indicates a cancellation.
- **StockCode:** A unique identifier for each product sold by the retailer.integral numbers
- **Description:** The name or a brief description of the product.
- **Quantity:** The number of units of the product sold in each transaction.
- **InvoiceDate:** The date and time when the transaction was made.
- **UnitPrice:** The price per unit of the product in sterling.
- **CustomerID:** unique number assigned to each customer
- **Country:** The country where the customer resides.
  
**Data Uses:** This dataset enables rich insights into wholesaler behavior, supporting inventory management, trend analysis for comprehensive retail analysis.

## 5. Data Cleaning:
Follows steps in `Cleaning and Extracting Data.ipynb` 

## 6. Data Analysis
### 6.1 Overall Statistics
![Overall](https://github.com/user-attachments/assets/fd534275-08a2-48af-9fb7-6d8de63a1dc2)

- With a total online revenue of nearly £8.76 million in 2011, this company can be considered a strong performer among small to mid-sized e-commerce businesses of its time, despite accounting for a small fraction of the national e-commerce market
- Handling over 400,000 transactions in 2011, the company demonstrates a significant operational scale for a non-store online retailer at the time, indicating both high customer activity and a steady volume of low-to-mid priced product sales.
- With approximately 3,800 distinct product codes, the company showcased a notably diverse product catalog for a non-store online retailer in 2011. Such breadth likely contributed to customer retention and positioned the business as a one-stop destination for gift-related items.
- United Kingdom dominates — local customer base is strongest. The largest share of revenue comes from UK-based customers. Other European countries represent strong export markets. Countries like the Netherlands, Ireland (EIRE), Germany, France, etc., contribute significantly.

### 6.2 TOP 10 Selling Products
![Top Selling 1](https://github.com/user-attachments/assets/ff0e1d6d-6258-4174-8668-c8554c6d2790)

![Untitled design](https://github.com/user-attachments/assets/ed889f2f-ce53-47de-b1a6-d685b6e38770)

  #### 6.2.1 One product dominates both revenue and volume
  `PAPER CRAFT , LITTLE BIRDIE`
  - Highest Total Sales: £168,469.60
  - Highest Quantity Sold: 80,995 units
  
  **Insight:** This is clearly a hero product — both high-demand and high-revenue.
  It is cheap per unit (£2.08) but sells in bulk.
  
  **Recommendation:** Ideal for bundling, promotion, or lead product campaigns.

  #### 6.2.2 Some products have high revenue but aren’t high in quantity
  `REGENCY CAKESTAND 3 TIER`
  - No.2 in Total Sales (£142,592.95)
  - Not in Top 10 by Quantity
  - 
  **Insight:** This likely has a higher price per unit (£12.75), meaning fewer units sold but still generating big revenue.
    
  **Recommendation:** Good for highlighting premium offerings or gifting campaigns.
  
#### 3. Others are top in both lists (sweet spot products)
These are consistent high performers:

`WHITE HANGING HEART T-LIGHT HOLDER (£2.55)`

`JUMBO BAG RED RETROSPOT (£1.95)`

`MEDIUM CERAMIC TOP STORAGE JAR (£1.25)`

**Insight:** These are fast-moving, well-priced, and widely liked.
**Recommendation:**
- Keeping high stock
- Creating bundles
- Featuring them in ads
  
**Sum up strategic takeaways for top-selling products:**

- PAPER CRAFT, JUMBO BAG, STORAGE JAR: Push volume, create bundles
- REGENCY CAKESTAND (luxury feel, gift packaging): Use premium positioning
- HEART HOLDER, STORAGE JAR: Ensure supply for fast-moving goods

### 6.3 Purchase behavior
#### 6.3.1 Customer Recency
This will calculate the number of days since each customer’s last purchase.
Determine a reference date for recency (one day after the last date in your dataset).

![Customer Behaviors 5](https://github.com/user-attachments/assets/91e98e31-c267-44d5-9ccc-efeb023311e9)

| Segment  | Recency (Days) | Interpretation  | Recommended Action |
| ------------- | ------------- | ------------- | ------------- |
| Very Recent  | 0-30 days  | Actively engaging  | Offer loyalty or referral deals  |
| Recent  | 31–90 days  | Recently interacted  | Send personalized promotions  |
| Lapsed  | 91–180 days  | At risk of churn  | Target re-engagement campaigns  |
| Inactive  | >180 days  | Possibly lost  | Win-back strategies  |

#### 6.3.2 Customer purchase frequency
