
### **Task 6: Automate Backups with Shell Scripting**  

#### **🔹 Step 1: Write the Backup Script**  
```bash
sudo nano /backups/backup_script.sh
```
Paste the following code inside:
```bash
#!/bin/bash
backup_file="/backups/backup_$(date +%F).tar.gz"
tar -czf $backup_file /devops_workspace
echo -e "\e[32mBackup Successful: $backup_file\e[0m"
```
- Creates a compressed backup of `/devops_workspace`.  

#### **🔹 Step 2: Make the Script Executable**  
```bash
sudo chmod +x /backups/backup_script.sh
```

#### **🔹 Step 3: Schedule it with Cron**  
```bash
crontab -e
```
Add the following line at the end:  
```
0 2 * * * /backups/backup_script.sh
```
- Runs the script **daily at 2 AM**.  

✅ **Task 6 Complete!** 🎯  

---

