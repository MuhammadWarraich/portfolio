# Commands Used

## Check Uptime

```bash
uptime
```

---

## Check CPU Usage

```bash
ps -eo pid,user,%cpu,%mem,cmd --sort=-%cpu | head -20
```

---

## Check Memory

```bash
free -h
```

---

## Check Disk Space

```bash
df -h
```

---

## Check Large Directories

```bash
du -sh /home/* 2>/dev/null | sort -hr | head -20
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

## Check Logs

```bash
journalctl -xe
```

---

# Note

Actual production server output has been removed for security reasons.
