# Lab: DOM XSS in document.write sink using source location.search

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/5cef4fb1-33bb-4b84-87c1-44aba7fe0061)

In this lab we will try to catch a DOM XSS vulnerability.

Let's access the lab.

We see a blog site.

Let's enter a random entry in the search box and examine the source code.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/f3cd3332-53d7-4931-bb51-bf2f62c20715)

At this point, we see the data we entered in the search box in the source code of the page in the following section.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/90821196-a609-428c-985d-cb26578c9f4c)

Now let's add the appropriate code to the search box.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/d400fd6c-61ee-4f11-9ff8-845e55e4d787)

With this code, we will run the onload part and the browser will send an XSS notification to the screen.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/5bb9f184-ed09-47ea-a422-00189d9eb9fc)

## We caught the vulnerability. 


