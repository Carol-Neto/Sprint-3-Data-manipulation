# Sprint 3 - Data Manipulation

# Introduction

Instacart is a grocery delivery platform where customers can place an order from a grocery store and then have their groceries delivered, similar to how Uber Eats and Deliveroo work. The dataset we provide has been modified from the original. We have reduced its size so that its calculations run faster, and we have included missing and duplicate values. We have also been careful to preserve the distributions of the original data when making the changes.

# What we will analyze in this project

Step 1: Reading the data file, I can already see that 'order_products.csv' contains a lot of rows of data. When a DataFrame has a lot of rows, info() does not print the counts of non-null values ​​by default. If you want to print them, include show_counts=True when you call info().

Step 2: I will preprocess the data as follows:

- I will check and correct the data types (e.g., make sure the ID columns are integers)
- I will check and fill in missing values
- I will check and remove duplicate values

Step 3: After preprocessing the data, I will perform the following analyses:

- I will check that the values ​​in the 'order_hour_of_day' and 'order_dow' columns in the orders table make sense (i.e., the values ​​in the 'order_hour_of_day' column range from 0 to 23 and the values ​​in the 'order_dow' column range from 0 to 6).
- I will create a graph that shows how many people place orders at each hour of the day.
- I will create a graph that shows what day of the week people shop.
- I will create a graph that shows how long people wait to place their next order.

- Are there differences between the distributions of 'order_hour_of_day' on Wednesday and Saturday? With a histogram for both days on the same graph we can see the differences.
- A distribution chart for the number of orders that customers make
- What are the top 20 most frequently purchased products?

- How many items do people typically purchase in an order? What would the distribution look like?
- What are the top 20 items most frequently included in repeat orders?
- For each product, what proportion of the orders in which it appears are repeat orders? I will create a table with columns for product ID, product name and the proportion of repeat orders.
- For each customer, what proportion of the products purchased are repeat orders?
- What are the top 20 items that people put in their carts before everyone else? I will show the product ID, name and the number of times it was the first item added to a cart.

----

# Data Dictionary

There are five tables in the dataset. Below is a dictionary that lists the columns in each table and describes the data contained in them.

'**instacart_orders.csv**': Each row corresponds to an order in the Instacart app
- 'order_id': This is the unique ID number for each order
- 'user_id': This is the unique ID number for each customer's account
- 'order_number': This is the number of times the customer has placed an order
- 'order_dow': This is the day of the week the order was placed (0 is Sunday)
- 'order_hour_of_day': This is the time of day the order was placed
- 'days_since_prior_order': This is the number of days since the customer placed their previous order

'**products.csv**': Each row corresponds to a unique product that customers can purchase
- 'product_id': This is the unique ID number for each product
- 'product_name': This is the name of the product
- 'aisle_id': This is the unique ID number for each aisle category in the grocery store
- 'department_id': This is the unique ID number for each department category in the grocery store supermarket

'**order_products.csv**': each row corresponds to an item included in an order
- 'order_id': is the unique identification number of each order
- 'product_id': is the unique identification number of each product
- 'add_to_cart_order': is the sequential order in which each item was placed in the cart
- 'reordered': 0 if the customer has never purchased the product before, 1 if they have already purchased it

'**aisles.csv**'
- 'aisle_id': is the unique identification number of each aisle category in the supermarket
- 'aisle': is the name of the aisle

'**departments.csv**'
- 'department_id': is the unique identification number of each department category in the supermarket
- 'department': is the name of the department
