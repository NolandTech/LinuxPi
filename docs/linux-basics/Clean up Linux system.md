Cleaning up Linux helps free up disk space and improve performance. Here’s a quick guide:

### **1. Remove Unused Packages**

- Remove unnecessary packages:
    
    ```bash
    sudo apt autoremove -y   # Debian/Ubuntu  
    sudo dnf autoremove -y   # Fedora  
    sudo pacman -Rns $(pacman -Qdtq)   # Arch  
    ```
    
- Clean up old package cache:
    
    ```bash
    sudo apt clean && sudo apt autoclean   # Debian/Ubuntu  
    sudo dnf clean all   # Fedora  
    sudo pacman -Sc   # Arch  
    ```

### **2. Find and Remove Large Files**

- Check disk usage:
    
    ```bash
    df -h  
    du -sh /* | sort -h  
    ```
    
- Remove large logs:
    
    ```bash
    sudo journalctl --vacuum-time=7d  
    sudo rm -rf /var/log/*.gz  
    ```

### **3. Clear Temporary Files**

- Manually remove:
    
    ```bash
    rm -rf ~/.cache/* /tmp/*  
    ```
    
- Use a cleaner tool:
    
    ```bash
    sudo apt install bleachbit && bleachbit  
    ```
    

### **4. Remove Old Kernels (If Needed)**

- Ubuntu/Debian:
    
    ```bash
    sudo apt purge $(dpkg -l | awk '/linux-image-[0-9]/{print $2}' | grep -v $(uname -r))  
    ```
    
- Fedora:
    
    ```bash
    sudo dnf remove $(dnf repoquery --installonly --latest-limit=-1 -q)  
    ```
    

### **5. Optimize File System**

- Check for errors:
    
    ```bash
    sudo fsck -A  
    ```
    
- Optimize ext4 file system:
    
    ```bash
    sudo e4defrag /  
    ```
    

Want a more automated way? Try **Stacer**:

```bash
sudo apt install stacer  
stacer  
```
