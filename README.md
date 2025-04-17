# Optimizing revenue by leveraging insights from top-selling products, customer behaviors and time-based revenue analysis.

## 1. Purpose and Outcome
**Purpose:**
- Identify the top-selling products
- Identify the customer behaviors: frequency, monetary and recency
- Identify time-based revenue (e.g Monthly, Weekday and Hour)
  
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
Follows steps in `Clean and Extract Data.ipynb` 

## 6. Data Analysis
### 6.1 Overall Statistics
![Overall](https://github.com/user-attachments/assets/22fea717-5ffc-46b3-b920-98872fb3f3a6)

- With a total online revenue of nearly £8.76 million in 2011, this company can be considered a strong performer among small to mid-sized e-commerce businesses of its time, despite accounting for a small fraction of the national e-commerce market (£6.1bil)
- Handling over 4,300 customers and 400,000 orders in 2011, the company demonstrates a significant operational scale for a non-store online retailer at the time, indicating both high customer activity and a steady volume of low-to-mid priced product sales.
- With approximately 3,800 distinct product codes, the company showcased a notably diverse product catalog for a non-store online retailer in 2011. Such breadth likely contributed to customer retention and positioned the business as a one-stop destination for gift-related items.
- United Kingdom dominates — local customer base is strongest. The largest share of revenue comes from UK-based customers. Other European countries represent strong export markets. Countries like the Netherlands, Ireland (EIRE), Germany, France, etc., contribute significantly.

### 6.2 TOP 10 Selling Products
![Top Selling 1](https://github.com/user-attachments/assets/ff0e1d6d-6258-4174-8668-c8554c6d2790)

![Untitled design](https://github.com/user-attachments/assets/ed889f2f-ce53-47de-b1a6-d685b6e38770)

#### 6.2.1 One product dominates both revenue and volume
`PAPER CRAFT , LITTLE BIRDIE`
- Highest Total Sales: £168,469.60
- Highest Quantity Sold: 80,995 units

**Insight:** This is clearly a hero product — both high-demand and high-revenue. It is cheap per unit (£2.08) but sells in bulk.
  
**Recommendation:** Ideal for bundling, promotion, or lead product campaigns.

#### 6.2.2 Some products have high revenue but aren’t high in quantity
  `REGENCY CAKESTAND 3 TIER`
  - No.2 in Total Sales (£142,592.95)
  - Not in Top 10 by Quantity
    
  **Insight:** This likely has a higher price per unit (£12.75), meaning fewer units sold but still generating big revenue.
    
  **Recommendation:** Good for highlighting premium offerings or gifting campaigns.
  
#### 6.2.3 Others are top in both lists (sweet spot products)
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

- `PAPER CRAFT, JUMBO BAG, STORAGE JAR`: Push volume, create bundles
- `REGENCY CAKESTAND` (luxury feel, gift packaging): Use premium positioning
- `HEART HOLDER, STORAGE JAR`: Ensure supply for fast-moving goods

### 6.3 Purchase behavior

We will segment customers based on Recency, which measures the number of days since each customer’s most recent purchase.

Reference date for calculating recency: one day after the last date in your dataset.

![Customer Behaviors 5](https://github.com/user-attachments/assets/91e98e31-c267-44d5-9ccc-efeb023311e9)

#### 6.3.1 Very Recent Segment (Recency from 0-30 days)

![0-30](https://github.com/user-attachments/assets/5cd1da4d-f3a3-490c-aced-8f431763b830)

**🔍 Insights:**

1. **High Engagement Group**
   - This segment is the largest, making up 37.54% of total customers
   - Likely contains both retail and wholesale customers
     
2. **Likely contributes strongly to revenue**
   - Since they’re recent purchasers and AOV is high ($519.62), this group likely generates a large share of recent revenue
     
3. **Overlap with high-frequency buyers**
   - Many of them may belong to the ≥ 30 Orders group (25.77%), making them key loyalty drivers
     
**💡 Recommendation for Very Recent Segment**

Keep nurturing to build loyalty and drive repeat purchases:
- For those with ≥30 orders → Invite to join loyalty program
- For one-time buyers → Offer next-purchase discounts, recommend relevant products

#### 6.3.2 Recent Segment (Recency from 31-90 days)

![30-91](https://github.com/user-attachments/assets/81edbb94-79bb-43fe-ba2c-0bc9833e600e)

**🔍 Insights**

1. **Moderately Engaged Group**
   - Purchase frequency = 3.10, showing they’ve bought more than once, but not frequently.
   - Likely includes both repeat retail customers and small wholesale buyers.

2. **Solid AOV but Lower than Very Recent**
   - AOV = $407.72 vs. $519.62 (Very Recent) and $429.53 (Inactive)
   - Suggests: this group is important for mid-level revenue and can be nudged to re-engage before they lapse

3. **At-risk of churn**
   - Recency is 31–90 days → this is the sweet spot for reactivation
   - These are not cold yet, but may soon become Lapsed or Inactive
     
**💡 Recommendations for Recent Segment**

1. **Re-engagement Campaign**

   Remind them of your brand before they forget
   
   Use email or retargeting with:

   "Haven’t seen you in a while — here’s 10% off your next order!"

2. **Highlight New or Seasonal Items**

   Suggest what’s changed since their last visit:

   "New arrivals you’ll love!"

   "Fresh stock just in for [season/event]"

3. **Loyalty Nudges**
   
   For customers with 3+ orders (esp. the 16% with ≥ 30 orders):
   - Offer loyalty program invitations
   - Encourage repeat buying habits

4. **Dynamic timing**

   Create an automated flow in your CRM or email system:

   - Target customers exactly at 45, 60, 75 days post-purchase with tailored offers

#### 6.3.3 Lapsed Segment (Recency from 91-180 days)
![91-180](https://github.com/user-attachments/assets/25234465-8eea-44d2-b6b4-7630139560ce)

**🔍 Insights**
1. **Moderately disengaged group**
   - Purchase frequency = 2.34: most of these customers purchased more than once, but not often
   - Many haven’t purchased in 3–6 months, so they're at risk of being lost

2. **Declining order value**
   - AOV is $337.81, lower than Recent ($407.72) and Very Recent ($519.62)
   - Indicates potential drop in interest, loyalty, or relevance of current products

3. **Smaller proportion of loyal buyers**
   - Only 4.5% have made ≥30 orders
   - Meanwhile, 9% are near one-time buyers (≤2 orders)

**💡 Recommendations for Lapsed Segment**
1. **Run targeted win-back campaigns**

   Use messaging like:

   “It’s been a while — here’s 20% off just for you!”

   Target them at 90, 120, and 150 days post last purchase

2. **Remind them of what they loved**
   
   Include items they purchased before or similar alternatives

   Add urgency: “Back in stock — limited quantity!”

3. **Test deeper discounts or bundles**

   Since this group shows fading interest, incentivize return with:
   - Bundled deals
   - Tiered discounts (e.g., save more when you buy more)

4. **Identify friction points**
   
   If possible, run a short survey:

   “We miss you — tell us how we can do better!”

   Helps uncover whether issues are product-related, delivery, or seasonal

#### 6.3.4 Inactive Segment (Recency >180 days)
![more than180](https://github.com/user-attachments/assets/064e28c6-727c-42ed-8e06-f318afb88f26)

**🔍 Insights**
1. **Lowest engagement across all segments**
   
   - Purchase frequency = 1.50 → majority are one-time or at most two-time buyers
   - Highest likelihood of churn or being permanently lost

2. **Surprisingly high AOV**
   - Despite being inactive, AOV = $429.53, which is higher than:
     - Lapsed ($337.81)
     - Recent ($407.72)
     
   - Suggests these may be one-time wholesale or gift buyers with large orders

3. **High unit price = high-value products**
   - Average unit price = $4.88, the highest among all segments
   - Indicates purchases may have been fewer items, but more expensive ones

**💡 Recommendations for Inactive Segment**
1. **Segment and target high-value one-timers**
   
   For those with high AOV, send personalized reminders like:
   "Enjoyed your last order? Here's something you'll love again."

2. **Reactivation with bold offers**
   
   Because these customers are far removed, test:
   - Flash sales
   - Bigger-than-normal discounts (e.g. 25–30%)
   - Exclusive 'back for a limited time' bundles

3. **Low-touch retention fallback**
   
   If they don't respond after multiple touchpoints:
   - Stop active marketing to reduce cost
   - Move them to low-frequency or seasonal-only email list

4. **Collect feedback (optional)**
   
   Run a short win-back survey:

   "Why haven’t you been back? We’d love to improve for you."

Sum up for Customer purchase behavior:
<img width="881" alt="Screenshot 2025-04-17 at 16 37 59" src="https://github.com/user-attachments/assets/e5ab9dae-029b-49ae-bc65-0214840fc04f" />

- Very Recent is the most active and valuable group (high frequency + AOV) → retain strongly

- Recent is still warm — perfect time to re-engage and upsell

- Lapsed shows declining behavior → needs win-back campaigns

- Inactive is mostly lost, but may include high-value one-timers → target selectively

### 6.4 Time-based analysis
#### 6.4.1 Monthly Revenue
![Time base 1](https://github.com/user-attachments/assets/e65891d3-9d4a-44cd-b2db-6342b08fed32)

**Insight:** 
- Revenue climbs steadily toward November (the peak month).
- Total quantity increased steadily in line with revenue throughout the year, while the number of orders remained relatively stable. This suggests that from January to July, the majority of customers were likely retail buyers, whereas from August to November, wholesale buyers became more dominant.
  
**Recommendations**

**- Segment Retail and Wholesale Strategies:**
  
 Develop separate marketing and pricing plans for retail (Jan–Jul) and wholesale (Aug–Nov) customers.

**- Target Wholesale Early:**

  Launch bulk-buy campaigns around July with incentives like free shipping or early access to holiday collections.

**- Optimize Inventory for Peak Season:**
  
 Stock up on high-demand items in advance of the Aug–Nov surge, especially for corporate and large-quantity orders.

**- Seasonal Messaging Focus:**
  
 Highlight personal gifting occasions in the first half of the year and shift to bulk and holiday themes in the second half.

 #### 6.4.3 Revenue by Weekday

![Time base 2](https://github.com/user-attachments/assets/1a1fcf52-340f-423f-a589-bfa7d4e2609f)

**Insight:** Tuesday and Thursday are top-performing days; Sunday is the weakest.

**Recommendations:**
- Launch new products or promotions on Tuesdays/Thursdays for maximum impact.
- Schedule ads/posts during these high-performing days using data-driven automation.
- Use Sunday for storytelling content (blog posts, behind-the-scenes) or light engagement → test content-driven brand touchpoints.

#### 6.4.3 Revenue by Hour

![Time base 4](https://github.com/user-attachments/assets/a6a5a783-6468-4d9d-8617-190162f5ea8d)

**Insight:** Most purchases happen between 9AM–2PM (UK time).

**Recommendations:**
- Schedule email blasts and promotions to hit inboxes between 8–9AM.
- Ad scheduling: Focus Facebook/Google ads budget between 9AM–2PM.
- Live chat/Customer support availability should prioritize this window.

## 7. Outcomes

To boost revenue from top-selling products, focus on promoting the hero item `PAPER CRAFT, LITTLE BIRDIE` through bundles, bulk discounts, and prominent ad placement. Leverage high-value products like the `REGENCY CAKESTAND 3 TIER` with premium positioning and gift-focused campaigns. Strengthen consistent sellers by cross-selling them in bundles and featuring them in seasonal promotions. Ensure stock availability, monitor monthly bestsellers, and optimize packaging to support repeat purchases and increase average order value.

Customers are segmented into four groups based on recency: Very Recent (0–30 days), Recent (31–90 days), Lapsed (91–180 days), and Inactive (>180 days). The Very Recent segment is the most engaged, with the highest purchase frequency and order value, making them ideal for loyalty-building and upsell strategies. The Recent group remains active but requires timely follow-up to prevent churn. Lapsed customers show declining engagement and should be targeted with win-back offers and reminders. Meanwhile, the Inactive group includes mostly one-time buyers; reactivation efforts should focus on high-value individuals, while others can be deprioritized to optimize resources.

The time-based revenue analysis reveals that sales peak in `November`, likely driven by wholesalers and holiday shopping; `Tuesdays and Thursdays` are the most active purchase days, while Sundays see the least activity; and most purchases occur between `9AM and 2PM`. To optimize performance, the company should focus marketing campaigns and promotions around `Q4`, especially October, schedule email and ad pushes during `weekday mornings`, and prioritize high-engagement days for new launches. Meanwhile, Sundays can be used for softer, brand-building content or experimentation.

