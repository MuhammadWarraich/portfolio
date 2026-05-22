# cPanel Server Migration – Liquid Web

## Overview

This case study documents a production cPanel server migration completed with Liquid Web support. The migration involved moving hosted websites from an old server to a new server, performing final synchronization, updating hostnames, moving IP addresses, and verifying that websites were live from the new server.

---

# Environment

- cPanel / WHM
- Linux Server
- Apache / PHP
- DNS Management
- IP Address Migration
- Hosting Account Migration
- Liquid Web Managed Support

---

# Problem Statement

The existing hosting server needed to be migrated to a new server environment. The objective was to move hosted accounts and websites safely while minimizing downtime and ensuring that domains continued resolving correctly after the migration.

---

# Objectives

- Complete final data synchronization
- Move IP addresses from old server to new server
- Assign IPs to their original hosting accounts
- Update server hostnames
- Confirm websites were live from the new server
- Remove temporary hosts file entries after migration
- Verify backup status after migration

---

# Migration Process

## 1. Final Synchronization

The final synchronization was completed to ensure that the latest website files, databases, and account data were copied from the old server to the new server.

---

## 2. IP Address Migration

The IP addresses from the old server were moved to the new server and assigned back to their respective original accounts.

This allowed websites to become live from the new server without requiring major DNS changes.

---

## 3. Hostname Updates

The server hostnames were updated after the migration.

Example:

```text
Old server hostname:
host.example.com → old.host.example.com

New server hostname:
temporary-hostname.example.net → host.example.com
```

This helped maintain continuity for the production hosting environment.

---

## 4. Hosts File Testing

During migration testing, local workstation hosts file entries may be used to preview websites on the new server before public DNS cutover.

After the IP swap, those hosts file entries must be removed to avoid incorrect domain resolution.

---

## 5. Backup Verification

After migration completion, backup configuration was reviewed. It was identified that cPanel backups were disabled on the target server, so backup setup became an important post-migration task.

---

# Post-Migration Checklist

- Confirm websites are loading from the new server
- Confirm IP addresses are correctly assigned
- Confirm hostnames are correct
- Remove local hosts file testing entries
- Check DNS resolution
- Check SSL certificates
- Check email delivery
- Enable and verify backups
- Monitor server load after migration

---

# Results

- Final sync completed successfully
- IP addresses moved to the new server
- Websites became live from the new server
- Hostnames were updated
- Migration was considered complete
- Backup configuration issue was identified for follow-up

---

# Skills Demonstrated

- cPanel / WHM server migration
- DNS and IP address management
- Production hosting support
- Linux server administration
- Migration validation
- Hostname management
- Backup verification
- Client/server coordination
- Post-migration troubleshooting

---

# Lessons Learned

- Final sync is critical before cutover
- IP migration can reduce DNS propagation impact
- Hosts file entries must be removed after testing
- Backup status must be verified immediately after migration
- Post-migration checks are as important as the migration itself

---

# Disclaimer

All real server names, IP addresses, domains, and client information have been removed or sanitized for security reasons.
