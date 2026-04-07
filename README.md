# osTicket Help Desk Lab

Built a local osTicket help desk lab on Windows using XAMPP, Apache, PHP, MySQL, and phpMyAdmin. After deployment, I configured the environment to simulate a small help desk by creating departments, roles, agents, and ticket workflow scenarios.

## Environment
- osTicket v1.18.3
- XAMPP
- Apache
- PHP 8.2.12
- MySQL
- phpMyAdmin
- Windows

## Local URLs
- Main page: http://localhost/osticket/
- Staff/admin login: http://localhost/osticket/scp
- Installer: http://localhost/osticket/setup/
- phpMyAdmin: http://localhost/phpmyadmin
- PHP info page used for troubleshooting: http://localhost/dashboard/phpinfo.php

## File Paths
- XAMPP install folder: `C:\xampp`
- Web root: `C:\xampp\htdocs`
- osTicket folder: `C:\xampp\htdocs\osticket`
- osTicket include folder: `C:\xampp\htdocs\osticket\include`

## Deployment Steps Completed
- Downloaded and extracted osTicket
- Installed XAMPP on Windows
- Moved the osTicket upload folder into `C:\xampp\htdocs\osticket`
- Started Apache and MySQL through XAMPP
- Created the `osticket` database in phpMyAdmin
- Created `ost-config.php` from `ost-sampleconfig.php`
- Completed the web-based osTicket installation
- Logged into the staff/admin panel successfully
- Removed or locked down the setup directory after installation for security

## Initial Configuration Completed

### Departments Created
- IT Support
- Accounts / Access
- Hardware
- Support (Default)

These departments were used to separate ticket ownership by support area.

### Roles Configured
- Tier 1 Support
- All Access

The Tier 1 Support role was configured for normal help desk work, including:
- assigning tickets
- closing tickets
- creating tickets on behalf of users
- editing tickets
- posting replies
- marking tickets as answered
- releasing ticket assignments
- transferring tickets between departments

More sensitive permissions such as deleting tickets, editing other agents' thread items, and knowledge base management were left disabled for Tier 1.

### Agents Added
- Antrun Alvarado — Support
- Bob Brown — IT Support
- Maya Laws — Accounts / Access
- Steve Black — Hardware

These agents were created to simulate a small support team and allow tickets to be assigned to different support areas.

## Ticket Workflow Practice Started
Began testing the ticket lifecycle by creating and routing realistic help desk scenarios.

### First Scenario Completed
**Scenario:** Unable to log in after password reset

**Workflow practiced:**
- ticket creation
- department-based routing
- assignment to the correct support agent
- user-facing response
- internal documentation
- troubleshooting and resolution
- ticket closure

This scenario was used to simulate an Accounts / Access issue and demonstrate a realistic help desk workflow from open to closed.

## Problems Encountered
- Installed the wrong XAMPP/PHP version at first
- Reinstalled XAMPP with PHP 8.2.12 for compatibility
- Hit a missing configuration file issue
- Hit a MySQL authentication error during installation
- Had to check Apache error logs to identify the database login problem
- Had a browser session/cookie issue that blocked login in normal Chrome, but login worked in incognito
- Learned that GitHub folder creation and file path management on the web interface can be confusing during documentation

## Fixes Applied
- Verified PHP version using phpinfo
- Reinstalled XAMPP with PHP 8.2.12
- Copied `ost-sampleconfig.php` to `ost-config.php`
- Created a dedicated MySQL user for osTicket instead of relying on root
- Used a valid placeholder system email instead of `helpdesk@localhost`
- Cleared or isolated browser session issues by testing login in incognito
- Removed or renamed the osTicket setup directory after installation

## Database Notes
- Database name: `osticket`
- Hostname: `localhost`
- Dedicated database user created for osTicket
- phpMyAdmin used to create the database and user account

## Login Notes
- Agent/admin login is done through: `http://localhost/osticket/scp`
- User portal is different from the agent portal
- Session timeout message was caused by a browser session/cookie issue, not bad credentials

## Skills Demonstrated
- Web application deployment on Windows
- Apache, PHP, and MySQL setup with XAMPP
- phpMyAdmin database creation and management
- Help desk ticketing system configuration
- Department-based ticket routing
- Role-based access control
- Help desk agent setup
- Ticket assignment and escalation workflow
- User-facing support communication
- Internal ticket documentation
- Basic troubleshooting and incident handling

## What I Learned
- osTicket is a web application, not a desktop app
- Apache serves files from `htdocs`
- PHP web apps depend on a web server and database
- phpMyAdmin can be used to create databases and users
- Apache error logs are useful for troubleshooting
- A dedicated database user is better than using root
- Help desk systems are more than installation; configuration and workflow design matter
- Departments, roles, and agents make the ticketing system function more realistically
- Internal notes, user-facing responses, and ticket summaries all serve different purposes in support workflows
