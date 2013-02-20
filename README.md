zf2-tutorial-paginate-sort
==========================

================
    ______ _         _____                 _
    | ___ (_)       |  ___|               | |
    | |_/ /_  __ _  | |__  _ __ ___  _ __ | | ___  _   _  ___  ___
    | ___ \ |/ _` | |  __|| '_ ` _ \| '_ \| |/ _ \| | | |/ _ \/ _ \
    | |_/ / | (_| | | |___| | | | | | |_) | | (_) | |_| |  __/  __/
    \____/|_|\__, | \____/|_| |_| |_| .__/|_|\___/ \__, |\___|\___|
              __/ |                 | |             __/ |
             |___/                  |_|            |___/

Introduction
------------
This tutorial extends the zf2-tutorial by akabat by adding sorting and pagination capabilities.

Installation
------------

Using Composer (recommended)
----------------------------
Clone the repository and manually invoke `composer` using the shipped
`composer.phar`:

    cd my/project/dir
    git://github.com/bigemployee/Big-Sticky-Notes.git
    cd Big-Sticky-Notes
    php composer.phar self-update
    php composer.phar install

(The `self-update` directive is to ensure you have an up-to-date `composer.phar`
available.)

Database
--------
Create zf2tutorial Database and run the following SQL statements to create the table and insert
sample data.

CREATE TABLE album (
  id int(11) NOT NULL auto_increment,
  artist varchar(100) NOT NULL,
  title varchar(100) NOT NULL,
  PRIMARY KEY (id)
);
INSERT INTO album (artist, title)
    VALUES  ('The  Military  Wives',  'In  My  Dreams');
INSERT INTO album (artist, title)
    VALUES  ('Adele',  '21');
INSERT INTO album (artist, title)
    VALUES  ('Bruce  Springsteen',  'Wrecking Ball (Deluxe)');
INSERT INTO album (artist, title)
    VALUES  ('Lana  Del  Rey',  'Born  To  Die');
INSERT INTO album (artist, title)
    VALUES  ('Gotye',  'Making  Mirrors');

open config/autoload/global.php and configure
your Database credentials.


Virtual Host
------------
Afterwards, set up a virtual host to point to the public/ directory of the
project and you should be ready to go!