![resim](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/4e42bd23-9178-495e-b3b9-3b3e53a47018)

SSRF - Server Side Request Forgery, let's try to tackle our first lab on this topic.

Starting with the information that the application has a stock control feature, let's proceed to access the laboratory.

![resim-1-1024x562](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/c2e92de4-b4c8-4335-beba-d89c074f1300)

Let's click on any of the ones that appear.

![resim-2-1024x792](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/ed3b3537-0085-4e68-8ed0-bce1ab274010)

At this point, the "Check Stock" button catches our eye. Let's send this request to burp and continue examining it from there.

![resim-3](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/01364d57-a1db-4d28-a349-187da7918815)

Here, the "http" request we see in the "stockApi" section is the request responsible for checking the stock of the clicked product.

Our goal at this point is to access the admin interface and attempt to delete the user named "carlos" from the system.

Let's move on to the "Repeater" section and try sending requests to access the admin page.

![Ekran-goruntusu-2024-01-25-052128-1024x279](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/b7e55542-5385-4c57-9f81-7c1bbac62e37)

We send the request trying to access the admin panel from the "stockApi" section, and we receive an "HTTP 200" response.

We have successfully reached the admin page without any issues.

![resim-4](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/431f6ed9-56fa-4831-b4a4-e67060748619)

After reaching the admin page, we send the necessary request to delete the user, delete the user without any problems and the laboratory is resolved.

