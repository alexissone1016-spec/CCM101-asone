
**Update your `README.md`:**
```markdown
# Laboratory 09 — Cloud Automation Engineer

## Mission Overview
Eliminated the human element from server backups by writing an automated Bash script, assigning executable permissions, and scheduling it to run autonomously every night at 2:00 AM using Linux Cron.

## Objectives
- Understand Bash syntax, shebangs, and variables
- Write and save executable scripts using nano
- Modify file permissions using `chmod`
- Schedule automated tasks using `crontab`
- Document automation code using Markdown

## Commands Executed
```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
nano backup.sh
./backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
env EDITOR=nano crontab -e