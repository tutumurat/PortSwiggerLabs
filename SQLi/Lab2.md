# Lab: SQL injection vulnerability allowing to bypass login

![resim](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/c89a468b-c797-4cea-b06e-25031b261381)

In this application, there is a "SQL" vulnerability in the user login section on the website.

![resim-1-1024x535](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/6723b5ee-9573-4588-9f2e-1947177a4be1)

After accessing the laboratory, we are greeted with a website. At this point, we click on the "My Account" section, and we encounter a member login screen. Based on the clue given to us, we know that the administrator username is "Administrator," and we proceed to make an attempt.

![resim-2](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/18f6515b-3a5b-401c-a7fd-107b904c3de2)


We enter the username as "administrator" and a random password. At this point, we will capture this login request using Burp Suite. Before logging in, let's enable FoxyProxy to capture the request.


![resim-3](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/cf9ceab0-0407-4125-8055-239342cd2eeb)

We append '-- to the end of the username, so the query should look like the image below.

![resim-5](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/0548f943-d50c-4b74-9e09-7ca5a1b8b93b)

The "--" symbol after the quotation mark is placed to serve as a comment for the remaining queries, ensuring that only the query before the quotation mark is executed.

![resim-6](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/7713f1da-89be-4052-bb8d-6efedd670315)

As seen in this image, we can change the email address of the administrator account to take control and access the administrator's information.
