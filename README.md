# WiFi Stuff

This repository collects some information about working with a TP-Link
TL-WN725N rev.2 USB WiFi dongle. It needs the rtl8188eu driver and included
firmware, AP mode is only supported with a custom hostapd version supplied by
Realtek.

## Compiling the driver
```
cd rtl8188eu
make
sudo make install
```

## Compiling hostapd

```
cd rtl8188_hostap/hostapd
cp defconfig-rtl8188 .config
make
```

## Running hostapd
sudo rtl8188_hostap/hostapd/hostapd configuration/hostapd/hostapd.conf
