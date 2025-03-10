
### **Task 4: Volume Management & Disk Usage**  

#### **🔹 Step 1: Create a Directory for Mounting**  
```bash
sudo mkdir /mnt/devops_data
```

#### **🔹 Step 2: Create a Loopback Device (For Local Practice)**  
```bash
sudo dd if=/dev/zero of=/mnt/devops_volume.img bs=1M count=100
sudo losetup /dev/loop1 /mnt/devops_volume.img
sudo mkfs.ext4 /dev/loop1
```
- Creates a **100MB** file and treats it as a virtual disk.  

#### **🔹 Step 3: Mount the Volume**  
```bash
sudo mount /dev/loop1 /mnt/devops_data
```

#### **🔹 Step 4: Verify the Mount**  
```bash
df -h | grep devops_data
mount | grep devops_data
```
- `df -h` → Displays disk usage.  
- `mount` → Verifies mounted devices.  

✅ **Task 4 Complete!** 🎯  

