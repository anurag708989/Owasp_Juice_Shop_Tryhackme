#owasp juice shop
#1 no questions
#2-lets go for adventure


1-what is administrator email
![](/ctf/tryhackme/owasp%20juice%20shop/administrator_email.png)
admin@juice-sh.op

2-what is the search parameter
![](/ctf/tryhackme/owasp%20juice%20shop/search_parameter.png)
p
3-what does reference in his review
![](/ctf/tryhackme/owasp%20juice%20shop/jim_reference.png)
star trek


#3-inject juice
SQL Injection - SQL Injection is when an attacker enters a malicious or malformed query to either retrieve or tamper data from a database. And in some cases, log into accounts.
Command Injection - Command Injection is when web applications take input or user-controlled data and run them as system commands. An attacker may tamper with this data to execute their own system commands. This can be seen in applications that perform misconfigured ping tests. 
Email Injection - Email injection is a security vulnerability that allows malicious users to send email messages without prior authorization by the email server. These occur when the attacker adds extra data to fields, which are not interpreted by the server correctly. 



use 'or1=1-- as an email paramter for login as admin 




1-log into administrator account


#flag-32a5e0f21372bcc1000a6088b93b458e41f0e02a

![](/ctf/tryhackme/owasp%20juice%20shop/administrator_flag.png)


#4 who broke my lock

token i got from burpsuit 
eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJzdGF0dXMiOiJzdWNjZXNzIiwiZGF0YSI6eyJpZCI6MSwidXNlcm5hbWUiOiIiLCJlbWFpbCI6ImFkbWluQGp1aWNlLXNoLm9wIiwicGFzc3dvcmQiOiIwMTkyMDIzYTdiYmQ3MzI1MDUxNmYwNjlkZjE4YjUwMCIsInJvbGUiOiJhZG1pbiIsImRlbHV4ZVRva2VuIjoiIiwibGFzdExvZ2luSXAiOiIxMC45Ljc4LjMwIiwicHJvZmlsZUltYWdlIjoiYXNzZXRzL3B1YmxpYy9pbWFnZXMvdXBsb2Fkcy9kZWZhdWx0LnN2ZyIsInRvdHBTZWNyZXQiOiIiLCJpc0FjdGl2ZSI6dHJ1ZSwiY3JlYXRlZEF0IjoiMjAyMC0wOS0zMCAxNjoxMjo1NC4wMTMgKzAwOjAwIiwidXBkYXRlZEF0IjoiMjAyMC0wOS0zMCAxNjoxNjo0Mi45OTQgKzAwOjAwIiwiZGVsZXRlZEF0IjpudWxsfSwiaWF0IjoxNjAxNDgyNjg5LCJleHAiOjE2MDE1MDA2ODl9.VdEsSrVkLUrUR4WkpQyeJIMEo4cG3HfobBP5QkW9hpru20Gl7_Wx7gJtc6RplE1MmYxgga7OiTGK2OHKerub-cTojQzfT5P4O9yx8Z-AnghfBDJyz2JHm_ASrlqxweDe56jCBYQK2oQOHhsMJHvzHFMk25agBQhM39wMQhMp6bA
![](/ctf/tryhackme/owasp%20juice%20shop/tokendecoding.png)
decode your token at-https://devtoolzone.com/decoder/jwt
password from token decoder-0192023a7bbd73250516f069df18b500
hash-type found- md5
password-admin123
![](/ctf/tryhackme/owasp%20juice%20shop/cracking_hash.png)
1-Brute force the administrator account password
using burp suit intruder for setuping the payload and then brute forcing the 
passwords
c2110d06dc6f81c67cd8099ff0ba601241f1ac0e



2-reset jim password
![](/ctf/tryhackme/owasp%20juice%20shop/jimflag.png)

094fbc9b48e525150ba97d05b942bbf114987257

#5-AH dont look
1-confidential document acquisitions.md
 edf9281222395a1c5fee9b89e32175f1ccf50c5b

2-log into MC safeSearch's Account

Mr. N00dles

token-
eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJzdGF0dXMiOiJzdWNjZXNzIiwiZGF0YSI6eyJpZCI6OCwidXNlcm5hbWUiOiIiLCJlbWFpbCI6Im1jLnNhZmVzZWFyY2hAanVpY2Utc2gub3AiLCJwYXNzd29yZCI6ImIwM2Y0YjBiYThiNDU4ZmEwYWNkYzAyY2RiOTUzYmM4Iiwicm9sZSI6ImN1c3RvbWVyIiwiZGVsdXhlVG9rZW4iOiIiLCJsYXN0TG9naW5JcCI6IjEwLjkuNzguMzAiLCJwcm9maWxlSW1hZ2UiOiJhc3NldHMvcHVibGljL2ltYWdlcy91cGxvYWRzL2RlZmF1bHQuc3ZnIiwidG90cFNlY3JldCI6IiIsImlzQWN0aXZlIjp0cnVlLCJjcmVhdGVkQXQiOiIyMDIwLTA5LTMwIDE2OjEyOjU0LjAyMCArMDA6MDAiLCJ1cGRhdGVkQXQiOiIyMDIwLTA5LTMwIDE3OjU2OjMxLjYyMyArMDA6MDAiLCJkZWxldGVkQXQiOm51bGx9LCJpYXQiOjE2MDE0ODg2MTgsImV4cCI6MTYwMTUwNjYxOH0.V5kxA_nsRz-naFDQnPth_V7liu4zJzz673UtFg2KbvYWzIP7jIx75UFT8kK5MV2gfofkvr9pjoO1_-gJpnYhNtM6lq-8Ib6XwbRBZjryz86jB-8Yb6FBgUYM5iUvU4d3Ewi-NvsEEFAJghwOkBPkxTQNkIy3Q0nVSPtqq9EA-6g
password hash-b03f4b0ba8b458fa0acdc02cdb953bc8
it doesnot works
3-forgotten developer backup
 bfc1e6b4a16579e85e06fee4c36ff8c02fb13795 




2- log  into bender account using bender@juice-sh.op'-- as the email
fb364762a3c102b2db932069c0e6b78e738d4066
