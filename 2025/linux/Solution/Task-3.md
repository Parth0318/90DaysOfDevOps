### **Task 3: Log File Analysis with AWK, Grep & Sed**  

#### **🔹 Step 1: Download the Log File**  
```bash
wget https://raw.githubusercontent.com/logpai/loghub/master/Linux/Linux_2k.log -O /tmp/Linux_2k.log
```
- Downloads the log file and saves it to `/tmp/Linux_2k.log`.  

---

#### **🔹 Step 2: Extract Insights Using Commands**  

1️⃣ **Find all occurrences of "error" using `grep`**  
```bash
grep -i "error" /tmp/Linux_2k.log
```
- `-i` → Case-insensitive search for "error".  

2️⃣ **Extract timestamps and log levels using `awk`**  
```bash
awk '{print $1, $2, $3}' /tmp/Linux_2k.log | head -10
```
- Prints the first three columns (assuming timestamps and log levels are in the first three fields).  

3️⃣ **Replace all IP addresses with `[REDACTED]` using `sed`**  
```bash
sed -E 's/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+/[REDACTED]/g' /tmp/Linux_2k.log | head -10
```
- Uses regex to match IPv4 addresses and replace them.  

4️⃣ **Find the most frequent log entry**  
```bash
awk '{print $0}' /tmp/Linux_2k.log | sort | uniq -c | sort -nr | head -10
```
- Counts occurrences of each log entry and sorts them in descending order.  

✅ **Task 3 Complete!** 🎯  

