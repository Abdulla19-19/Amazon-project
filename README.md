# Amazon-project

## Executive Summary
This report provides a comprehensive analysis of the e-commerce database, focusing on
key business metrics such as top-selling products, revenue by category, customer behavior,
and operational performance. The analysis leverages SQL queries to extract insights
from tables including products, orders, order_items, customers, payments, shipping,
inventory, sellers, and category. The findings aim to support data-driven decisionmaking for optimizing sales, inventory, and customer engagement strategies.

**1 Database Schema Modifications**

To ensure data integrity, foreign key constraints were added to the database schema,
linking related tables. Additionally, a total_sale column was added to the order_items
table to store the calculated sales value (quantity * price_per_unit). These changes
enable accurate and efficient querying for business insights.

**2 Key Business Insights**

***2.1 Top 10 Selling Products***

The top 10 products by total sales value provide insights into high-performing products.
The query joins orders, order_items, and products to calculate total quantity sold and
sales value.
• Key Metrics: Product ID, product name, total quantity sold, total sales value.
• Result: The top 10 products are ranked by total sales value, helping identify
bestsellers for inventory and marketing focus.

***2.2 Revenue by Category***

Revenue distribution across product categories highlights the most profitable segments.
• Key Metrics: Category ID, category name, total revenue, percentage contribution
to total revenue.
• Result: Categories are ranked by revenue, with their percentage contribution to
total sales, aiding strategic category prioritization.

***2.3 Average Order Value (AOV)***

The average order value for customers with more than 5 orders reveals high-value customer segments.
• Key Metrics: Customer ID, full name, AOV, total orders.
• Result: Customers with frequent orders and high AOV are identified, supporting
targeted retention strategies.

***2.4 Monthly Sales Trend***

Monthly sales trends over the past year highlight seasonality and growth patterns.
• Key Metrics: Year, month, current month sales, previous month sales.
• Result: Sales trends show month-over-month changes, useful for forecasting and
planning promotions.

***2.5 Non-Purchasing Customers***

Customers who registered but never placed an order are identified for re-engagement
campaigns.
• Key Metrics: Customer ID, first name, last name.
• Result: A list of inactive customers to target with marketing initiatives.

***2.6 Least-Selling Categories by State***

Identifying the least-selling product categories per state helps optimize regional inventory.
• Key Metrics: State, category name, total sales.
• Result: Categories with the lowest sales in each state are highlighted for potential
phase-out or promotion.

***2.7 Customer Lifetime Value (CLTV)***

CLTV ranks customers by their total spending, identifying high-value customers.
• Key Metrics: Customer ID, full name, CLTV, customer ranking.
• Result: Top-spending customers are ranked, guiding loyalty program development.

***2.8 Inventory Stock Alerts***

Products with stock levels below 10 units are flagged for restocking.
• Key Metrics: Inventory ID, product name, current stock, last restock date, warehouse ID.
• Result: Low-stock products are identified, ensuring timely restocking to avoid sales
disruptions.

***2.9 Shipping Delays***

Orders with shipping delays exceeding 3 days are analyzed to improve logistics.
• Key Metrics: Customer ID, full name, order ID, order date, shipping date, shipping
System: provider, days to ship.
• Result: Orders with significant delays are listed, highlighting areas for logistics
optimization.

***2.10 Payment Success Rate***

The percentage of successful payments provides insights into payment processing efficiency.
• Key Metrics: Payment status, total count, percentage of total payments.
• Result: Breakdown by payment status (e.g., successful, failed, pending) helps
identify payment issues.

***2.11 Top Performing Sellers***

The top 5 sellers by total sales value are evaluated, including their order success rate.
• Key Metrics: Seller ID, seller name, completed orders, cancelled orders, total
orders, successful order percentage.
• Result: High-performing sellers are identified, with success rates guiding seller
partnerships.

***2.12 Product Profit Margin***

Profit margins for each product highlight profitability.
• Key Metrics: Product ID, product name, profit margin, product ranking.
• Result: Products are ranked by profit margin, informing pricing and sourcing
strategies.

***2.13 Most Returned Products***

Products with high return rates are identified to address quality or customer satisfaction
issues.
• Key Metrics: Product ID, product name, total units sold, total returned, return
percentage.
• Result: The top 10 products by return rate are listed, guiding quality control
efforts.

***2.14 Inactive Sellers***

Sellers with no sales in the last 6 months are flagged for review.
• Key Metrics: Seller ID, last sale date, total sales.
• Result: Inactive sellers are identified, with details on their last activity for reengagement or removal.

***2.15 Customer Categorization***

Customers are categorized as "Returning" or "New" based on return count.
• Key Metrics: Customer ID, customer name, total orders, total returns, customer
category.
• Result: Customers with more than 5 returns are classified as "Returning," aiding
personalized marketing.

***2.16 Top 5 Customers by Orders in Each State***

The top 5 customers per state by order count are identified for regional targeting.
• Key Metrics: State, customer ID, customer name, total orders, total sales, rank.
• Result: High-order customers per state are ranked, supporting localized marketing
strategies.

***2.17 Revenue by Shipping Provider***

Revenue and delivery performance by shipping provider highlight logistics efficiency.
• Key Metrics: Shipping provider, total orders, total revenue, average delivery days.
• Result: Providers are ranked by revenue and delivery time, informing logistics
partnerships.

***2.18 Top 10 Products with Decreasing Revenue***

Products with the highest revenue decline are identified for strategic review.
• Key Metrics: Product ID, product name, category name, 2022 revenue, 2023
revenue, revenue decrease ratio.
• Result: The top 10 products with declining revenue are listed, guiding product
strategy adjustments.

***2.19 Monthly Repeat Purchase Rate***

The percentage of customers making multiple purchases in a month indicates loyalty.
• Key Metrics: Year, month, total customers, repeat customers, repeat rate.
• Result: Monthly repeat purchase rates are calculated, supporting retention strategies.

***2.20 Longest Shipping Delays per Customer***

Orders with the longest shipping times per customer highlight logistics bottlenecks.
• Key Metrics: Customer ID, order ID, shipping provider, days to ship.
• Result: The longest shipping delays per customer are identified, aiding logistics
improvements.

## Recommendations
***1. Inventory Management:*** 

Prioritize restocking products with stock below 10 units
to prevent sales losses.

***2. Product Strategy:***

Focus on high-margin and top-selling products while investigating high-return products for quality issues.

***3. Customer Engagement:***

Target non-purchasing and returning customers with
tailored campaigns to boost engagement.

***4. Seller Management:***

Support top-performing sellers and re-engage or phase out
inactive sellers.

***5. Logistics Optimization:***

Address shipping delays by reviewing providers with
high average delivery times.

***6. Regional Strategy:***

Adjust inventory and marketing based on least-selling categories by state and top customers per state.

## Conclusion

This analysis provides actionable insights into product performance, customer behavior,
and operational efficiency. By leveraging these findings, the e-commerce platform can
optimize inventory, enhance customer retention, improve logistics, and drive revenue
growth.
