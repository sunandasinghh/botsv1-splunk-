1.What is the likely IPv4 address of someone from the Po1s0n1vy group scanning imreallynotbatman.com for web application vulnerabilities?

To look for IPv4 address first we look at the source ip address feild.
Query: index=botsv1 imreallynotbatman src_ip=*
       |stats countby src_ip 
       |sort -count

The ans is 40.80.148.42 as we cannot take ip address from internal range. External ip are attackers.



![Alt text](https://github.com/sunandasinghh/botsv1-splunk-/blob/4c463819f98304f09b73eda184dcd931c88003c1/web-defacement-investigation/web-defacement-investigation-q1.jpeg)
