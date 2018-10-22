# Laravel Starter Template for AWS Cloud9

Save yourself from agony by using this template for Laravel 5.7 

## Dependencies

- PHP 7.2
- Laravel 5.7
- Composer
- AWS Cloud9 running on EC2 Instance

## Installation

To use this project, follow these steps:

#### Create Blank Cloud9 Instance

<a href="https://aws.amazon.com/cloud9/">AWS Cloud9 IDE</a>

AWS Cloud 9 runs on Linux CentOS distriction. You must use, "yum" commands vs "apt-get"

`use "yum" vs "apt-get"`

#### Install PHP 7.2

Laravel 5.7 requires PHP 7.1 or higher. All AWS CLoud9 EC2 instances come with 5.6 installed. The following steps will removed PHP 5.6 and install PHP 7.2

1) Check which version of PHP installed by running: `php -v`
2) Remove all traces of PHP 5.6: `sudo yum remove php56*`
3) Install PHP 7.2: `sudo yum install php72*`
4) Verify PHP 7.2 is installed: `php -v`

#### Install Composer

Composer is an application-level package manager for the PHP. It makes managing dependencies super easy!

Instructions for downloading Composer can be found here: <a href="https://getcomposer.org/download/">Download Composer</a>

1) In your bash terminal, copy and paste the following commands. Be sure to run the last line.

`
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '93b54496392c062774670ac18b134c3b3a95e5a5e5c8f1a9f115f203b75bf9a129d5daa8ba6a13e2cc8a1da0806388a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
`
2) Check to see if Composer is installed by running: `php composer.phar`. You should be able to see the Composer menu and commands.
3) Clean up the command by running the following: `sudo mv composer.phar /usr/local/bin/composer`. Now you will be able to access composer by typing in `composer` in your bash terminal.

#### Install Laravel

Composer will handle the Laravel installation.

1) Install Laravel: `composer create-project laravel/laravel --prefer-dist`
2) Move all content of this folder to the parent/root level directory and remove the empty folder.
3) Show hidden files: In your file menu (left side), click on the gear icon in the upper right. Make sure, "Show Hidden Files" is checked off. 
4) All Laravel local settings are in your .env file. This is where you store sensative information and this does not get uploaded to your repo. Its up to whoever is setting up their environment to make the correct environment varaibles and settings.

#### Install Database

You may install your database locally or connect with AWS RDS database.

1) Open your .env file and replace the following with your database credientials:

DB_CONNECTION can be: pgsql, mysql, sqlite, etc

`
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret
`

2) Migrate your database by entering the following command: `php artisan migrate`

#### Preview Project

Cloud9 only allows port 8080,8081 and 8082. So you must specify which port to run. 

1) Run server: `php artisan serve --port=8080`. This will run your project on port 8080.
2) Preview project: on the top, next to the green, "Run" button there is an option to "preview". Select, "Preview Running Application"





# laravel-template
