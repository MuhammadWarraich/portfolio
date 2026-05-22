# Troubleshooting Commands Used

## Check Server Uptime

```bash
uptime
```

---

## Check Memory Usage

```bash
free -h
```

---

## Check Disk Usage

```bash
df -h
```

---

## Check Apache Status

```bash
systemctl status apache2
```

or:

```bash
systemctl status httpd
```

---

## Check MySQL Status

```bash
systemctl status mysql
```

or:

```bash
systemctl status mariadb
```

---

## Check PHP Processes

```bash
ps aux | grep php
```

---

## Check Apache Error Logs

```bash
tail -n 100 /var/log/apache2/error.log
```

or:

```bash
tail -n 100 /usr/local/apache/logs/error_log
```

---

## Check PHP Version

```bash
php -v
```

---

## Check Active Connections

```bash
netstat -antp
```

or:

```bash
ss -antp
```

---

## Check Running Services

```bash
systemctl list-units --type=service --state=running
```

---

# Note

Actual production output has been removed or sanitized for security purposes.
