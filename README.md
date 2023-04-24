# Banana-Pi-W2
LTE router based on Banana Pi W2 board

Custom kernel Based on: https://github.com/BPI-SINOVOIP/BPI-W2-bsp

$uname -a
Linux bpiw2 4.9.119-BPI-W2-Kernel #2 SMP PREEMPT Sat Apr 22 19:49:04 +05 2023 aarch64 GNU/Linux

Features list:
1. Set CPU speed to 300...1400MHz with ondemand governor.
2. Disable all video, multimedia, HID device.
3. Add support for CDC NCM, MBIM, RNDIS modems with modemmanager control.
4. Modem On/Off support with GPIO63.
5. Add support for PCIE and USB WiFi cards (Atheros, Intel, Realtek).
6. Setup isc-dhcp-server as DHCP server. 
7. Setup systemd-resolved as DNS resolver.

Network:
IP address: 192.168.1.1/24
DNS: 8.8.8.8, 8.8.4.4
Login: pi
Passord: bananapi

Modem on bpiw2 board don't recognise inserted SIM card. For fix this bug you need a remove R243. By defaul this resistor pull up USIM_DET signal to USIM_VDD (1.8 or 3.3 volt), but USIM_VDD generated at modem after 1-2 seconds USIM_DET signal asserted to Hi.
![SIM_DET_BPIW2_](https://user-images.githubusercontent.com/65107625/233972016-12b9c20a-11d6-4f2d-bf11-1634d7c19295.jpg)
