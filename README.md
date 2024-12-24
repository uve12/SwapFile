# SwapFile
How to add swapfile to increase RAM on VPS


###  🔧 Swapfile  

A swapfile helps manage memory overflow and ensures smooth server performance. You'll learn how to configure your VPS to add a swapfile for additional memory management.  


### 🖥️ Steps to Buy a VPS  

1. Choose a provider based on your workload requirements.  
2. Pick a plan that suits your resource needs (CPU, RAM, storage, bandwidth).  
3. Follow the checkout process to set up your server and access credentials.  

###  💻 Contabo VPS Deals! 🚀  

📌 VPS 1: https://www.jdoqocy.com/click-101278318-15692486  
4 vCPU Cores | 4 GB RAM | 100 GB NVMe or 400 GB SSD | 32 TB Traffic  

📌 VPS 2: https://www.anrdoezrs.net/click-101278318-13796472  
6 vCPU Cores | 16 GB RAM | 200 GB NVMe | 32 TB Traffic  

📌 VPS 3: https://www.dpbolvw.net/click-101278318-13796474  
8 vCPU Cores | 24 GB RAM | 300 GB NVMe | 32 TB Traffic  

📌 VPS 4: https://www.anrdoezrs.net/click-101278318-13796476  
12 vCPU Cores | 48 GB RAM | 400 GB NVMe | 32 TB Traffic  

💡 *Get started with the perfect VPS for your needs!* 🚀  


---

🔒 Initial Steps After Buying a VPS  

1. Update and upgrade your system to the latest packages.  
🔹Additionally !
2. Set up a firewall to secure your server.  
3. Create a non-root user for daily operations.  
4. Harden SSH access for added security.  
5. Install essential tools for server management.  

---

🔗 Resources:  

👉 Crypto credit Card : https://url.hk/i/en/pw5d2 (code: pw5d2)

📌 Stay Connected:  

🔹 Twitter: https://x.com/cryptoconsol  
🔹 Telegram: https://t.me/cryptoconsol  

---

### 1. Check Existing Swap

Run the following command to check if a swap file already exists:
```
swapon --show
```
If there’s no output, swap is not enabled.


### 2. Verify Available Disk Space

Ensure your VPS has enough free disk space to create a swap file:
```
df -h
```

### 3. Create a Swap File

Create a swap file of the desired size (e.g., 10GB):

```
sudo fallocate -l 10G /swapfile
```

### 4. Set Permissions

Secure the swap file to prevent unauthorized access:
```
sudo chmod 600 /swapfile
```


### 5. Configure the Swap File

Format the file as swap space:
```
sudo mkswap /swapfile
```
Enable the swap:
```
sudo swapon /swapfile
```


### 6. Make Swap Permanent

Add the swap file to /etc/fstab to enable it at boot:
```
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```


### 7. Optimize Swap Settings (Optional)

Reduce swap usage for better performance by adjusting the swappiness value:

```
sudo sysctl vm.swappiness=10
```

To make it permanent, add the setting to /etc/sysctl.conf:
```
echo 'vm.swappiness=10' | sudo tee -a /etc/sysctl.conf
```


### 8. Verify Swap

Check the swap status:
```
free -h
```

The swap file is slower than RAM, so it should be a fallback.


Follow : https://x.com/cryptoconsol
