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



###  
