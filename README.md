# Telnet-root on TP-Link Archer AX1500

<img src="https://raw.github.com/gmaxus/TP-Link-Archer-AX1500-telnet-root/main/img/router.jpeg" width=50% height=50%>

### Downgrading firmware

<img src="https://github.com/b17e5250-9e30-4a0d-bcb5-6f78ca7be08a" width=50% height=50%>

You need to downgrade from your version of firmware(now it's 1.3.9) to 1.3.1.
Step by step. It's means that if you have 1.3.9 now, you need upload 1.3.8 to your router, then 1.3.4 and 1.3.1.

### Gettin telnet-root
Look CVE-2022-30075 folder.

You mey download your config from router and manualy correct ArcherAX1500v120220401131n/ori-backup-user-config.xml file.
```text
python3 tplink.py -t 192.168.0.1 -p password -b
```

Or

Upload config that activates telnet
```text
python3 tplink.py -t 192.168.0.1 -p password -r ./ArcherAX1500v120220401131n
```

Wait until router will reboot.
Then push the WPS botton on back panel.
Rightest green led on router must glow some time.

Wi-Fi net will be named "THIS-NETWORK!".

Password for network is "password".

Password for admin is "3plex4you".
```text
telnet 192.168.0.1
```
<img src="https://raw.github.com/gmaxus/TP-Link-Archer-AX1500-telnet-root/main/img/telnet.jpeg" width=50% height=50%>

# LINKS
https://github.com/aaronsvk/CVE-2022-30075