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
