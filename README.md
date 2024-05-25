# telegram_bot_uptime
Check uptime of server and send status to telegram

Telegram bot sends message to you when server is up and running.

python = 3.9.7

Library - https://github.com/luckydonald/pytgbot#releases


How to add the script to autostart with a server(raspberry pi):

* make script executable: chmod +x main.py
* open crontab: crontab -e
* add script to crontab: ``` @reboot python /root/main.py & ```

or

* edit /etc/rc.local file
* add ```python /root/main.py & ``` before ```exit 0```

or 

Add to systemd:
Example of configuration you may find in [the file](systemctl)
* ```cd /lib/systemd/system```
* ```vim uptime-python.service```
* ```chmod 644 uptime-python.service```
* ```systemctl daemon-reload```
* ```systemctl enable uptime-python.service```


#### PS:
* group or channel id - put ```-``` before id
