# Mosquitto

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