# Laboratuvar: WHERE yan tümcesinde gizli verilerin alınmasına izin veren SQL enjeksiyon güvenlik açığı

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/56ca3e80-6988-4173-bde7-19b0b9a04124)

After accessing the app, we are greeted by a product sales screen.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/a922bbf5-24d5-4eff-9ae3-7137248997b7)

From the clues we know that the SQL injection is located in the "category" section.

So we click on any of the categories and capture this request with BurpSuite.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/0d29cd61-985a-4973-a28a-5acdb07a35e0)

To more easily examine the responses of our application, we right click on the captured request and select the "Send to Repeater" option

Our goal at this point is to place the appropriate query on the url and reveal all the products in the application.

Therefore we add the query " '+or+1=1-- " to the url.
This query will return all the tables in the categories and reveal the hidden products.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/e7cbd833-b6cb-49ef-b819-19ed473b021b)

While there are 12 products published in the application, after this query, 8 more unpublished products are revealed.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/4290baab-4d01-4712-b931-f621ecb1f1c2)

As it turns out, our lab is solved
