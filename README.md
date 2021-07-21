# mosquitto

[![Build Status](https://drone.theautomation.nl/api/badges/theautomation/mosquitto/status.svg)](https://drone.theautomation.nl/theautomation/mosquitto)
![GitHub repo size](https://img.shields.io/github/repo-size/theautomation/mosquitto?logo=Github)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/theautomation/mosquitto?logo=github)
![GitHub last commit (branch)](https://img.shields.io/github/last-commit/theautomation/mosquitto/main?logo=github)

[mosquitto](https://mosquitto.org/): an open source message broker that implements the MQTT protocol.


## allow port set firewall rule
```bash
#!/bin/bash
sudo ufw allow 1883/tcp
```

## Add new row in the passwordfile with username and password separated by a colon "username:password"
```bash
#!/bin/bash
echo "<username>:<password>" | sudo tee passwordfile
```

## encrypt the passwords, go into container
```bash
#!/bin/bash
mosquitto_passwd -U /mosquitto/config/passwordfile
```