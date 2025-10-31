# **USA Regional Sales Analysis (EDA)**

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/USA%20Regional%20Sales%20Analysis.png)

## 🗂️ **Project Summary**

This EDA notebook provides an in-depth exploration of **Acme Co.’s 2014–2018 U.S. sales dataset**, covering data quality, trends, and customer insights to uncover key business patterns and opportunities.

#### 🔍 *Key Focus Areas:*

- **Data Profiling & Cleaning:**  

  Verified schema integrity, handled missing budget values, and standardized data types for accurate analysis.

- **Univariate & Bivariate Analysis:**  

  Explored revenue, profit margin, and unit price distributions; analyzed breakdowns by product, channel, and region.

- **Trend & Seasonality:**  

  Visualized monthly and yearly sales performance to highlight recurring peaks, dips, and seasonal trends.

- **Outlier Detection:**  

  Identified and examined extreme transactions on both ends of the revenue and unit-price ranges.

- **Correlation & Segmentation:**  

  Analyzed relationships among key metrics and segmented customers based on revenue versus profit margin.

💡 *This analysis serves as a foundation for improving sales strategy, optimizing profitability, and enhancing customer targeting.*

## ❓**Problem Statement**

Analyze Acme Co.’s 2014–2018 sales performance to pinpoint the key drivers of revenue and profitability across products, channels, and regions. Identify seasonality and outlier behavior, evaluate results against budget targets, and leverage these insights to optimize pricing strategies, promotional efforts, and market expansion initiatives—ultimately supporting sustainable growth while reducing customer and product concentration risk.

## 🎯 **Objective**

Deliver actionable insights from Acme Co.’s 2014–2018 sales dataset to:

✅ Identify top-performing **products**, **channels**, and **regions** driving revenue and profit  
✅ Detect **seasonal trends** and **anomalies** to improve demand planning  
✅ Spot **pricing** and **margin risks** stemming from outlier transactions  
✅ Inform **pricing**, **promotion**, and **market expansion** strategies  

These findings will guide the design of a **Power BI dashboard** that supports:
- Data-driven strategic decisions
- Improved forecasting accuracy
- Sustainable revenue growth

## 📊 **Exploratory Analysis**

### 🔹 *1. Monthly Sales Trend Over Time*

- **Goal:** Track revenue trends over time to identify seasonality, growth patterns, and sales spikes.

- **Chart Type:** Line Chart

- **EDA Category:** Temporal (Time Series)

- **Visualization Structure:** Line with markers to highlight monthly revenue points for improved clarity and comparison.

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Monthly%20Sales%20Trend.png)

#### 🔍 **INSIGHTS:**

- **Consistent Seasonal Pattern:** Sales cycle between **$24M - $26M**, with recurring peaks in **May–June** and troughs in **January**.
  
- **Stable Year-Over-Year Trend:** The revenue curve remains steady across the observed period, indicating predictable seasonal demand.
  
- **Notable Outlier:** An unexpected revenue drop in **early 2017** suggests a potential anomaly. This may warrant investigation into factors such as market disruptions, supply constraints, or poorly timed promotions.

### 🔹 *2. Total Monthly Sales Trend (Excluding Year 2018)*

- **Goal:** Reveal overall seasonality trends by aggregating sales for each calendar month across all years.
  
- **Chart Type:** Line chart
  
- **EDA Category:** Temporal (Time Series)
  
- **Structure:** Line plot with markers, ordered from **January → December** using month number for correct chronological sequencing.

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Overall%20Monthly%20Sales%20Trend.png)

#### 🔍 **INSIGHTS:**

- **January** starts strong at approximately **99M** in revenue.
  
- A **steady decline** follows through **April**, reaching the annual low of around **95M**.

- Sales **rebound** in **May** and **August**, climbing to roughly **102M**.
  
- From **September to December**, revenue stabilizes into a **99M–101M plateau**.

**Overall Pattern:**  
A recurring cycle featuring a **post–New Year surge**, a **spring dip**, and a **mid-summer bump** consistently appears across all calendar years.

### 🔹 *3. Top 10 Products by Revenue (in Millions)*

- **Goal:** Identify the **highest-grossing products** to prioritize marketing, inventory planning, and sales strategy efforts.

- **Chart Type:** Bar Chart

- **EDA Type:** Univariate Analysis

- **Structure:**

  - Bars are sorted in descending order to display the Top 10 products.
  - Revenue values are scaled in millions (USD) for clarity and comparison.

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Top%2010%20products%20by%20Revenue.png)

#### 🔍 **INSIGHTS:**

- **Products 26 and 25** lead significantly with revenues of **117M** and **109M**, respectively.  
    
