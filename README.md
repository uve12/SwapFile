# SwapFile
How to add swapfile to increase RAM on VPS

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
