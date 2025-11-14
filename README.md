# Pizza_Sales_Analysis

## Table of content
- [Project_Overview](#project-overview)
- [Objectives](#objectives)
- 
### Project Overview
- Pizza ID: Unique identifier for each pizza sold, used to track individual items.
- Order ID: Unique identifier for each order, linking multiple pizzas to one transaction.
- Pizza Name ID: Identifier linking to the specific pizza name.
- Quantity: Number of pizzas ordered per line item, indicating order volume.
- Order Date: Full date of the order (e.g., 06/10/2025), for time-based analysis.
- Order Day: Day of the week (e.g., Tuesday), for daily trend analysis.
- Order Month: Month of the order (e.g., June), for seasonal patterns.
- Order Time: Time of the order (e.g., 01:48 PM), for hourly peak analysis.
- Unit Price: Price per pizza (e.g., $12.99), for pricing insights.
- Total Price: Total cost per item (Quantity × Unit Price)
- Pizza Size: Size of the pizza (Small, Medium, Large), for size preference.
- Pizza Category: Type of pizza (e.g., Classic, Veggie), for category trends.
- Pizza Name: Specific name of the pizza for product popularity.
- Pizza Ingredients: List of ingredients for recipe analysis.
- Pizza Type: Indicates whether a pizza is vegetarian or non-vegetarian.
- Order Patterns: Includes Single Pizza and Multiple Pizzas
### Objectives
The aim is to analyze pizza sales data to identify;
- Trends - Peak order times and days with the highest number of orders.
- Popular products - Size, category and most ordered pizza.
- Revenue drivers - Pizza that generates the highest revenue & compare revenue between pizza categories.
- Customer preferences - Vegetarian and Non-Vegetarian pizza.
- Order patterns - How often customers order more than one pizza at a time.
- Pricing variations - Price range of the pizzas sold.
- Time-based sales anomalies, enabling data-driven decisions to boost profitability and customer satisfaction.
### Tools Used
The analysis tool used to evaluate and analyze the dataset is **Excel**.
### Exploratory Data Analysis
1. Sales Trends
- Peak order times for pizzas?- Used Order Hour as rows in a Pivot Table, and counted unique Order IDs as values to determine the busiest hours.
- Days have the highest number of orders?- Set up a Pivot Table with Order Days as rows, and counted unique Order IDs as values to identify days with the most orders.
2. Popular Products:
- Which pizza is the most ordered?- Created a Pivot Table with Pizza Name as rows, Sum of Quantity as values, and sorted to highlight the top selling pizza.
- Most popular pizza size?- Built a Pivot Table with Pizza Size as rows and used Sum of Quantity as values to determine the preferred size.
- Most popular pizza category?- Used a Pivot Table with Pizza Category as rows and summed Quantity as values, to determine the dominant category
3. Revenue Analysis:
- Which pizza generates the highest revenue?- Constructed a Pivot Table with Pizza Name as rows, Sum of Total Price as values, and sorted to identify the highest revenue-generating pizza.
- Average order value?- In a Pivot Table, with Order ID in rows and Total Sales as values and summarize values by Average.
- How does the revenue compare between different pizza categories?- Created a Pivot Table with Pizza Category as rows and Sum of Total Price as values to compare category performance
4. Order Patterns
- How often do customers order more than one pizza at a time?- Used Power Query to add a conditional column: if Quantity = 1, "Single Pizza”; if Quantity ≥ 2, "Multiple Pizzas." Then, created a Pivot Table with this column as rows and counted the number of Order IDs to determine the frequency of each order type.
5. Customer Preferences:
- Is there a preference for vegetarian or non-vegetarian pizzas?- A new column was created to classify each pizza by analyzing the Pizza Ingredients field. This involved searching for specific keywords (e.g., "meat," "chicken," "pepperoni") to determine if a pizza contained non-vegetarian ingredients, labeling it as "Non-Vegetarian" if found, or "Vegetarian" if not. 
A Pivot Table was then used to group the data by this new category, summing the Quantity field to compare the total number of vegetarian versus non-vegetarian pizzas sold, providing insight into customer preferences.
6. Pricing Insights:
- What is the price range of the pizzas sold? - With Pizza Name in rows and Unit Price as values, summarized values as max and min to determine the price range of pizzas sold
- How does the unit price of pizzas vary across different sizes & categories? - Built a Pivot Table with Pizza Size as columns and Category as rows, calculated the average of Unit Price as values, to examine price differences.
7. Time-Based Insights:
- Are there any time periods with unusually high or low sales? - Created a Pivot Table with Order Month in rows and total price summed, providing a clear view of monthly sales performance. 
### Findings
- Sales Trends: Peak orders occur between 11:59 AM and 12:53 PM, exceeding 100 orders daily, with Fridays and Saturdays dominate weekly sales with 7,700 and 7,300 orders respectively.
- Popular Products: "Classic Deluxe Pizza" is the most ordered pizza leading with 2,453 orders. Large sizes are most popular and the Classic category leads in sales.
- Revenue Analysis: “Thai Chicken Pizza” generates the highest revenue and the Supreme category contributes significantly to total revenue.
- Customer Preferences:  Non-Vegetarian pizzas are preferred by 37,200 out of 48,600 customers.
- Order Patterns: Multi pizza orders are relatively low with only 900 orders out of 48,600
- Pricing Insights: Prices range from 10 to 83 Naira with variations across sizes and categories.
- Time Based Insights: January sees the highest revenue while December experiences a dip in sales

  ![Pizza Sales_Dashboard](https://github.com/user-attachments/assets/32073afc-bb2b-4211-b89d-67d1ee252c97)

### Recommendations
- Offer more non-vegetarian pizza options and promotions on Fridays and Saturdays to capitalize on peak demand. Consider rebranding or adjusting prices of underperforming pizzas to make them more competitive or appealing.
- Ensure efficient production processes for large-sized pizzas to meet high demand
- Analyze the factors contributing to the dip in sales in December and develop strategies to mitigate them such as introducing promotions, discounts or limited-time offers during these periods.
- Launch targeted marketing campaigns in January to sustain peak sales and revenue.
- Focus on improving customer satisfaction by ensuring timely delivery, high-quality products and excellent customer service.
### Conclusion
The pizza sales analysis offers valuable insights into customer preferences, sales trends and revenue patterns. By implementing targeted strategies to optimize menu and promotions and address seasonal fluctuations, the company can enhance customer satisfaction, drive revenue growth and ultimately achieve long term success.