- A sharp decline follows, with **Product 13** at **78M**, and a mid-tier cluster ranging between **67–78M**.  
    
- The **bottom four products** group tightly around **52M–57M**, suggesting consistent but limited performance.  

### 🔹 *4. Bottom 10 Products by Revenue (in Millions)*

- **Goal:** Identify the **lowest-performing products by revenue** to uncover potential areas for improvement in product strategy and sales focus.

- **Chart Type:** Bar chart

- **EDA Category:** Univariate Analysis

- **Structure:** Bars sorted in **ascending order** to display the **bottom 10 products by total revenue (in millions USD)**, highlighting products with the lowest sales performance for targeted optimization.

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Bottom%2010%20products%20by%20revenue.png)

#### 🔍 **INSIGHTS:**

- Products **24** and **9** record the **lowest revenues**, both around **14.6M**, marking the weakest performers.
  
- A gradual rise is observed among **Products 29** and **22**, reaching approximately **15M–16M**.

- Mid-tier performers such as **Products 7** and **10** achieve revenues around **17M–18M**, indicating moderate but stable sales.

- The top of this bottom group — **Products 27, 30, 23, and 21** — cluster between **18M–19M**, showing slightly stronger performance yet still trailing significantly behind higher-revenue products.

- Overall, the **revenue gap across the bottom 10** remains narrow **(≈ 14M–19M)**, suggesting uniformly low contribution and potential candidates for product rationalization or marketing support.  

### 🔹 *5. Total Sales by Channel*

- **Goal:** Show the **distribution of total sales across different channels** to identify the **most dominant sales routes**.

- **Chart Type:** Pie Chart

- **EDA Category:** Univariate Analysis

- **Structure:** Pie segments labeled with **percentages**, distinct **colors for clarity**, and an **adjusted start angle** for visual balance.

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Total%20Sales%20by%20Channel.png)

#### 🔍 **INSIGHTS:**  

- **Wholesale** dominates with **54%** of total sales, followed by **Distributors (~31%)** and **Exports (~15%)**, highlighting a strong dependence on domestic bulk channels.
  
- To **reduce concentration risk** and **diversify revenue streams**, focus on **expanding export operations** through targeted **international marketing** and **strategic partnerships**.

### 🔹 *6. Top 10 Products by Avg Profit Margin (USD)*

- **Goal:**  Compare **average profitability across products** to pinpoint **high-margin performers** driving profitability.  

- **Chart Type:**  Horizontal Bar Chart

- **EDA Category:**  Univariate Analysis

- **Structure:**  Bars are **sorted in ascending order** to display the **top 10 products** ranked by their **average profit margin (USD)**.

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Top%2010%20products%20by%20average%20profit%20margin.png)

#### 🔍 **INSIGHTS:**  

- **Products 18 and 28** lead with average profit margins of approximately **8.1–8.5K USD**, followed closely by **Products 5 and 11** around **7.9K USD**.
  
- **Mid-tier performers** such as **Products 12, 26, and 21** cluster within the **7.4–7.5K USD** range.

- The **bottom tier** — **Products 4, 16, and 1** — show lower margins around **7.3K USD**.  

💡 **Recommendation:**  
Analyze cost structures and pricing strategies of the **top-margin products** to replicate success and **improve overall product profitability**.

### 🔹 *7. Average Order Value (AOV) Distribution*

- **Goal:**  Understand the **distribution of order values** to identify **typical customer spending levels** and detect **potential outliers**.

- **Chart Type:**  Histogram

- **EDA Category:**  Univariate

- **Structure:**

    - **50 bins** representing order value ranges  
    - **Colored bars** with contrasting **edge highlights** for clear visibility  
    - Shows the **frequency distribution** of order values across all transactions

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Distribution%20of%20Average%20order%20value.png)

#### 🔍 **INSIGHTS:**  

- The **order value distribution** is **right-skewed**, indicating that most orders fall within the **20K–120K** range.
  
- A distinct **mode** is observed around **50K–60K**, representing the most common order size.
  
- A **long tail** stretches toward **400K–500K**, reflecting a small number of **high-value transactions** that, while infrequent, contribute significantly to total revenue.

- This suggests a **concentrated mid-range demand** with occasional large orders driving top-line spikes.

### 🔹 *8. Profit Margin % vs. Unit Price*

- **Goal:**  Examine the **relationship between unit price and profit margin (%)** across all orders to understand pricing efficiency and margin behavior.  

- **Chart Type:**  Scatter Plot

- **EDA Category:**  Bivariate Analysis

