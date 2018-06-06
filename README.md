# Statusmonitor

## Example configuration

```ini
[main]
host = smtp.example.com
user = smtp-user
pass = smtp-password
from = sender@example.com
statusfile = /var/www/html/statusmonitor

[Service 1]
url = https://service1.example.com/status
to = receiver1@example.com

[Service 2 with HTTP auth]
url = https://status-user:status-password@service2.example.com/status
to = receiver2@example.com, receiver3@example.com

[Service 2 statusmonitor]
url = https://service2.example.com/statusmonitor
to = receiver2@example.com

[Service 3 custom script]
url = sh: ssh status@service3.example.com -- ./status_script
to = receiver3@example.com
```
