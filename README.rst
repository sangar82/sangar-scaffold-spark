###################
sangar-scaffold-spark
###################
A new way to do scaffolding (works with php-activerecord)

UNDER DEVELOPMENT!! (The spark isn´t yet into the repository)


*******************
Server Requirements
*******************

PHP version 5.3.5 or newer.


************
Installation
************

Disable index_page
=====================

Sangar-scaffold-spark needs that you don't uses 'index.php' in your base_url.

To disable this function, go to the config folder and edit the config.php



Change

    $config['index_page'] = 'index.php';

for

    $config['index_page'] = '';




Create and .htaccess file in your root folder with the following code:


	AddDefaultCharset UTF-8

	RewriteEngine on

	RewriteCond $1 !^(index\.php|public|robots\.txt)

	RewriteRule ^(.*)$ /index.php/$1 [L]



Removing the index.php file on Codeigniter User Guide:

http://codeigniter.com/user_guide/general/urls.html


************
How to use it?
************

Copy the file controllers/scaffolds.php and views/scaffolds_create.php of this spark in your application directory. Each one in their respective folders.

Go to the scaffold page

	www.yourdomain.com/scaffolds

Follow the instructions and create a new scaffold

This will create the files that you need to do a CRUD operations (controller, model, and two views: create and list).




