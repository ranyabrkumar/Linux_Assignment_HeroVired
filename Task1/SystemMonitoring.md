## 1. System Monitoring
### Install and configure monitoring tools: htop or nmon
![htop_nmon_installation](https://github.com/user-attachments/assets/fef253e5-f29d-451c-9952-363d6193b5ac)

```bash
sudo apt update
sudo apt install htop nmon -y
```

### Script: `monitor_du.sh`

This script logs:
- Disk usage (`df -h`)
- Home directory usage (`du -sh`)
- Top 10 CPU-consuming processes  (` ps command I have used  Or top also we can use | htop is interactive tool and hard to  script ` )
- Top 10 memory-consuming processes ( `ps` )

**Log files are saved in:**  
`~/system_monitor/system_info_<YYYY-MM-DD>.log`

#### Usage

```bash
sh monitor_du.sh
```

#### Automate with Cron

To run the script every 10 min, add to your crontab:

```bash
crontab -e
```

![Crontab_v1](https://github.com/user-attachments/assets/ac171be3-34cb-43e4-a94e-1d38c5353b4c)


```
Add:
```
*/10 * * * * /bin/bash /path/to/monitor_du.sh   
```

---
#### Output log file:
<img width="563" alt="logfile" src="https://github.com/user-attachments/assets/e8e190db-c65d-4c38-82a9-2e2691ede2aa" />

### htop output:
![alt text](image-1.png)

### top output:
![alt text](image.png)