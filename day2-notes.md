# Linux Notes Day 2 (DevOps Foundations)

---

## ✅ Difference between `chown` and `chmod`

### `chown` — Change **Ownership**
- Stands for **change owner**
- Modifies **who owns** a file or directory (user and/or group)
- Does **NOT** change permissions

**Examples:**
```bash
chown alice file.txt
chown alice:devops file.txt
```

`chmod` — Change Permissions

- Stands for change mode

- Controls what users can do with a file (read, write, execute)

- Does NOT change ownership

**Example** 
`chmod 755 file.txt`


## ✅ What `tail -f` does
- `tail` shows the last lines of a file
- The `-f` option means follow in real time 
- Commonly used for live log monitoring 

**Example"**
`tail -f /var/log/syslog`

use case : 
- Watching application logs
- Debugging errors as they happen
- Monitoring services in real time

### ✅ How to debug a “disk full” issue
1. Check disk usage `df -h`
2. Find largest directories `du -sh /*`
3. find large files `find / -type f -size +size +1G 2>/dev/null`


### ✅ What systemctl does
- Manages system services in systemd-based Linux systems
- Used to start, stop, restart, enable, disable, and check services
common commands: 
```systemctl status nginx
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
systemctl enable nginx   # start on boot
systemctl disable nginx  # stop from auto-start
```
Use cases: 
- Managing web servers (nginx, apache)
- managing databases (mysql, postgresql)
- Managing background services. 
