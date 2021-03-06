*This is an in-development project, in a very early stage! Please keep that in mind. The release of this thing might
be in early 2014.*

# PHP-MVC

An extremely simple and easy to understand MVC skeleton application, reduced to the max.
Everything is as simple as possible, as readable as possible and as manually as possible.
This project tries to be the extremely slimmed down opposite of big frameworks like Zend2, Symfony or Laravel.

## Why does this project exist ?

One of the biggest question in the PHP world is "How do I build an application ?".
It's hard to find a good base, a good file structure and useful information on that, but at the same time
there are masses of frameworks that might be really good, but really hard to understand, hard to use and extremely
complex. This project tries to be some kind of naked skeleton bare-bone for quick application building,
especially for the not-so-advanced coder.

### This project tries to promote clean and modern PHP coding, by

- fitting PSR 1/2 coding guidelines
- usage of PDO
- promoting the usage of Composer, in exactly the way it should be used
- more or less clean folder/file structure
- promoting developing with max. error reporting

## Installation

1. [TODO] Install mod_rewrite, follow this guideline:
[How to install mod_rewite in Ubuntu](http://www.dev-metal.com/enable-mod_rewrite-ubuntu-12-04-lts/)

2. Create a new database (and remember the name, you'll need that in step 5) and import the SQL file from the
application/_install folder (which contains demo data).

3. Change the .htaccess file from
```
RewriteBase /php-mvc/
```
to where you put this project, relative to the web root folder (usually /var/www). So when you put this project into
the web root, like directly in /var/www, then the line should look like or can be commented out:
```
RewriteBase /
```
If you have put the project into a sub-folder, then put the name of the sub-folder here:
```
RewriteBase /sub-folder/
```

4. Edit the application/config/config.php, change this line
```php
define('URL', 'http://127.0.0.1/php-mvc/');
```
to where your project is. Real domain, IP or 127.0.0.1 when developing locally. Make sure you put the sub-folder
in here (when installing in a sub-folder) too, also don't forget the trailing slash !

5. Edit the application/config/config.php, change this lines
```php
define('DB_TYPE', 'mysql');
define('DB_HOST', '127.0.0.1');
define('DB_NAME', 'php-mvc');
define('DB_USER', 'root');
define('DB_PASS', 'mysql');
```
to your database credentials. If you don't have an empty database, create one. Only change the type `mysql` if you
know what you are doing.

## Useful information

1. SQLite does not have a rowCount() method (!). Keep that in mind in case you use SQLite.

2. Don't use the same name for class and method, as this might trigger an (unintended) __construct of the class.
   This is really weird behaviour, but documented here: http://php.net/manual/en/language.oop5.decon.php

## TODO

Content of DOCUMENTATION.md goes here !

## TODO

TODO file

## What is a model, a view, a controller

### Controller

TODO

### Model

A model is that part of the application that reads, manipulates, deletes etc. data, according to the information
the model gets from the controller. The definition of what a model is or should be is not *really* clear, as a class
that handles all the data of - in this example - the songs can be defined as a model, but also the container that
holds all the data from several models (song model, stats model, etc.) can be defined as "the model". Some MVC
constructs collect data from several models and put everything in a container (let's say $model) and pass this to the
view. The view only accesses this $model, not the real model objects.

### View

TODO

## License

This project is licensed under the MIT License.
This means you can use and modify it for free in private or commercial projects.

The MIT License (MIT)

Copyright (c) 2013 Panique

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Support / Donate

If you think this script is useful and saves you a lot of work, then think about supporting the project by

1. Donating via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=P5YLUK4MW3LDG)
   or [GitTip](https://www.gittip.com/Panique/)
2. Renting your next server at [DigitalOcean](https://www.digitalocean.com/?refcode=40d978532a20).
   SSD servers for $5+ per month or $0.007 per hour (!). PHP-MVC will get a small reward for every new customer.
3. Contributing to this project. Feel free to improve this project with your skills.

## Statistics (by BitDeli)

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/panique/php-mvc/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
