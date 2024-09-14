# Получение root прав на роутере TP-Link Archer V.1 AX10 (AX1500)

<img src="https://raw.github.com/gmaxus/TP-Link-Archer-AX1500-telnet-root/main/img/router.jpeg" width=70% height=70%>

## Даунгрейд прошивки

<img src="https://raw.github.com/gmaxus/TP-Link-Archer-AX1500-telnet-root/main/img/firmware.jpeg" width=70% height=70%>

Надо даунгрейднуть прошивку до версии 1.3.1, сейчас актуальная версия 1.3.9.
Это надо сделать последовательно, сразу прошиться на 1.3.1 не получится. То есть с 1.3.9 надо перешиться на 1.3.8, потом на 1.3.4 и только потом на 1.3.1.

## Получение рут прав
#### Копирование репозитория
```text
git clone git@github.com:gmaxus/TP-Link-Archer-AX1500-telnet-root.git
```

#### Копирование репозитория
```text
git clone git@github.com:gmaxus/TP-Link-Archer-AX1500-telnet-root.git
```

Следующие действия будут происходить в папке root

```text
cd TP-Link-Archer-AX1500-telnet-root/.
```

Загрузите готовый конфиг ледующе коммандой, где 192.168.0.1 замените на IP адрес и password замените на пароль вашего роутера
```text
python3 tplink.py -t 192.168.0.1 -p password -r ./ArcherAX1500v120220401131n
```

Or

Download your config from router and manualy correct ArcherAX1500v120220401131n/ori-backup-user-config.xml file.
```text
python3 tplink.py -t 192.168.0.1 -p password -b
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
<img src="https://raw.github.com/gmaxus/TP-Link-Archer-AX1500-telnet-root/main/img/telnet.jpeg" width=70% height=70%>

# LINKS
https://github.com/aaronsvk/CVE-2022-30075