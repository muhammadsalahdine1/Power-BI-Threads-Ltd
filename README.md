# Power-BI-Threads-Ltd

### Dataset: Orders - Products - Retailers - Returns
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/1.PNG" width="1000">

### Add a table and slicers
- we will add a table with some basic information about orders that Threads Ltd has received: the order ID, the product stock-keeping unit (SKU), the quantity of items the order is for, and the sales amount received by the company for the order.
- We will also add a pair of filters for year and product name, allowing for more granular analysis for the Head of Sales of the company.
- What is the "Order ID" with the highest sales amount for the product "Aero Daily Fitness Tee"?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/2.PNG" width="1000">


### Create a scatter plot
- Cost of goods sold, or COGS, is the cost of goods or products that are either manufactured or purchased by a company and then sold.
- They are a business expense, and the lower the COGS amount, the better it is for a company like Threads Ltd.
- To determine a company's gross profit, the cost of goods sold can be subtracted from the sales revenue.
- This is why the Head of Sales is interested in seeing what type of relationship there might be between the sales amount and the cost of goods sold over time.
-  We will use a scatter plot (or scatter chart) to figure this out. 
- Add the sales amount (Orders[Sales_Amount]) to the X Axis and the cost of goods sold (Orders[Cost_of_Goods_Sold]) to the Y Axis.
- Add Orders[Order_Date] to the Values field. We want to see all dates in the visual, so make sure to display a standard date value and not the date hierarchy.
- Narrow down the year range from 2020-2021.
- What is the greatest sales amount within the date period?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/3.PNG" width="1000">


 ### Create a bubble chart
- A bubble chart is a scatter chart where the size of the bubble represents a measure.
- This allows us to track three separate measures on a single visual.
- In this case, we will track the relationship between the total sales amount (Sales_Amount) and the average product price (Product_Price), using the total order quantity (Order_Quantity) as the size of the chart.
- The Head of Sales is looking at adding further "Tank Tops" products to the catalog of items sold by Threads Ltd. Therefore, we will visualize some key measures related to recent performance that can help with the decision-making process.
- Add a third slicer to the page with Product[Product_Category] as the Field.
- Add a scatter plot to the page, taking up the remaining canvas.
- To make this a bubble chart, you will use three measures.
- X Axis will contain the total sales amount (sum of Sales_Amount)
- Y Axis will contain the average price of each product (average of Product_Price)
- Size will contain the total order quantity (sum of Order_Quantity)
- Finally, add Product_Name to the Values field of your new bubble chart.
- Use the slicers to filter down to 2021 and the product category "Tank Tops".
- Add a filter on the bubble chart to include only total sales amounts of at least £5,000.00 or more.
- What is the total order quantity of the product with the highest average product price?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/4.PNG" width="1000">


### Create a bar chart
- The product manager of Thread Ltd needs to know how the different products within our product catalog have been performing.
- This will help determine upcoming marketing strategies, investment in new products, as well as communications with customers.
- Our first task is to review the "Women" products sold by Threads Ltd to supermarket retailers in the most recent year of data (2021).
- The product manager wishes to understand which products sold well and which didn't.
- To do this, we will start with a simple comparison of products by sales amount. 
- Add a new Clustered bar chart visual.
- Create your chart with the total sales amount (Orders[Sales_Amount]) by product name (Products[Product_Name]).
- Add a slicer, and then filter by gender (Products[Product_Gender]). Narrow the list down to products for women only.
- Add a page-level filter where the year is 2021. Use the year part of the date hierarchy from the Order_Date column.
- Add a slicer and filter by retailer channel (Retailers[Retailer_Channel]). Only show products that have been ordered by supermarkets.
- What product has the highest total sales amount from all "Women" only products sold in 2021 to Supermarket retailers?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/5.PNG" width="1000">


### Format a visual
- In order to make some insights from our bar chart stand out more so that we can evoke an emotional response from our audience,
- we will add some lines to our visual using Power BI's Analytics pane.
- In discussion with the product manager, we have obtained more details about what he expects to see from the sales amount information in 2021.
- This can help us format our visuals accordingly.
- In addition, the product manager will want to see and share our work with his team, so we want to make sure the page looks nice for him.
- Change the title on the bar chart visual from "SalesAmount by ProductName" to "Total Sales Amount by Product for Women".
- Change the display of total sales amount axis on the bar chart to display the full amount with zero decimal places.
- Add a constant line at £5,000. To see this line better, make sure that the color is "Black, 0% darker" and transparency is 50%. Name the constant line "Ideal Sales Amount".
- In addition to the ideal sales amount line, it would be nice to add a line representing the average total sales amount for products set within the visual.
- Which product has total sales amount just below the ideal sales amount constant line?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/6.PNG" width="1000">


