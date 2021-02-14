# Part 1: W3Schools SQL Lab

*Introductory level SQL*

\--

This challenge uses the [W3Schools SQL playground](http://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all). Please add solutions to this markdown file and submit.

1. Which customers are from the UK?

   ```sql
   SELECT * FROM Customers where Country='UK'
   ```

2. What is the name of the customer who has the most orders?

   ```sql
   SELECT Orders.OrderID, Customers.CustomerName, OrderDetails.Quantity
   FROM ((Orders
          INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID)
          INNER JOIN OderDetails ON Orders.OrderID=OrderDetails.OrderID)
   ORDER BY Quantity DESC;
   ```

   

3. Which supplier has the highest average product price?

   ```sql
   SELECT Suppliers.SupplierName, Products.Price
   FROM Suppliers
   INNER JOIN Products ON Suppliers.SupplierID=Products.SupplierID
   ORDER BY Price DESC;
   ```

4. How many different countries are all the customers from? (*Hint:* consider [DISTINCT](http://www.w3schools.com/sql/sql_distinct.asp).)

   ```sql
   SELECT DISTINCT Country FROM Customers;
   ```

   

5. What category appears in the most orders?

   ```sql
   SELECT Categories.CategoryName, OderDetails.Quantity
   FROM ((Products
         INNER JOIN Categories ON Products.CategoryID=Categories.CategoryID)
         INNN JOIN OrderDetails ON Products.ProductID= OrderDetails.ProductID)
   ORDER BY Quantity DESC;
   ```

   

6. What was the total cost for each order?

   ```sql
   SELECT OrderDetails.OrderDetailID,
   Products.Price * OrderDetails.Quantity AS TotalPrice
   FROM (OrderDetails
         INNER JOIN Products ON OrderDetails.ProductID=Products.ProductID);
   ```

   

7. Which employee made the most sales (by total price)?

   ```sql
   SELECT OrderDetails.OrderDetailID, Orders.EmployeeID,
   Products.Price * OrderDetails.Quantity AS TotalPrice
   FROM ((OrderDetails
         INNER JOIN Products ON OrderDetails.ProductID=Products.ProductID)
         INNER JOIN Orders ON OrderDetails.OrderID=Orders.OrderID)
   ORDER BY Price DESC, Quantity DESC;
   ```

   

8. Which employees have BS degrees? (*Hint:* look at the [LIKE](http://www.w3schools.com/sql/sql_like.asp) operator.)

   ```sql
   SELECT * FROM Employees
   WHERE Notes LIKE '%BS%';
   ```

   

9. Which supplier of three or more products has the highest average product price? (*Hint:* look at the [HAVING](http://www.w3schools.com/sql/sql_having.asp) operator.)

   ```sql
   SELECT Suppliers.SupplierName, COUNT(Products.CategoryID)
   FROM (Suppliers
        INNER JOIN Products ON Suppliers.SupplierID=Products.SupplierID)
   GROUP BY SupplierName
   HAVING COUNT(Products.CategoryID) > 3;
   ```

   