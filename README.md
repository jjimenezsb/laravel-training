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
4. Setup the virtual host following [these](https://www.youtube.com/watch?v=2UbpmSNr48c) instructions

5. Modify the host file in the operating system to redirect the URL to localhost. For example: 

    127.0.0.1       laravel.local.site

6. Restart the apache service to load new values in the config files.