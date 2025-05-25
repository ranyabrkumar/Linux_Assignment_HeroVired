## 1. System Monitoring

### Script: `monitor_du.sh`

This script logs:
- Disk usage (`df -h`)
- Home directory usage (`du -sh`)
- Top 10 CPU-consuming processes  (` ps ` )
- Top 10 memory-consuming processes ( `top`)

**Log files are saved in:**  
`~/system_monitor/system_info_<YYYY-MM-DD>.log`

#### Usage

```bash
bash monitor_du.sh
```

#### Automate with Cron

To run the script every 10, add to your crontab:

```bash
crontab -e
```
Add:
```
*/10 * * * * /bin/bash /path/to/monitor_du.sh   
```

---
