1.What is the likely IPv4 address of someone from the Po1s0n1vy group scanning imreallynotbatman.com for web application vulnerabilities?

To look for IPv4 address first we look at the source ip address feild.
Query: index=botsv1 imreallynotbatman src_ip=*
       |stats countby src_ip 
       |sort -count

The ans is 40.80.148.42 as we cannot take ip address from internal range. External ip are attackers.



![Alt text](https://github.com/sunandasinghh/botsv1-splunk-/blob/4c463819f98304f09b73eda184dcd931c88003c1/web-defacement-investigation/web-defacement-investigation-q1.jpeg)


2.What company created the web vulnerability scanner used by Po1s0n1vy? Type the company name.

To look for the scanner that is used, look at the user agents feild. In this case http.http_user_agent.
Here there is a Acunetix_wvs_security_test, Acunetix is the ans.


<img width="1280" height="620" alt="web-defacement-investigation-ans2" src="https://github.com/user-attachments/assets/d9f98b1f-0595-46da-afc8-e217b4295699" />


3.What content management system is imreallynotbatman.com likely using?

We search for uri(Uniform Resooource identifiers) helps find the website after domain name.
query= index=botsv1 imreallynotbatman
       |table uri uri_raw

       
<img width="1600" height="878" alt="web-defacement-investigation-ans3 jpeg " src="https://github.com/user-attachments/assets/f0b6bc30-e5a7-4aa8-bd8c-3343deaeca60" />
