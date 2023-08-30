# Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/8e9029b2-88ff-4ebd-b310-cdfcc00dba90)

Since SQL Injection is in the category of products, we catch a burp suite request in the "Gifts" category based on the clues given to us.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/953006f3-e012-4f55-9aea-d6d6d4930c85)

Then we right click on this request and select "Send to Repeater".

Our goal at this stage is to reveal unreleased products on the application by making an appropriate SQL query.

For this, we add the query " '+or+1=1-- " to the url.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/f2eab973-ad7e-41dd-a2f0-17096d034e2d)

This query will reveal all tables in the "category" as it will definitely be provided.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/174b269f-b822-4e53-9833-899f02305e05)

There were a total of 12 products in the app. 
But after our SQL Injection application, we uncovered 8 unpublished products.



