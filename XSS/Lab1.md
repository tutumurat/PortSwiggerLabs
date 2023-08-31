# Lab: Reflected XSS into HTML context with nothing encoded

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/e5b82e23-3e99-42c8-aa28-cac46a30765f)

In this application we will try to catch an XSS vulnerability.

When we access the lab, we see a simple blog site.

To catch the vulnerability at this point, we will inject a javascript code into the browser and make it run.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/a5c68190-baab-44b8-940d-6b3b6cf6250b)

In the search box, type <script>alert('XSS')</script>  and press the search button.

If the browser executes this code, we have caught an XSS vulnerability.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/5795b915-8d60-4cfa-8a16-dc8f4de30a57)

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/ef8a2690-fdf5-43d3-b01e-20b8470f4546)

As you can see, the browser sent us a notification box and we caught the vulnerability.

With this kind of vulnerability, the attacker can execute any javascript code in the browser and launch dangerous attacks through this website.
