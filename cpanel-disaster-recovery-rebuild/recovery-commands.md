# Recovery Commands Used

## Check MySQL Status

```bash
systemctl status mysql
```

---

## Attempt Local MySQL Login

```bash
mysql -u root --protocol=socket
```

---

## Stop MySQL Service

```bash
systemctl stop mysql
```

---

## Start MySQL in Recovery Mode

```bash
mysqld_safe --skip-grant-tables --skip-networking &
```

---

## Attempt Root Login in Recovery Mode

```bash
mysql -u root
```

---

## Check Running MySQL Processes

```bash
ps aux | grep mysql
```

---

## Check MySQL Error Logs

```bash
tail -n 100 /var/log/mysql/error.log
```

or:

```bash
journalctl -u mysql
```

---

## Check Server Uptime

```bash
uptime
```

---

## Check Disk Usage

```bash
df -h
```

---

## Check Memory Usage

```bash
free -h
```

---

## Verify Running Services

```bash
systemctl list-units --type=service --state=running
```

---

# Note

All sensitive production output has been removed for security purposes.