- **Structure:**

    - Scatter points plotted for each order  
    - Transparency (`alpha`) applied to highlight **data density**  
    - Axes represent **Unit Price ($)** and **Profit Margin (%)**  
    - Used to detect potential **correlations or margin inefficiencies** at different pricing levels  

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Profit%20Margin%20Vs%20Unit%20Price.png)

#### 🔍 **INSIGHTS:**  

- **Profit margins** cluster between **~18% and 60%**, showing **no strong correlation** with unit price, which ranges from near **0 to 6,500 (USD)**.
  
- Dense **horizontal bands** suggest stable margin tiers across a wide range of prices, indicating **consistent pricing strategies**.

- **Outliers below 18%**—present at both low and high price levels—may point to **cost inefficiencies or pricing anomalies** that warrant further analysis.  

### 🔹 *9. Unit Price Distribution per Product*

- **Goal:**  Compare **pricing variability** across different products to identify **price consistency** and potential **outliers**.

- **Chart Type:**  Boxplot

- **EDA Category:**  Bivariate Analysis

- **Structure:**  Boxplot showing **unit price distribution per product**, with **rotated x-axis labels** for readability and clear visualization of **price spread and outliers**.  

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Unit%20price%20distribution%20per%20product.png)

#### 🔍 **INSIGHTS:** 

- Products **20**, **27**, and **28** exhibit **high-end outliers** in unit price, surpassing their upper whiskers — suggesting **premium versions**, **bulk order deals**, or **special product variants** driving temporary price spikes.  

- Several products (e.g., **20**, **27**, **26**) show **low-end outliers near zero**, possibly representing **discounted promotions**, **trial SKUs**, or **clearance transactions** that distort average pricing.  

- The **interquartile ranges (IQRs)** across most products remain fairly consistent, indicating **stable pricing strategies** overall, though variance exists among a few mid-tier products (e.g., **13**, **18**, **25**).  

- To improve pricing precision, **exclude extreme outlier transactions** from margin and profitability analyses.  

- **Recommendation:** Investigate whether the identified anomalies stem from **intentional marketing tactics** (e.g., promotions) or **data irregularities**, and determine if such pricing behavior should be **standardized or discontinued** to maintain price stability.  

### 🔹 *10. Total Sales by State (Choropleth Map)*

- **Goal:**  Visualize the **geographic distribution of sales** to identify **high- and low-performing states** and uncover **regional sales gaps**.

- **Chart Type:**  US Choropleth Map

- **EDA Category:**  Univariate Geospatial

- **Structure:**  
    - States are **shaded by total sales** (in **millions USD**) using a **blue gradient**.  
    - A **legend on the right** indicates the **sales scale (M USD)**.  
    - **Hover tooltips** display exact sales values for each state.  
    - The **map is scoped to the USA** to provide clear regional context and comparison.

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Total%20Sales%20by%20State.png)

#### 🔍 **INSIGHTS:**  

- **California** dominates with **228M**, followed by **Illinois (111M)** and **Florida (90M)** — forming a **top-tier cluster (> 90M)**.
    
- **Mid-tier states** such as **Texas (84M)** and **New York (55M)** show consistent performance but lag the leaders by **40M–145M**.

- **Lower-tier states** — from **New Jersey (47M)** down to **Massachusetts (35M)** — indicate **uneven market penetration**.  

##### 🚀 **Actionable Takeaways:**  

- **Reinforce** growth in top-performing states through **tailored promotions and strategic partnerships**.  
- **Expand** market presence in **under-penetrated regions** via **localized campaigns** and **channel diversification** to close performance gaps.

### 🔹 *11. Top 10 States by Revenue and Order Count*

- **Goal:**  Identify the **highest revenue-generating states** and compare them with their **order volumes** to assess sales concentration and regional performance alignment.  

- **Chart Type:**  Two **horizontal bar charts**  

- **EDA Category:**  Multivariate  

- **Structure:**

    - **Chart 1:** Top 10 states by **total revenue** (in millions USD)  
    - **Chart 2:** Top 10 states by **number of orders**  
    - Bars sorted in descending order for easy comparison  
    - Consistent color palette and shared axis formatting for visual alignment  

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Top%2010%20states%20by%20Revenue%20and%20Order%20count.png)

#### 🔍 **INSIGHTS:** 

- **California (CA)** clearly leads with **$228.8M revenue** and **7,613 orders**, establishing it as the company’s **most dominant and high-volume market**.  

- **Illinois (IL)** and **Florida (FL)** follow strongly (**111M / 4,607 orders** and **90M / 3,836 orders**), showing **healthy sales momentum and balanced demand**.  

