# TestLink Server Performance Optimization Case Study

## Overview

This case study documents a real-world server performance investigation performed on a Linux-based TestLink hosting server. The server was hosting multiple TestLink and WordPress-based test environments, some of which were inactive or no longer required.

The goal was to investigate server performance issues, identify unnecessary hosted instances, coordinate cleanup with the development team, and improve overall server stability.

---

## Environment

- Linux VPS Server
- Apache / PHP-FPM
- MySQL / MariaDB
- WordPress-based test websites
- TestLink environments
- SSH access
- WHM/cPanel-style hosting environment

---

## Problem Statement

The TestLink server was experiencing performance concerns due to multiple hosted test websites and inactive environments. Some websites were still present on the test server even though their live versions were already active on the production server.

This created unnecessary server load and made it harder to maintain the test environment efficiently.

---

## Objectives

- Check current server health
- Review server load and resource usage
- Identify active and inactive hosted websites
- Prepare a list of test websites
- Compare test websites with live websites
- Coordinate with developers to confirm which test websites could be removed
- Improve server performance by reducing unnecessary hosted accounts/sites

---

## Investigation Steps

### 1. Checked Server Uptime and Load Average

The server uptime and load average were reviewed to understand the current performance condition.

```bash
uptime
