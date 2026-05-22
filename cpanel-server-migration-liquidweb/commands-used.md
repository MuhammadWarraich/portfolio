# Commands Used During Migration Verification

## Check Server Hostname

```bash
hostname
```

---

## Check Server IP Addresses

```bash
ip addr
```

---

## Check DNS Resolution

```bash
dig domain.com
```

or:

```bash
nslookup domain.com
```

---

## Check Website Response

```bash
curl -I https://domain.com
```

---

## Check Apache Status

```bash
systemctl status httpd
```

or:

```bash
systemctl status apache2
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

## Check Disk Space

```bash
df -h
```

---

## Check Server Load

```bash
uptime
```

---

## Check Listening Services

```bash
netstat -tulnp
```

or:

```bash
ss -tulnp
```

---

## Check Active Connections

```bash
netstat -antp
```

---

# Note

Actual production output and sensitive information have been removed for security purposes.
