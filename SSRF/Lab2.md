![resim](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/dde7ad76-af63-4f07-8a60-30a1bea57209)

Let's try to solve the second lab specifically focusing on SSRF. It seems that partial information about the IP address and port of the admin panel is provided. At this point, our goal is to access the admin panel and attempt to delete the user named "carlos."

Similar to the previous lab, we will try to gather clues through the stock control feature of the application.

![resim-7-1024x261](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/d0fc2707-4993-4e28-9667-37c20ab47957)

After accessing the lab, when you click on the "View Details" button for any product, you will encounter the "Check Stock" button on the resulting page. Let's capture the request for this button using Burp Suite.

![1](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/289ef346-0fa5-4e21-b4f1-fbbecd191dc9)

We've captured the request. To access the admin panel, let's input the provided IP address and port in the "stockApi" section:

"http://192.168.0.x:8080/admin"

At this point, we'll substitute "x" with "1" and attempt to access the admin panel by trying all numbers between 1 and 255.

![2-1024x226](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/e4b6e96b-2894-49d3-80ff-af4f6e66a45a)

After entering "1" in the specified section, select it on the right side using the "Add" option, and navigate to the "Payloads" section.

![3](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/7271bc88-9fe7-49a7-88b6-e9f4e4324b7f)

Here, in the "Payload type" section, we select "Numbers" because we are only conducting numerical trials.

From: 1 
To: 255
Step: 1 

After completing these options, we will click "Start Attack" and try to catch the number with the HTTP Code "200".

![5](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/fb1fd431-b7d9-40f9-abd0-0ffa505be8eb)

Yes, here we determine that the admin panel is located at "http://192.168.0.58:8080/admin."

Let's perform "Send To Repeater" for the captured request.

![6-1024x275](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/9a61de5c-8696-4903-8a68-39e4a2b5590d)

Let's write the admin panel page we have in the stockApi section, and add the username we want to delete.

![7](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/aaa3ab71-6f3e-4c5c-8073-d853a767c033)

We accessed the admin panel and deleted the user we wanted to delete and exploited the vulnerability.





