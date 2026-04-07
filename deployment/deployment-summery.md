# osTicket Setup Notes

Built a local osTicket help desk lab on Windows using XAMPP, Apache, PHP, MySQL, and phpMyAdmin.

## Environment
- osTicket v1.18.3
- XAMPP
- Apache
- PHP 8.2.12
- MySQL
- phpMyAdmin

## Local URLs
- Main page: http://localhost/osticket/
- Staff/admin login: http://localhost/osticket/scp
- Installer: http://localhost/osticket/setup/
- phpMyAdmin: http://localhost/phpmyadmin
- PHP info page used for troubleshooting: http://localhost/dashboard/phpinfo.php

## File Paths
- XAMPP install folder: C:\xampp
- Web root: C:\xampp\htdocs
- osTicket folder: C:\xampp\htdocs\osticket
- osTicket include folder: C:\xampp\htdocs\osticket\include

## Setup Steps Completed
- Downloaded and extracted osTicket
- Installed XAMPP on Windows
- Moved the osTicket upload folder into C:\xampp\htdocs\osticket
- Started Apache and MySQL through XAMPP
- Created the osticket database in phpMyAdmin
- Created ost-config.php from ost-sampleconfig.php
- Completed the web-based osTicket installation
- Logged into the staff/admin panel successfully

## Problems Encountered
- Installed the wrong XAMPP/PHP version at first
- Reinstalled XAMPP with PHP 8.2.12 for compatibility
- Hit a missing configuration file issue
- Hit a MySQL authentication error during installation
- Had to check Apache error logs to identify the database login problem
- Had a browser session/cookie issue that blocked login in normal Chrome, but login worked in incognito

## Fixes Applied
- Verified PHP version using phpinfo
- Reinstalled XAMPP with PHP 8.2.12
- Copied ost-sampleconfig.php to ost-config.php
- Created a dedicated MySQL user for osTicket instead of relying on root
- Used a valid placeholder system email instead of helpdesk@localhost
- Cleared/isolated browser session issues by testing login in incognito

## Database Notes
- Database name: osticket
- Hostname: localhost
- Dedicated database user created for osTicket
- phpMyAdmin used to create the database and user account

## Login Notes
- Agent/admin login is done through: http://localhost/osticket/scp
- User portal is different from the agent portal
- Session timeout message was caused by a browser session/cookie issue, not bad credentials

## What I Learned
- osTicket is a web app, not a desktop app
- Apache serves files from htdocs
- PHP web apps depend on a web server and database
- phpMyAdmin can be used to create databases and users
- Apache error logs are useful for troubleshooting
- A dedicated database user is better than using root
