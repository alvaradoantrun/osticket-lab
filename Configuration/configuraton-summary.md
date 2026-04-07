# osTicket Configuration Summary

## Overview
After deploying osTicket with XAMPP, I configured the ticketing environment to simulate a small help desk. This included creating departments, defining support roles, and adding agents assigned to different support areas.

## Departments Created
The following departments were created to simulate different areas of support:

- IT Support
- Accounts / Access
- Hardware
- Support (Default)

### Department Purpose
- **IT Support** was used for general software and technical issues.
- **Accounts / Access** was used for login, password reset, and access-related issues.
- **Hardware** was used for device and equipment problems.
- **Support (Default)** remained as the system default fallback department.

## Roles Configured
Two main support role levels were used:

- Tier 1 Support
- All Access

### Tier 1 Support Permissions
The Tier 1 Support role was configured with permissions appropriate for a front-line help desk technician, including:

- assigning tickets
- closing tickets
- creating tickets on behalf of users
- editing tickets
- posting replies
- marking tickets as answered
- releasing ticket assignments
- transferring tickets between departments

More sensitive permissions such as deleting tickets, editing other agents’ thread items, and managing the knowledge base were left disabled.

### All Access Role
The All Access role was kept as the full-permission administrative role for lab management and configuration.

## Agents Added
The following agents were added to simulate a small support team:

- Antrun Alvarado — Support
- Bob Brown — IT Support
- Maya Laws — Accounts / Access
- Steve Black — Hardware

## Configuration Goals
This configuration was designed to simulate a realistic help desk workflow by:

- separating support responsibilities by department
- assigning agents to specific support areas
- using role-based permissions
- preparing the environment for ticket lifecycle scenarios

## Skills Demonstrated
- Ticketing system configuration
- Department-based ticket routing
- Role-based access control
- Help desk agent setup
- Support workflow planning
