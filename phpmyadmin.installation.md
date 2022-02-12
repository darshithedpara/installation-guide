##Phpmyadmin Installation

##### 1st Attempt : 
```shell
sudo apt update
sudo apt install phpmyadmin
sudo systemctl restart apache2


mysql -u root
ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';
ALTER USER 'phpmyadmin'@'localhost' IDENTIFIED WITH mysql_native_password BY 'YOUR_NEW_PASSWORD';
GRANT ALL PRIVILEGES ON * . * TO 'phpmyadmin'@'localhost';
FLUSH PRIVILEGES;
```

##### 2nd Attempt : If it's still not working then perform below command : 
```shell
sudo dpkg-reconfigure phpmyadmin
```

##### 3rd and Final Attempt : 
```shell
# After performing 1st and 2nd steps 
# if it is still not working for you then 
# contact Mr. Darshit Hedpara 😆
```
