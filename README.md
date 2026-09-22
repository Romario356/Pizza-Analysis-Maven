# 🍕 Operations, Sales & Menu Performance Analysis — Plato's Pizza
**Tool Used:** Microsoft Excel & Google Sheets (Advanced Formulas, Data Blending, Pivot Tables & Analytics)

---

## 🎯 1. Project Context & Business Problem
**Plato's Pizza** (New Jersey) collects a full year of transactional data, capturing 49,574 rows of order details across 21,350 unique orders. Despite possessing this valuable data asset, management currently operates the business blindly without data-driven insights.

As a Data Analyst, my goal is to design a comprehensive analytical report to **maximize revenue** and **optimize operational efficiency** by addressing 4 strategic pillars:
1. **Traffic Analysis:** Identify peak days and hours to streamline staff scheduling.
2. **Kitchen Capacity:** Measure the actual volume of pizza production during high-stress periods.
3. **Menu Optimization:** Pinpoint "star" products and eliminate "underperforming" items from the menu.
4. **Financial Performance:** Determine the Average Order Value (AOV).

---

## 🛠️ 2. Data Cleaning & Preparation
Before launching the analysis, a rigorous data preparation phase was conducted to guarantee the integrity of all key metrics:
* **Data Auditing:** Used the `COUNTBLANK` function to confirm zero missing values across critical variables (`order_id`, `date`, `time`).
* **Formatting:** Converted time and numeric formats. Removed blank artifact rows at the bottom of the worksheet to stabilize the dataset.
* **Time Engineering:** Applied the `=TEXT(Date, "dddd")` function to dynamically extract the days of the week from raw dates.
* **Data Blending (Table Joining):** Implemented the `VLOOKUP` function to map and import unit prices from the pizza reference table into the active order details table.

---

## 📊 3. Pivot Table Analysis & Business Insights

### Step A: Order Traffic & Kitchen Production Volumes
Cross-referencing hours and days revealed critical operational trends for kitchen management:
* **The Weekly Rush:** **Friday** emerges as the highest traffic day of the week with **3,538 unique orders**, followed closely by Thursday (3,239) and Saturday (3,158).
* **Bimodal Production Peaks:** Hourly analysis highlights two distinct daily peaks. The lunchtime rush (**12:00 PM**) represents the ultimate operational bottleneck, requiring the kitchen to output **6,776 pizzas** annually, compared to the dinner peak at 6:00 PM (**5,417 pizzas**).
* **Key Insight:** Although overall transaction volume remains high in the evening, lunchtime customers order a significantly higher volume of pizzas per ticket.

### Step B: Financial Performance & Average Order Value (AOV)
Exploiting revenue data allowed us to establish the financial baseline of the restaurant:
* **Global Revenue:** Total annual gross sales reached precisely **\$817,860.05**, with Friday driving a record **\$136,073.90**.
* **Average Order Value (AOV):** By dividing total revenue by the 21,350 unique transactions, the average basket size settles at **\$38.31** per order. This metric will serve as a baseline to measure the impact of future up-selling and cross-selling campaigns.

### Step C: Menu Performance (Tops & Flops)
Sorting sales volumes by recipe and size isolated the commercial extremes of the menu card:
* **Top 3 Best Sellers:** In terms of quantity, the `big_meat_s` (Small size) is the absolute best seller (**1,914 units**). In terms of financial impact, chicken recipes dominate the leaderboard, led by `The Thai Chicken Pizza` generating **\$43,434.25**.
* **Flop 3 Underperformers:** `the_greek_xxl` is a total commercial failure, selling only **28 units** over the entire year, followed by `green_garden_l` (95 units) and `ckn_alfredo_s` (96 units).

---

## ⚠️ 4. Data Limitations & Capacity Analysis
Evaluating the dining room capacity (15 tables, 60 seats) exposed a major structural blind spot in the dataset: the absence of an order type variable (`Dine-in` vs. `Takeout/Delivery`).

**Logical Demonstration:** With an average of **2.3 pizzas per order**, an average Friday lunchtime rush (68 orders/hour) would physically oversaturate the dining Room by 450%. This mathematically proves that *Plato's Pizza relies heavily on takeout and Delivery channels** to absorb its peak production volumes.
###  5.Strategic Recommendations
1. **Human Resources:** Reinforce the preparation team during the morning shift (10:00 AM - 12:00 PM) to fully prepare ingredients aheadof the massive 12:00 PM lunch production rush.
2.  **Menu Rationalization** Immediately remove the XXL size of the *The Greek* pizza to eliminate the waste of specific ingredients and simplify inventory management.
3.  **Data Governance**: ** Upgrade the point of sales (POS) system immediately to log the order channel ('Dine-in','Takeout','Delivery'). This data is mandatory before making any capital decisions regarding dining room expansions.<img width="1040" height="780" alt="WhatsApp Image 2026-09-22 at 22 02 33" src="https://github.com/user-attachments/assets/4cf6d684-3c30-43e6-ba97-7ea2013b6940" />
[PIZZA CLEAN DATA.xlsx](https://github.com/user-attachments/files/32530290/PIZZA.CLEAN.DATA.xlsx)
[MAVEN PIZZA CLEAN.xlsx](https://github.com/user-attachments/files/32530198/MAVEN.PIZZA.CLEAN.xlsx)
