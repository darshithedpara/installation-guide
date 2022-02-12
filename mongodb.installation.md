##Mongo DB Installation
```shell
sudo pecl install mongodb
sudo bash
sudo echo "extension=mongodb.so" >> /etc/php/X.X/apache2/php.ini


sudo systemctl restart apache2.service
sudo ufw allow 47017
sudo ufw enable
```

####The last thing to do is to create the directory for mongo to store the data:
`sudo mkdir -p /data/db`

```shell
mongo
use admin
db.createUser({ user: "mongoroot", pwd: "mongowot!@#", roles: [ { role: "root", db: "admin" } ] });
sudo nano /etc/mongod.conf
```

####Update below lines in config files :
```
net:
   bindIpAll: true
security:
  authorization: enabled
```

```shell
sudo systemctl restart mongod
sudo systemctl status mongod
```

```shell
mongo -u yourusername -p --authenticationDatabase admin => optional just do mongo command
show dbs
```
