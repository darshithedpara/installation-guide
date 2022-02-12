##Install Apache

```shell
sudo apt update
sudo apt install apache2
```

####Replace 3 tags in : `/etc/apache2/apache2.conf`

```shell
<Directory />
	Options Indexes FollowSymLinks Includes ExecCGI
	AllowOverride All
	Require all granted
	Allow from all
</Directory>

<Directory /usr/share>
	AllowOverride None
	Require all granted
</Directory>

<Directory /var/www>
        Order allow,deny
	Options Indexes FollowSymLinks
	AllowOverride All
	Require all granted
	Allow from all
</Directory>
```

Add new tag at end of the file, location : `/etc/apache2/sites-enabled/000-default.conf`

```shell
<Directory /var/www/>
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Order allow,deny
        allow from all
        Require all granted
</Directory>
```

```shell
sudo ufw app list
sudo ufw allow "Apache Full"
sudo ufw enable
```