- **Mid-tier states** like **Texas (TX)**, **Indiana (IN)**, and **New York (NY)** maintain solid order volumes, though **minor revenue gaps** hint at differences in **average order value or product mix**.  

- **Lower-ranked states** — **New Jersey (NJ)**, **Connecticut (CT)**, **Michigan (MI)**, and **Massachusetts (MA)** — contribute modestly (**35M–47M**), presenting **potential growth opportunities through regional expansion and targeted marketing**.    

- **Overall Observation:**  
  Revenue and order rankings show **strong correlation**, implying that **sales volume drives revenue more than price differences**. However, slight gaps between order count and revenue for certain states suggest **variability in average transaction size** worth further exploration.

### 🔹 *12. Average Profit Margin by Channel*

- **Goal:**  Compare **average profit margins** across different **sales channels** to identify the **most and least profitable routes**.  

- **Chart Type:**  Bar Chart

- **EDA Category:**  Bivariate Analysis

- **Structure:**

    - Vertical bars sorted in **descending order by channel**  
    - Data labels display **average profit margin percentages**  
    - Color differentiation used for clear visual comparison between channels  

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Average%20profit%20margin%20by%20channel.png)

#### 🔍 **INSIGHTS:** 

- **Export** leads with an **average profit margin of 37.9%**, followed closely by **Distributor (37.6%)** and **Wholesale (37.1%)**.
  
- The **narrow margin spread (<0.2%)** highlights **strong and consistent profitability** across all sales channels.
  
- This **uniformity** suggests **effective cost control** and **robust pricing strategies** throughout the business.

- **Action:** Prioritize **volume growth in Export** while maintaining operational **efficiency in Distributor and Wholesale** channels to maximize overall profitability.  

### 🔹 *13. Top and Bottom 10 Customers by Revenue*

- **Goal:**  Identify the **highest- and lowest-revenue customers** to develop targeted engagement and retention strategies.  

- **Chart Type:** Side-by-side **horizontal bar charts**  

- **EDA Category:** Multivariate  

- **Structure:**  
    - **Left chart:** Top 10 customers by total revenue (in millions USD)  
    - **Right chart:** Bottom 10 customers by total revenue (in millions USD)  

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Top%20and%20Bottom%2010%20Customers%20by%20Revenue.png)

#### 🔍 **INSIGHTS:** 

- **Top Performers:** *Aibox Company* leads with **12.5M**, followed closely by *State Ltd* at **12.2M**. Even the 10th-ranked *Deseret Group* contributes **9.9M**, forming a tight **10–12M** top tier.
  
- **Bottom Performers:** *Johnson Ltd* tops the lower group with **5.1M**, dropping to *BB17 Company* at **4.1M** - about **half the revenue** of the leading customer.

- **Revenue Concentration:** The sharp decline from **~10M+ to 4–5M** underscores significant **dependence on top customers** for total sales.

- **Actionable Insight:**

  - Focus on **retention, loyalty, and upselling** for top-tier customers.  
  - Implement **targeted growth initiatives** to uplift the lower-revenue segment and reduce concentration risk.  

### 🔹 *14. Customer Segmentation: Revenue vs. Profit Margin*

- **Goal:**  Segment customers based on **total revenue** and **average profit margin**, while visually emphasizing **order volume**.

- **Chart Type:**  Bubble Chart (scatter plot with variable point sizes)

- **EDA Category:**  Multivariate

- **Structure:**  Scatter points sized by **number of orders**, plotted with:

    - **X-axis:** Total Revenue (in Million USD)  
    - **Y-axis:** Average Profit Margin (%)    

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Customer%20Segmentation.png)

#### 🔍 **INSIGHTS:** 

- **High-revenue customers** (>$10M) maintain steady profit margins between **36–40%**, showing that scale doesn’t compromise profitability.
  
- The **majority cluster** within the **$6–10M** revenue range, exhibiting stable margins (~34–40%) — reflecting consistent pricing and cost control.

- **Smaller customers** (<$6M) show the **widest margin variance** (~33–43%), likely due to fluctuating discounts or cost inefficiencies.

- **Bubble size** grows with revenue, but margins remain unaffected — indicating that **revenue**, not order volume, is the key performance driver.  

### 🔹 *15. Correlation Heatmap of Numeric Features*

- **Goal:**  Identify relationships among key numeric variables to uncover potential **multicollinearity** and understand interdependencies across performance metrics.  

- **Chart Type:**  Correlation Heatmap

- **EDA Category:**  Multivariate Analysis**

- **Structure:**

    - Annotated heatmap displaying **correlation coefficients** between selected numeric variables  
    - Color gradient to visualize strength and direction of correlations  
    - Helps detect redundant or highly correlated metrics for model refinement or KPI selection  

