# BONK Transactions Analysis Workflow

This repository contains a KNIME workflow designed to analyze BONK cryptocurrency transactions. The workflow aggregates and visualizes transaction data to identify peak trading hours and high-value trades for a specific date, November 28.

## Workflow Overview
The KNIME workflow connects to multiple MongoDB clusters, extracts transaction data, and performs the following operations:

## Data Extraction:

- Connects to MongoDB clusters using the MongoDB Connector node.
- Reads transaction data using the MongoDB Reader node.
- Converts JSON data to table format using the JSON to Table node.
  
Data Preparation:

Merges datasets from multiple clusters using Joiner and Column Filter nodes.
Filters relevant columns such as transaction ID, block month, block time, and transaction amount in USD.
Data Aggregation:

Groups transactions by hour (from block_time) and sums the amount_usd for each hour.
Extracts high-value transactions where amount_usd > 50.
Data Visualization:

Line Plot: Displays trading volumes by hour on November 28.
Bar Chart: Highlights the top 5 largest transactions on November 28.
Pie Chart: Shows the contribution of each high-value trade among overall trades on November 28.
Key Insights
Peak Trading Hours: Determine the hours with the highest transaction volumes.
High-Value Trades: Analyze and rank the top transactions by USD value.
Prerequisites
To use this workflow, ensure you have the following:

KNIME Analytics Platform installed.
Access to MongoDB clusters containing BONK transaction data.
Required dependencies for MongoDB integration in KNIME.
How to Use
Clone this repository:
bash
Copy code
git clone https://github.com/your-username/bonk-transactions-analysis.git
Open the workflow file (Bonk_Project3_Team9.knwf) in KNIME Analytics Platform.
Configure the MongoDB Connector nodes with your MongoDB credentials.
Execute the workflow to generate insights and visualizations.
Results
The output visualizations provide actionable insights into BONK trading patterns, including:

Trading activity trends throughout the day.
The largest trades in terms of value.
Proportional contributions of high-value trades.
