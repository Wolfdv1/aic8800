Forked from https://github.com/lynxlikenation/aic8800 as I could not compile it on Debian 12 (Bookworm) GNU/Linux firmware  6.1.0-28-amd64  

confirmed now working with an aic8800 device (AX300 Wi-Fi 6 USB Adapter - BL-WN300AX - LB-LINK)  

#### install steps taken  
1. ```
   sudo apt upgrade  
2. ```
   sudo apt install git make dpkg firmware-headers-$(uname -r)  
3. ```
   git clone https://github.com/Wolfdv1/aic8800.git  
4. ```
   cd ./aic8800/drivers/aic8800/  
5. ```
   make  
6. ```
   sudo make install  
7. ```
   sudo modprobe aic8800_fdrv  
8. verification and optionals  
```
lsmod | grep aic8800_fdrv
```
```
sudo nmcli radio wifi on
```
```
sudo systemctl restart networking
```
```
ip link
```
```
sudo reboot  
```

###### No Warranties/licenses other than original source, use at your own risk  
