###################
sangar-scaffold-spark
###################
A new way to do scaffolding (works with php-activerecord).

Sangar Scaffolds create the files for CRUD operations for you! 

It creates the table on the database, the controller, the models and the views.

It modify also the routes.php file.

You can create forms with the followings elements:

- name
- textarea
- radiobuttons
- checkboxs
- select
- select 1:N (populate the form select with a existent Model)
- upload images (with thumbnail creation and uploads rules)
- upload files (with uploads rules)
- hidden relational (It's a special element. Only one hidden relational by scaffolding is allowed. It will produce a form with relation 1:N linked with his parent form automatically)

Each elements have a validations rules and the possibility to do this multilanguage.

Create also a paginated list view.


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


************
How create a new scaffold
************

- Write the Controller name you want produce.
- Write the Model name you want produce.
- Copy the code blocks of elements that you need and paste to scaffold code input. Each code block must be separated by commas. The scaffold code is a JSON without the first '{' and the last '}'
- Choose the options that you want
- Scaffold!



************
Folder for uploads
************

If you want to uploads files, you must create a folder in your root folder named public, and inside this, another folder called uploads. It will be here where your files will be uploaded. :)




************
CSS for scaffolds
************

If you want, you will find into the resources directory a css to link with your scaffold code. It will look much better. :)



