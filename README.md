# Laravel Pet Project
## Set up of environment

1. Install composer

2. Install Laravel's dependencies

```
    sudo apt-get install php7.2-mbstring
```


3. Initialize a Laravel project using composer

```
    composer create-project laravel/laravel {project-name}
```
    
4. Enable the vhost feature, uncomment the line that contains 
`Include etc/extra/httpd-vhosts.conf`:

```
    sudo nano +488 /opt/lampp/etc/httpd.conf
```

5. Setup the root folder for the Virtual Host and the permissions:

```
sudo nano /opt/lampp/etc/extra/httpd-vhosts.conf 
```

For example:

```
    <VirtualHost *:80>
       DocumentRoot "/home/jjimenez/Documents/Training/laravel-training/trainingap$
       ServerName laravel.local.site
       <Directory "/home/jjimenez/Documents/Training/laravel-training/trainingapp/$
           AllowOverride All
           Require local
       </Directory>
   </VirtualHost>
 ```

5. Modify the host file in the operating system to redirect the URL to localhost. For example: 

    `127.0.0.1       laravel.local.site`

6. In the root of the project, execute the following commands:

```   
    sudo find -type d -exec chmod 755 {} \;
    sudo find -type f -exec chmod 644 {} \;
```

7. Restart the apache service to load new values in the config files.

References:

- [Virtual Host setup](https://www.youtube.com/watch?v=2UbpmSNr48c)