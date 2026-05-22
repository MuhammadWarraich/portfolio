# Rebuild Strategy

## Objective

The objective of the rebuild was to restore a stable hosting environment after identifying severe cPanel and MySQL-related instability.

---

# Planned Recovery Workflow

## Step 1 — Secure Existing Backups

Before rebuilding:

- Verify cPanel backups
- Verify database backups
- Verify website file backups
- Verify email backups

---

## Step 2 — Reinstall Operating System

Selected target environment:

- AlmaLinux
- WHM/cPanel

A fresh installation was selected to avoid carrying corruption into the rebuilt environment.

---

## Step 3 — Deploy Fresh WHM/cPanel

Install and configure:

- WHM
- Apache
- PHP
- MySQL/MariaDB
- DNS services
- Mail services

---

## Step 4 — Restore Hosting Accounts

Restore:

- websites
- databases
- email accounts
- DNS zones

---

## Step 5 — Validate Services

Verify:

- website functionality
- database connectivity
- email functionality
- SSL certificates
- DNS resolution

---

# Important Lessons

- Backup validation is critical
- Fresh deployments are sometimes safer than repairs
- Disaster recovery procedures should be documented in advance
- Hosting environments require proactive maintenance
