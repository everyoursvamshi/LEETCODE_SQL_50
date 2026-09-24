<h2><a href="https://leetcode.com/problems/recyclable-and-low-fat-products/description/?envType=study-plan-v2&envId=top-sql-50">
1757. Recyclable and Low Fat Products</a></h2>

Recyclable and Low Fat Products — LeetCode

📝 Problem

You are given a Products table containing information about products, including whether each product is low fat and recyclable.

Write a SQL query to find the product_id of products that are both low fat and recyclable.

The result can be returned in any order.

📊 Table: Products
Column Name	Type	Description
product_id	int	Primary key of the table
low_fats	enum	'Y' if the product is low fat, otherwise 'N'
recyclable	enum	'Y' if the product is recyclable, otherwise 'N'
ENUM Values

low_fats: 'Y', 'N'

recyclable: 'Y', 'N'

💡 Approach

We need products where both conditions are satisfied:

low_fats = 'Y'

recyclable = 'Y'

Use the WHERE clause with the AND operator to filter the required products.

💻 SQL Solution
SELECT product_id
FROM Products
WHERE low_fats = 'Y'
  AND recyclable = 'Y';

📥 Example Input
Products
product_id	low_fats	recyclable
0	Y	N
1	Y	Y
2	N	Y
3	Y	Y
4	N	N
📤 Example Output
product_id
1
3
🔍 Explanation

Products 1 and 3 have:

low_fats = 'Y'

recyclable = 'Y'

Therefore, the result contains product IDs 1 and 3.

🧠 SQL Concepts

SELECT

WHERE

AND

Filtering rows based on multiple conditions
