### **Task 5: Process Management & Monitoring**  

#### **🔹 Step 1: Start a Background Process**  
```bash
ping google.com > /tmp/ping_test.log &
```
- Runs `ping` in the background and saves output to a log file.  

#### **🔹 Step 2: Monitor the Process**  
```bash
ps aux | grep ping
top -n 1 | grep ping
htop
```
- `ps aux` → Lists processes.  
- `top` → Shows running processes.  
- `htop` → Interactive process viewer.  

#### **🔹 Step 3: Kill the Process and Verify**  
```bash
kill $(pgrep ping)
ps aux | grep ping  # Should not show any running process.
```
- Kills the `ping` process using `pgrep`.  

✅ **Task 5 Complete!** 🎯  

