##Install PHP

```shell
sudo add-apt-repository ppa:ondrej/php
sudo apt update
```

####7.0
```shell
sudo apt-get install -y php7.0-{cli,common,opcache,curl,mbstring,mysql,xml,zip,fpm,dev,redis,imagick,bcmath,bz2,intl,gd,mysql,gettext}
```

####7.1
```shell
sudo apt-get install -y php7.1-{cli,common,opcache,curl,mbstring,mysql,xml,zip,fpm,dev,redis,imagick,bcmath,bz2,intl,gd,mysql,gettext}
```

####7.2
```shell
sudo apt-get install -y php7.2-{cli,common,opcache,curl,mbstring,mysql,xml,zip,fpm,dev,redis,imagick,bcmath,bz2,intl,gd,mysql,gettext}
```

####7.3
```shell
sudo apt-get install -y php7.3-{cli,common,opcache,curl,mbstring,mysql,xml,zip,fpm,dev,redis,imagick,bcmath,bz2,intl,gd,mysql,gettext}
```

####7.4
```shell
sudo apt-get install -y php7.4-{cli,common,opcache,curl,mbstring,mysql,xml,zip,fpm,dev,redis,imagick,bcmath,bz2,intl,gd,mysql,gettext}
```

####8.0
```shell
sudo apt-get install -y php8.0-{cli,common,opcache,curl,mbstring,mysql,xml,zip,fpm,dev,redis,imagick,bcmath,bz2,intl,gd,mysql,gettext}
```

####8.1
```shell
sudo apt-get install -y php8.1-{cli,common,opcache,curl,mbstring,mysql,xml,zip,fpm,dev,redis,imagick,bcmath,bz2,intl,gd,mysql,gettext}
```

####Optional Extension
```shell
sudo apt-get install libapache2-mod-phpX.X
sudo apt-get install php-pear
```

```shell
sudo update-alternatives --config php

# select one version using above command and then  
# turn of all the other php version 
# using dismod and then enable one 
php version using enmode command

sudo a2enmod phpX.x
sudo a2dismod phpX.x
```

####Default config variable in below config files: 
- `/etc/php/X.X/apache2/php.ini`
- `/etc/php/X.X/cli/php.ini`
- `/etc/php/X.X/fpm/php.ini`

```dotenv
file_uploads=On
upload_max_filesize=200M
post_max_size=200M
max_execution_time=180
memory_limit=200M
```

####Update mod file : `sudo nano /etc/apache2/mods-enabled/dir.conf` 
```shell
<IfModule mod_dir.c>
    DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
</IfModule>
```

####Move the PHP index file (highlighted above) to the first position after the DirectoryIndex specification, like this:

```shell
<IfModule mod_dir.c>
    DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
```

```shell
sudo systemctl restart apache2
```

