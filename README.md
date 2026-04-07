## Stack
- osTicket v1.18.3
- XAMPP
- Apache
- PHP 8.2.12
- MySQL
- phpMyAdmin

## What I Did
- Downloaded and extracted osTicket
- Installed XAMPP on Windows
- Moved the osTicket `upload` folder into `C:\xampp\htdocs\osticket`
- Started Apache and MySQL through XAMPP
- Created an `osticket` database in phpMyAdmin
- Created the required `ost-config.php` file from the sample config
- Completed the web-based osTicket installation
- Logged into the osTicket staff/admin panel

## Problems I Ran Into
- Installed the wrong XAMPP/PHP version at first
- Reinstalled XAMPP with PHP 8.2.12 for compatibility
- Ran into a missing configuration file issue
- Hit a MySQL authentication error during installation
- Checked Apache error logs to identify the database login problem
- Created a dedicated MySQL user for osTicket to complete the install successfully

## What I Learned
- How Apache serves files from `htdocs`
- How PHP web apps depend on a web server and database
- How to use phpMyAdmin to create databases and users
- How to read Apache error logs for troubleshooting
- Why using a dedicated database user is better than using `root`
- How a self-hosted ticketing system is deployed locally

## Current Status
The osTicket lab is installed and working locally. Next steps are to configure the help desk environment, create sample users and tickets, and practice ticket workflows.

## Resume Relevance
This lab demonstrates hands-on experience with:
- ticketing systems
- local web application deployment
- Apache/PHP/MySQL setup
- database creation and configuration
- troubleshooting installation and authentication issues
