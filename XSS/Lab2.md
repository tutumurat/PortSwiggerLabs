# Lab: Stored XSS into HTML context with nothing encoded

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/73d21c53-9335-494a-9d1c-6134800a7ea9)

When we access the lab, we are greeted by a blog site.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/2dceb2ec-bf61-45ab-9f44-d53549da05a0)

We know that this blog site has stored XSS.

Let's find an input field to enter our Javascript code.
For this, we enter a post and look at the comment section.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/155f699b-71db-48b6-ad96-8d13ad97804f)

We injected the code in the comment section, we run it, if the browser runs this code it will show us a notification window.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/45f8d8d8-3d78-4e69-975d-710412666cba)

We successfully submitted the comment and the lab was solved.

![image](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/70636c3f-0b53-4e89-ba6e-8fec1b3d9046)

The browser ran our code and sent us a notification screen with XSS text.

At this point, the attacker can use the comment section to execute various dangerous attacks by running the malicious script they want through the browser.