### Stacking variables
- The product manager likes our analysis so far and now wants to understand how products are performing across different retailer channels.
- He wants to know how to apply the upcoming company strategies to specific channels.
- Therefore, we will focus on the total order quantities processed for each channel.
- Here, we can use a stacked bar chart to get an impression of how many items each channel ordered in total and break it down by the product categories for further analysis.
- Add a page-level filter where the year is 2021.
- Add a Stacked bar chart visual.
- Chart the total order quantity (Orders[Order_Quantity]) by retailer channel (Retailers[Retailer_Channel]), broken out by the product category (Products[Category]).
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/7.PNG" width="1000">


### Using small multiples
- Small multiples are a way of showing comparison information across two categorical dimensions,
- saving a bit of space and a lot of time over making individual charts for each combination of factors.
- Here, we will look at the total order quantities of Hoodies & Sweatshirts by Franchise outlets and compare product colors for each clothing gender type for our product manager.
- Add page-level filters where the year (Orders[Order_Date].[Year]) is 2021, the retailer channel (Retailers[Retailer_Channel]) is "Franchise", and the product category (Products[Product_Category]) is "Hoodies & Sweaters".
- Add a new clustered column chart visual, mapping total order quantity (Orders[Order_Quantity]) by product gender (in the Products table).
- Add the color of the product to the Small multiples field. Then, format the visual and ensure that the grid layout is four rows by three columns.
- Which gender and product color combination had the highest total orders from "Franchise" channels in 2021?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/8.PNG" width="1000">



###  Line and area charts
- Here, we will use a line chart to track three important financial indicators for Threads Ltd: total sales amount (or revenue), total COGS, and gross profit.
- Then we will see how these measures move over time using area charts.
- Add a slicer for product category.
- Add a new line chart and track total sales amount, total cost of good sold (COGS), and total profit by month and year.
- Change the line chart to be an area chart.
- Change the chart back to a line chart.
- Which month-year had the highest total profit over the four year period?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/9.PNG" width="1000">


 
### Combo charts
- Profit margin is a measure of a business's profitability.
- It represents the percentage of revenue that a company gets to keep as profit.
- Threads Ltd has provided us with information related to gross profit and gross profit margin.
- Although gross profit is required to calculate gross profit margin, an increase in revenue or profit doesn't necessarily mean an increase in the profit margin. This is an important question that the CCO has been asking in recent meetings.
- we will start providing the CCO with some answers. Combination charts are best used in situations such as where you wish to compare a rate variable and a counting variable over time.
- Add a new line and clustered column chart visual.
- Using the Orders table, visualize total gross profit and the average profit margin over time.
- Use Profit as the bars and the Profit_Margin as the line.
- For the time on the x-axis, use the year and month of Order\_Date.
- Aggregate Profit_Margin as the average profit margin.
- Format the Profit_Margin column in the Orders table so that it appears as a percentage.
- This can be done using the Column tools menu tab after double-clicking Profit_Margin in the Data pane.
- Format the chart so that the "Title text" reads "Gross Profit and Average Profit Margin over Time".
- Change the X axis "Axis title" to read "Month and Year".
- Apply the correct filter to the page in order to see the financial information for products within the "Tank Tops" category.
- In March 2019, the average profit margin for Tank Tops reached its high point. What was the percentage of the average profit margin?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/10.PNG" width="1000">



### Tornado charts
- Now focus on a particular year in time, as well as making it as clear as possible what the profit and profit margin have shown so far - that total sales amount is never lower than sales costs across all products. Here, we will use a custom tornado chart visual to see whether the conjecture above holds.
- Replace the current "Category" slicer so that it allows you to filter by year, and show information only for 2021. 
- Add a new custom Tornado chart.
- Set the tornado chart to track the total sales amount and total cost of goods sold by category.
- Then, sort the tornado chart by category (either ascending or descending).
- Change the "Title text" for the visual to "Revenue versus Cost".
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/11.PNG" width="1000">



