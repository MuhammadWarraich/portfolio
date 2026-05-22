# cPanel Disaster Recovery & Server Rebuild

## Overview

This case study documents a disaster recovery scenario involving a corrupted cPanel/WHM environment on a Linux VPS server.

The server experienced severe control panel and MySQL-related issues, making normal administration difficult. A recovery and rebuild strategy was planned to restore hosting functionality using backups and a fresh operating system installation.

---

# Environment

- Linux VPS
- WHM / cPanel
- MySQL / MariaDB
- SSH Administration
- AlmaLinux
- Web Hosting Environment

---

# Problem Statement

The hosting server developed multiple issues affecting cPanel and database functionality.

The environment became unstable and difficult to maintain, while hosting provider support was limited because the VPS service was unmanaged.

The objective became:

- investigate recoverability
- secure backups
- evaluate repair options
- prepare rebuild strategy if necessary

---

# Key Issues Identified

## MySQL Authentication Failure

Attempts to access MySQL locally failed:

```text
ERROR 1045 (28000): Access denied for user 'root'@'localhost'
```

---

## MySQL Socket Connection Failure

Attempts to connect after starting MySQL in recovery mode failed:

```text
ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/var/run/mysqld/mysqld.sock'
```

---

## cPanel Environment Instability

The WHM/cPanel environment became unreliable and difficult to repair safely.

Potential contributing factors included:

- outdated environment
- corrupted services
- failed updates
- database inconsistencies
- legacy operating system concerns

---

# Investigation Process

## Checking MySQL Service

```bash
systemctl status mysql
```

---

## Attempting Local MySQL Login

```bash
mysql -u root --protocol=socket
```

---

## Starting MySQL in Recovery Mode

```bash
systemctl stop mysql
mysqld_safe --skip-grant-tables --skip-networking &
```

---

## Attempting Root Recovery Login

```bash
mysql -u root
```

---

# Recovery Strategy

After evaluating the environment, a rebuild approach was considered safer and more reliable than attempting to repair the corrupted server indefinitely.

The recovery strategy included:

- securing available backups
- reinstalling operating system
- deploying fresh WHM/cPanel environment
- restoring hosting accounts and databases
- rebuilding services cleanly

---

# Rebuild Planning

## Selected Operating System

AlmaLinux with WHM/cPanel was selected for the rebuild process.

---

## Backup Considerations

Available backups were reviewed before rebuild planning.

Important recovery considerations:

- cPanel account backups
- database backups
- website files
- email data
- DNS zone configurations

---

# Results

- Root cause investigation performed
- MySQL issues identified
- Recovery attempts documented
- Backup-first strategy prioritized
- Fresh rebuild approach selected
- Reinstallation planning completed

---

# Skills Demonstrated

- Linux troubleshooting
- MySQL recovery investigation
- Disaster recovery planning
- WHM/cPanel administration
- Backup strategy
- VPS rebuild planning
- Infrastructure recovery
- SSH troubleshooting
- Risk-aware decision making

---

# Lessons Learned

- Unmanaged VPS environments require strong backup discipline
- Recovery attempts should not continue indefinitely on unstable systems
- Backup verification is critical before rebuilds
- Fresh deployments are sometimes safer than prolonged repairs
- Disaster recovery planning should exist before failures occur

---

# Disclaimer

All real server names, IP addresses, usernames, and sensitive information have been removed or sanitized for security purposes.