![](https://github.com/subrata-dey7/usa-regional-sales-analysis/blob/main/images/Correlation%20Matrix.png)

#### 🔍 **INSIGHTS:** 

- **Profit and revenue** exhibit a **strong positive correlation (0.87)** — higher sales directly drive higher profitability.
   
- **Unit price** emerges as a **key performance driver**, correlating **0.91 with revenue**, **0.79 with profit**, and **0.86 with total cost**, emphasizing how pricing impacts both income and expenses.

- **Total cost** maintains a **strong link to revenue (0.95)** but only a **moderate correlation with profit (0.67)**, suggesting that while higher sales increase spending, margins still fluctuate.

- **Quantity** shows **minimal correlation** with **unit price (~0.00)** and only **modest ties to revenue (0.34)** and **profit (0.30)**, indicating that **volume plays a secondary role** compared to pricing strategies.  

## 🔍 **Key Insights:** 

#### **1. 🌎 California Dominates Market Performance**

- California (CA) leads all states with $228.8M in total revenue and 7,613 orders, establishing itself as the strongest and most active region.

- Illinois (IL) and Florida (FL) follow with 111M and 90M, respectively, maintaining balanced sales-to-order ratios that indicate consistent demand and healthy market penetration.

#### **2. 💰 Stable Profit Margins Across Channels**

- All sales channels — Export (37.9%), Distributor (37.6%), and Wholesale (37.1%) — show minimal variation (<0.2%).

- This consistency highlights tight cost management and effective pricing discipline across routes.

#### **3. 📦 Revenue Driven by Pricing, Not Quantity**

- Strong correlations exist between revenue, profit, and unit price (r > 0.85), while order quantity shows only a weak influence (~0.3).

- This indicates that unit pricing, not volume, is the dominant profitability driver.

#### **4. 🧾 Product-Level Variability and Outliers**

- Products 8, 17, 20, 27, and 28 exhibit premium price spikes, likely due to bulk or special-edition orders.

- Low-end outliers near $0–$100 suggest promotional or test SKUs, which may distort margin analysis if not excluded.

#### **5. 🏢 Customer Revenue Concentration**

- Aibox Company (12.5M) and State Ltd (12.2M) top the customer list, forming a tight 9.9–12M high-revenue tier.

- The bottom segment (4–5M) highlights high dependency on key accounts, emphasizing the need for retention and upsell strategies.

#### **6. 🗺️ Geographic Sales Distribution**

- Sales heatmap reveals strong coastal and Midwest presence, while central states remain underpenetrated.

- This indicates growth potential through targeted regional campaigns and channel expansion.

#### **7. 📊 Profit Margin vs. Unit Price Patterns**

- Margins cluster between 18–60%, independent of price levels — showing a uniform pricing strategy.

- Outliers below 18% may reflect inefficient cost structures or pricing issues requiring review.

#### **8. 🔵 Customer Revenue–Margin Segmentation**

- Customers with >$10M revenue maintain stable margins (36–40%), proving scale efficiency.

- Smaller customers (<$6M) show wide margin variance (33–43%), indicating inconsistent pricing or higher cost volatility.

#### **9. 🧩 Product Performance Distribution**

- Top products contribute $27–32M each, forming the core revenue base.

- Bottom performers ( $15–18M ) signal opportunities for product optimization or portfolio rationalization.

#### **10. 📅 Seasonal Sales Trends**

- Excluding 2018, monthly sales steadily rise throughout the year, peaking in Q4 (Oct–Dec).

- Indicates strong year-end demand, valuable for inventory and marketing planning.

#### **🧠 Overall Observation**

- Revenue strongly aligns with sales volume, showing limited influence from pricing fluctuations.

- Top states and customers drive majority of earnings, emphasizing revenue concentration risks.

- Cost control and pricing discipline remain key strengths, while geographic and customer diversification offer clear paths for future growth.

## **💡 Recommendations**

- 1️⃣ **Expand high-performing regions** like California, Illinois, and Florida through targeted marketing and distribution support.

- 2️⃣ **Boost export sales** — the highest-margin channel — via international partnerships and trade promotions.

- 3️⃣ **Reassess low-revenue products** to optimize pricing, packaging, or discontinue underperforming SKUs.

- 4️⃣ **Strengthen top-customer retention** while launching growth programs for mid- and low-tier clients.

- 5️⃣ **Align inventory and campaigns** with clear seasonal demand peaks (May–June, Q4).

- 6️⃣ **Use data correlations** to refine pricing strategies and forecast revenue–profit trends more accurately.
