
## _create your own service in kali linux_



[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)





## Creation guide 
```
cd /usr/lib/systemd/system/filename.service

To create a file
nano /usr/lib/systemd/system/filename.service

```


copy and paste given code with .service extention.

```[Unit]
Description=Change MAC address at boot time

[Service]
Type=simple
ExecStart=/usr/bin/macchanger -a eth0

[Install]
WantedBy=multi-user.target

```

give executable permission

```
sudo chmod +x /usr/lib/systemd/system/filename.service

```
After that type following command 
```
sudo systemctl enable filename.service
sudo systemctl start filename.service
```

