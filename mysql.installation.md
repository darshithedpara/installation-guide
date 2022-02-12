##MySql Installation

```shell
sudo apt install mysql-server
sudo mysql_secure_installation

#This will ask if you want to configure the VALIDATE PASSWORD PLUGIN.

#Answer Y for yes, or anything else to continue without enabling.

# Enter n/N

# When you’re finished, test if you’re able to log in to the MySQL console by typing:
sudo mysql
mysql> exit

```

```shell
sudo mysql -u root

mysql> USE mysql;
mysql> UPDATE user SET plugin='mysql_native_password' WHERE User='root';
mysql> FLUSH PRIVILEGES;
mysql> exit;

sudo service mysql restart
```