### Shares of the whole
- Two common ways of demonstrating shares of a whole in Power BI are pie charts and treemaps.
- Pie charts are best for showing simple shares of a static total. Treemaps, meanwhile, are best for showing hierarchical, categorical data.
- Add two page-level filters, one where the year is 2021 and the other where the category is "Tees".
- Add a new pie chart to the canvas.
- Display the total order quantity of items, with the product size as the legend.
- Add a filter to the visual where channel is "Local store".
- Add a new treemap to the canvas.
- This visualization should contain the total order quantity, channel, and product size. Ideally, we will want to use the treemap hierarchy features, so make sure to take that into consideration when adding the columns to the visual.
- Enable Drill Mode on the treemap.
- Select a channel like "Supermarket" to review the sizes sold by this channel and see how this affects the pie chart: the pie disappears!
- Remove the visual-level filter on the pie chart and notice how different your experience is with the treemap versus pie chart at each level of drill-down.
- What was the total order quantity for "M" sized products from Small chain stores?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/12.PNG" width="1000">



### Gauges and cards
- Gauges can provide us useful information if we know the current value, target value, and maximum value of a measure.
- In this case, we will look at gross profit margin (Profit_Margin) using a target value of 70%, which has been set by the executive team at Threads Ltd, and is something the CCO is very interested in.
- Cards can show us one important piece of information, making the card a clean visual when looking at one or a few very important metrics.
- In this case, we will use cards to determine how many individual orders had a profit margin greater than the company target profit margin.
- Create two new DAX measures on the Orders table:
- Target Profit Margin which should be equal to the fixed value 0.70
- Maximum Profit Margin that must be equal to the fixed value 1.00.
- For each of these new measures, set the format to percentage and to show two decimal places.
- Add a new gauge visualization.
- Use this gauge to measure the average profit margin versus the target and maximum measures you created.
- Add a new DAX measures to the Orders table:
- The measure, "Orders Above Target Profit Margin", should contain SUMX(Orders, IF(Orders[Profit_Margin] > Orders[Target Profit Margin], 1, 0))
- this will count the number of orders that achieved a profit margin above the target profit margin.
- Add a second new DAX measure to the Orders table:
- The new measure, "Orders Below Target Profit Margin", should contain SUMX(Orders, IF(Orders[Profit_Margin] < Orders[Target Profit Margin], 1, 0))
- add two new cards to display Orders Above Target Profit Margin and Orders Below Target Profit Margin.
- Comparing orders with products in the "Tees" category for 2021 and 2020, which year had more orders above the target profit margin?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/13.PNG" width="1000">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/14.PNG" width="1000">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/15.PNG" width="1000">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/16.PNG" width="1000">
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/17.PNG" width="1000">



### Key performance indicators
- Key Performance Indicators (KPIs) help businesses track how they are doing versus relevant metrics.
- In this case, our CCO wants to see how the company is faring compared to two important measures, one for total orders and one for total returns. Returns are not good for the company, as it means an order that was processed for a retailer was sent back due to errors or faulty goods. This costs Threads Ltd money, so the fewer returns made the better.
- Add one page-level filter where the year is 2021.
- Create two new DAX measures in the Orders table:
- Total Orders which should should contain COUNT(Orders[Order_ID]).
- This will count the total number of orders that have been processed by the company.
- Add a KPI visualization.
- This KPI should follow Total Orders by Order_Date.Month against the Target Orders.
- Create two new DAX measures in the Returns table:
- Total Returns which should should contain COUNT(Returns[Order_ID]).
- This will count the total number of orders that have been returned by retailers after the order was carried out by the company.
- Target Returns that must be equal to the fixed value 10.
- Target Orders that must be equal to the fixed value 180.
- KPI which follows the Total Returns by Order_Date.Month against the Target Number of Returns.
- How much worse did the company do with respect to total orders versus the target?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/18.PNG" width="1000">




### Conditional formatting
- Conditional formatting is a great tool for displaying color when certain conditions are met.
- These can be cases when the situation is particularly good or particularly bad, but in either event, the change in color will draw the eye.
- Here, we will go back to a visual created in a previous exercise and edit it so that a neutral color is used for certain products over a total sales amount threshold but show a different color for products that do not reach the £5,000 total sales amount threshold.
- On the Product Comparison page, select bar chart and enter the conditional formatting menu to change the colors of the bars.
- Format by Rules, with the first rule using some dark red color, such as "Theme color 8, 25% darker", or #a1343c. This color should display when Sales_Amount >= 0 and Sales_Amounth < 5000.
- In the same window, add a second rule where Sales_Amount >= 5000 and Sales_Amounth < Max. The rule should use some grey color, such as "White 30% darker". Save the changes made.
- What is the third product that fits the dark red conditional formatting rule?
<img src="https://github.com/muhammadsalahdine1/Power-BI-Threads-Ltd/blob/main/19.PNG" width="1000">
 
