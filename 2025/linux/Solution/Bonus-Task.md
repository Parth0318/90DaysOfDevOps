## **🎯 Bonus Tasks**  

1️⃣ **Find the Top 5 Most Common Log Messages**  
```bash
awk '{print $0}' /tmp/Linux_2k.log | sort | uniq -c | sort -nr | head -5
```
- Counts and sorts log messages.  

2️⃣ **Find All Files Modified in the Last 7 Days**  
```bash
find / -type f -mtime -7 2>/dev/null
```
- Lists files modified in the last 7 days.  

3️⃣ **Extract ERROR and WARNING Logs**  
```bash
grep -E "ERROR|WARNING" /tmp/Linux_2k.log > /tmp/filtered_logs.log
```
- Extracts only **ERROR** and **WARNING** logs.  

✅ **Bonus Tasks Complete!** 🚀  

---

### **🎉 All Tasks Completed Successfully!** 🚀  
