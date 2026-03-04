🎵 Apple iTunes Music Store Analysis
📋 Project Overview
A comprehensive SQL analysis of Apple iTunes Music Store data to derive actionable business insights on customer behavior, sales performance, and product popularity.

🗄️ Database Schema

Tables: employee, customer, invoice, invoice_line, track, album, artist, genre, media_type, playlist, playlist_track

🔍 Key Analysis Areas
• Customer Analytics: Top spenders, lifetime value, repeat purchases

• Sales Analysis: Revenue trends, seasonal patterns, rep performance

• Product Analysis: Popular tracks, unsold inventory, genre performance

• Geographic Trends: Regional revenue, market opportunities

• Operational Efficiency: Employee performance, inventory optimization

📊 Key Insights
Metric	                  Value
Total Revenue	            $11,800
Active Customers	        45
Avg Customer Value        $115
Catalog Utilization       64%
Top Genre               	Rock(35%)
Top Artist	              Queen

💻 Sample Query
sql
-- Top 10 customers by spending
SELECT c.first_name, c.last_name, c.country, 
       ROUND(SUM(i.total),2) AS total_spent
FROM customer c
JOIN invoice i ON c.customer_id = i.customer_id
GROUP BY c.customer_id
ORDER BY total_spent DESC
LIMIT 10;

📁 Repository Structure
text
├── README.md
├── schema.sql
├── queries/
│   ├── customer_analytics.sql
│   ├── sales_analytics.sql
│   └── product_analytics.sql
├── data/ (CSV files)
└── insights/
    ├── summary.md
    └── recommendations.md
    
🛠️ Technologies
• SQL (MySQL/PostgreSQL)

• CSV datasets

• Power BI / Tableau (optional)

🚀 Quick Start
• Run schema.sql to create tables

• Import CSV files

• Execute queries in /queries folder

• Explore insights in /insights

📈 Business Recommendations
• Marketing: Target inactive customers, expand in high-potential markets

• Product: Bundle unsold tracks, create artist collections

• Operations: Balance rep workloads, optimize inventory

